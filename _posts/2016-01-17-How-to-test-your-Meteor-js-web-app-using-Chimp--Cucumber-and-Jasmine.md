---
title: 'How to test your Meteor.js web app using Chimp, Cucumber and Jasmine'
date: '2016-01-17T11:37:05.801Z'
excerpt: >-
  After sharing my struggle in finding the right tools and from-scratch
  procedures; I provide simple instructions to test your Meteor project…
layout: post
---
I feel that automated tests are like teenage sex: developers talk a lot about it, but only few of them actually do it. (at least from the developers I talk with)

Yesterday, while I was integrating a complex login/signup flow on a [Meteor.js](https://www.meteor.com/) web app for a client, I felt that this complexity could lead to future bugs. So I decided to write a test to make sure that it won’t fall apart on any future commit.

> **EDIT**: At the time, I was using **Chimp v0.24.1**, running on **Node v0.12.9**.  
> Be careful, Chimp is evolving a lot, so this tutorial may already be deprecated.

My problems were:

*   I have very little experience with automated testing,
*   I had never written tests for a Meteor.js app,
*   and I was confused about the current best practices (if any) with that technology: [*What tool should I use*](http://xolv.io/blog-posts/2015/11/6/the-seven-testing-modes-of-meteor)*?*

#### Why did I struggle?

Apparently MDG had [decided to use Velocity as their standard test driver](http://info.meteor.com/blog/meteor-testing-framework-velocity), but I could not see any reference to testing (besides tinytest for testing packages) in [Meteor.js’ official documentation](http://docs.meteor.com/#/full/) and [guide](http://guide.meteor.com/).

I also read that [Chimp was the direction MDG was currently heading towards](https://forums.meteor.com/t/the-state-of-velocity-and-testing-in-meteor/15084/9). But I spent some time understanding how to setup my tests from scratch, because I had to discover several tools and langages at once:

*   [Chimp](https://github.com/xolvio/chimp) (the test runner),
*   [Cucumber](https://cucumber.io) (the langage for writing test scenarios),
*   and [Jasmine](http://jasmine.github.io/2.3/introduction.html#section-Expectations) (the the langage for expressing test validation criteria).

Moreover, these tools are generic, and Meteor.js brings additional objects and methods that can (or must) be used from Chimp and Cucumber.

#### The setup process

As explained on [their documentation](https://chimp.readme.io/docs/tutorial), I installed Chimp globally using \`npm install -g chimp\` so that I could run the \`chimp\` command from anywhere. On the first run, Chimp installed webdriver (or scelenium, I don’t remember).

But, the first run concluded with a weird error: \`Directory features does not exist. Not running\`, and I had not found any mention of that directory (or error) in Chimp’s documentation.

I had to find in [this tutorial](https://chimp.readme.io/docs/tutorial) that tests had to be described in a \`features\` directory, using the [Gherkin langage](https://cucumber.io/docs/reference#gherkin). So I added a \`./tests/features/test.feature\` file in my Meteor.js project, to see what would happen:

    @watch  
    Feature: Search the Web  
      
      As a human  
      I want to search the web  
      So I can find information  
      
      Scenario: Search for Xolv.io  
        Given I have visited Google  
        When I search for "Xolv.io"  
        Then I see "Xolv.io"

As Chimp was running in \`watch\` mode, it provided me with some code in the console, to help me implement the corresponding tests:

    You can implement step definitions for undefined steps with these snippets:  
      
    this.Given(/^I have visited Google$/, function () {  
      // Write the automation code here  
      pending();  
    });  
      
    this.When(/^I search for "([^"]*)"$/, function () {  
      // Write the automation code here  
      pending();  
    });  
      
    this.Then(/^I see "([^"]*)"$/, function () {  
      // Write the automation code here  
      pending();  
    });

So, by following the tutorial, and reading [Cucumber-js’ docs](https://github.com/cucumber/cucumber-js), I wrote the following \`./tests/features/support/defs.js\` file:

    module.exports = function() {
     // Hooks
     // this function is run before testing each scenario.  
      // it makes sure that we're using a test (i.e. empty) database.  
      this.Before(function(scenario) {  
        console.log('meteor running on:',  
          server._original.host + ‘:’ + server._original.port);  
        console.log(‘about to test:’, scenario.getName());  
        var result = server.execute(function() {  
          console.log(‘counting...’); // displays in Meteor's console  
          return Meteor.users.find().fetch().length;  
        });  
        expect(result).toEqual(0);  
      });
     // this function is run after testing each scenario    
      this.After(function(scenario) {  
        // TODO: clean DB, to prevent side-effects between tests  
      });
     // Tests
     this.Given(/^I have visited Google$/, function () {  
        browser.url('http://google.com'); // ...or localhost:3000 ^^  
        // browser = WebdriverIO instance  
      });  
      
      this.When(/^I search for "([^"]*)"$/, function (searchTerm) {  
        browser.setValue('input[name="q"]', searchTerm);  
        browser.keys(['Enter']);  
      });  
      
      this.Then(/^I see "([^"]*)"$/, function (link) {  
        browser.waitForExist('a=' + link);  
      });
     // I also added this test, based on another example:  
      this.Then(/^They see the title "([^"]*)"$/, function(title) {  
        browser.saveScreenshot("screenshot.png");  
        expect(browser.getTitle()).toEqual(title); // Jasmine Expect  
      });    
    }

When both files are correct, and Chimp is running in watch mode from the ./tests directory, it’s working awesomely!

*   Chimp opens a Chrome browser, and we can see tests running in that window, like if a real human user was doing it!
*   Test results display in Chimp’s console.

But my \`Before\` hook prevents the tests from actually running, because the database is not empty. Indeed, as advised by [Chimp’s Meteor tutorial](https://chimp.readme.io/docs/getting-started-with-meteor-cucumber), I had launched Chimp that way:

    chimp --ddp=[http://localhost:3000](http://localhost:3000) --watch

…which connects to my development Meteor.js instance, and thus, to my development database (containing data: users, etc…).

I found on a forum that it was ok to run two Meteor instances:

*   one for development, by just running the \`meteor\` command;
*   and one for testing, by specifying different HTTP and DB ports.

So I ended up writing the following \`./tests.sh\` script that I use today:

    #!/bin/bash
    # Startup Chimp testing instance  
    MONGO_PORT=3001  
    METEOR_PORT=3100
    echo After METEOR IS READY, run: chimp --path=tests \  
         --ddp=[http://localhost:$METEOR_PORT](http://localhost:$METEOR_PORT) --watch
    bash -c "MONGO_URL=mongodb://localhost:$MONGO_PORT/chimp_db \  
         meteor --port $METEOR_PORT $@"

When I’m working on my project:

*   I run \`meteor\` to start the development instance, as usual;
*   then I run \`./tests.sh\` in another console, to start the testing instance.
*   When, the testing instance is running, I copy-paste the chimp command printed by my script, to yet another console.

That way, I’m able to develop as usual from localhost:3000, using my development database; and to run tests in the background, on a dedicated (clean) database.

#### In a nutshell (tl;dr)

If you want to add end-to-end tests using Chimp+Cucumber+Jasmine to your Meteor.js project:

*   Install Chimp;
*   Copy-paste the code blocks provided above, into the corresponding files;
*   Run ./tests.sh to start your testing Meteor instance, then the printed Chimp command to actually run the tests.
*   Add feature descriptions using Cucumber’s [Gherkin langage](https://cucumber.io/docs/reference#gherkin).
*   Add test definitions using [Cucumber-js’ doc](https://github.com/cucumber/cucumber-js), the [browser object API](http://webdriver.io/api.html), Meteor’s [server and client objects](https://chimp.readme.io/docs/getting-started-with-meteor-cucumber), and [Jasmine’s expectations](http://jasmine.github.io/2.3/introduction.html#section-Expectations).
