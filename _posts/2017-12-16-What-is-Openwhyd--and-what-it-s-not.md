---
title: 'What is Openwhyd, and what it‘s not.'
date: '2017-12-16T13:19:28.487Z'
subtitle: My answers to frequently asked questions.
excerpt: My answers to frequently asked questions.
thumb_img_path: images/What-is-Openwhyd--and-what-it-s-not/1*Jcd2lWxS8Z0GdRivxm-eEg.jpeg
layout: post
---
Everybody loves music. And many people have high expectation on how music should be found, played and shared.

As a free and open-source music curation platform, [Openwhyd](https://openwhyd.org/) gives high hopes to thousands of music lovers looking for an alternative to Spotify and other “legal streaming” platforms.

In this quick blog post, I answer to questions I’m getting a lot about Openwhyd.

* * *

![](/images/What-is-Openwhyd--and-what-it-s-not/1*Jcd2lWxS8Z0GdRivxm-eEg.jpeg)

<figcaption>Spoiler alert: yes, he&nbsp;exists!</figcaption>

### Does Tony, the “Chief BBQ Officer” really exist?

Yes! And a proof if given on the photo above! 👆

When Openwhyd was still a startup product (called Whyd), Tony was in charge of communicating with our users, and he loved organising barbecues and parties so that we could regularly meet them. So, even though the role sounds funny, it was not completely a joke at the time!

Since the Whyd company shifted its focus to building smart speakers, Tony has moved on to another full time opportunity. And he agreed to let Openwhyd send welcome emails on his behalf.

As you guessed, these welcome emails are send automatically by Openwhyd whenever a new user signs up, and Tony does not longer receives replies to them. That being said, your replies are redirected to our official contact email address, so I receive them and do my best to reply to everybody! ✍️

* * *

![](/images/What-is-Openwhyd--and-what-it-s-not/1*bTCjUBX6DkDwFnPQp1XWlw.png)

<figcaption>This is how Openwhyd displays removed tracks. We don’t delete them from your playlists.</figcaption>

### What happens when one of the tracks I added is removed from Youtube?

Shit happens. Tracks get removed sometimes, especially on Youtube.

If you keep your playlists on youtube.com, be warned that any track that is removed will also be deleted from the playlists you had added it to, without warning. 😱

At Openwhyd, we know that many music lovers (myself included) are obsessed about being in control of the information that is kept in their collection of music. So we do things differently: when a Youtube track is removed, it is **not** deleted from your Openwhyd playlists. Even though the track will not play anymore, its title, description and comments added on openwhyd.org will stay. 🗃

This situation is not perfect, but it’s important for us that the list of tracks that we patiently collected on Openwhyd will never be altered.

If it’s important for you to be able to play a removed track, feel free to delete that removed track from your Openwhyd playlist, and re-add it from another source. It’s up to you.

* * *

### Is there a way to stream just the audio signal (e.g. from Soundcloud) of a given video track?

Maybe, but we’re not going to do it.

Firstly, Youtube does not allow to stream a track’s audio without displaying the video.

Secondly, I’ve spent weeks trying to find matches of tracks automatically from one streaming platform to another. My conclusion was that it would work just 50% of the time, or many matches would be incorrect. Especially because many Openwhyd users collect tracks that are rare, in very specific versions and/or available through just one platform.

If you really want to have a more bandwidth-efficient way to listen to music, I invite you to try a “legal streaming” music platform like Spotify instead. Because Openwhyd was not designed for that.

* * *

![](/images/What-is-Openwhyd--and-what-it-s-not/1*bhuzfgC2A30_hWhDevEVbQ.png)

### Is it possible to follow playlists rather than users?

I agree that some of the music lovers you follow may share a wide range of genres on Openwhyd, and that you might be interested in following just one or two of their playlists. That’s a feature that I’ve wanted badly to have too!

Unfortunately, this feature would have a heavy footprint on Openwhyd’s source code and infrastructure. Therefore it would require a lot of work from developers, to implement and maintain it over time. So far, none of our contributors offered this kind of commitment. If you would like to help, please say hi there: [https://github.com/openwhyd/openwhyd/issues/129](https://github.com/openwhyd/openwhyd/issues/129)

* * *

### Is there a “dark mode” design of Openwhyd?

We don’t provide design customisation features, sorry…

That being said, several browser extensions exist to help to change the design of any website. For instance:

[**Stylish - Custom themes for any website**  
*Customize any website to your color scheme in 1 click, thousands of user styles with beautiful themes, skins & free…*chrome.google.com](https://chrome.google.com/webstore/detail/stylish-custom-themes-for/fjnbnpbmkenffdnngjfgmeleoegfcffe "https://chrome.google.com/webstore/detail/stylish-custom-themes-for/fjnbnpbmkenffdnngjfgmeleoegfcffe")[](https://chrome.google.com/webstore/detail/stylish-custom-themes-for/fjnbnpbmkenffdnngjfgmeleoegfcffe)

* * *

### Is it possible to edit a playlist collaboratively?

We started working on collaborative playlists several years ago, but ended up cancelling that feature because it was making our product more complicated and confusing to use, and it was costly to implement and maintain. ❌

Developers, if you ever want to give life to this feature in your own version of Openwhyd, there are still traces of its foundations in Openwhyd’s source code!

[**openwhyd/openwhyd**  
*openwhyd - 💎 Discover, collect and play music from Youtube, Soundcloud, Bandcamp, Deezer and other streaming platforms*github.com](https://github.com/openwhyd/openwhyd/search?utf8=%E2%9C%93&q=collaborative+playlist&type= "https://github.com/openwhyd/openwhyd/search?utf8=%E2%9C%93&q=collaborative+playlist&type=")[](https://github.com/openwhyd/openwhyd/search?utf8=%E2%9C%93&q=collaborative+playlist&type=)

* * *

### How to play Openwhyd tracks on Android phones?

It’s complicated to stream tracks in mobile web browsers, and we don’t have an Android app yet, sorry…

There is hope, though: one of Openwhyd’s contributors has rebuilt a good chunk of openwhyd.org using the React technology: [https://sound-nuggets.xyz](https://sound-nuggets.xyz) 💪

This is great news, because the use of React will make it easier to build a React Native app, and therefore to build an Android app!

If you want to help, please write a comment on this post: [https://www.facebook.com/groups/openwhyd/permalink/1999454520336097/](https://www.facebook.com/groups/openwhyd/permalink/1999454520336097/) (*note: you will need to join our Facebook group first*)

* * *

### Can’t we display advertising to raise money, so that we can pay developers to add new features?

We did think of that, when the Openwhyd platform was still the main product of the Whyd company.

Based on its usage (i.e. the website is kept in the background all the time), our conclusions were that displaying advertising would not bring enough cash to pay the development of the platform. 💸

We also [thought of other ways to generate revenue](https://github.com/openwhyd/openwhyd/issues/101#issuecomment-336666263), but they are controversial: play audio ads between tracks, integrated sponsored music tracks in your stream, heat up your CPU to mine bitcoins while you’re playing music…

Now, here are reasons why I believe that it’s better for Openwhyd to rely on donations and sponsoring:

*   It gives users (especially non-developers) an opportunity to contribute to sustaining Openwhyd. I.e. show actively that they care about the platform.
*   Seeing that users still donate to sustain the project, developers are more motivated to contribute, because they know that at least these users will really care about these contributions. In other words, the presence of donations indirectly increase the value and impact of contributions.
*   Also, I’m not a lawyer, but remaining a human-sized and non-profit project makes us less of a threat to music right-holders and streaming platforms. Complaints are easier to deal with when you don’t make money.

For all these reasons, I prefer to stick to donations and partnerships to support the costs of Openwhyd’s technical infrastructure, and rely on intrinsic motivation of developers who want to get involved in evolving the project. ✊

* * *

### Why don’t we host Openwhyd on a cheaper hosting server, to reduce costs?

DigitalOcean has been our hosting provider for years. It’s not cheap, but we picked an extremely performant and reliable solution to maintain an awesome quality of service without spending too much time caring about our infrastructure.

When we decided to turn Whyd into an open-source project, it was running on a very powerful server that costed $150/month. With help from the team, I migrated it to a smaller instance, in order to reduce that cost to $48/month. This process was risky and tedious, because our codebase was getting old (i.e. relying on deprecated dependencies) and we were lacking internal documentation on how to do this migration properly.

Sure, we could migrate to an even smaller server, but the platform may become slower. Or we could switch to a cheaper provider, but who is going to commit to maintain the infrastructure 24/7 in case of problems? In both cases, I’m not interested in spending time migrating anytime soon. ✋

Moreover, DigitalOcean loves Openwhyd, so they offered us 1 year of free hosting! 😍

* * *

### By doing XXX or ZZZ, Openwhyd can become a major player in the market and attract many more users

I would like to make this clear: the goal of Openwhyd is not (and will never be) to make money. It’s not a business, it’s a non-profit and collaborative project. It will always be.

Our objective is not to “win” anything or anyone. It’s rather to sustain a platform that our community of music lovers use to discover, play and share music. Its also a good project for developers to gain experience collaborating on a real-world open-source product and improve their programming skills.

As explained in [my previous article](https://medium.com/openwhyd/the-future-of-openwhyd-9a39e0839ac3), my vision for the future of Openwhyd is about empowering developers to implement their ideas on top of Openwhyd’s platform. Make it easier for them to create external applications (e.g. mobile apps, different UIs, additional features…) that Openwhyd users could use to enhance their experience. (i.e. similarly to applications that allow you to connect to your Facebook account)

If you wish for a better Openwhyd and want to hire developers to make it, you can freely “fork” [Openwhyd’s source code](https://github.com/openwhyd/openwhyd) and create your own version of it from the existing implementation. That’s one of the good things about open sources licenses like the one we’ve chosen (MIT license). But keep in mind that I will not be involved in such a project.

* * *

### If Openwhyd ever dies, how can I get my data back?

Don’t worry too much about that. 😌

As a music lover, I care a lot about the safety of the collection of tracks I’ve maintained for years on [my Openwhyd profile](https://openwhyd.org/adrien). So I’ve put everything in place so that no one ever loses their tracks!

Firstly, you can export your data (e.g. tracks and playlists) in standard JSON format at anytime, [as explained in our official FAQ](https://github.com/openwhyd/openwhyd/blob/master/docs/FAQ.md#how-to-export-my-tracks--comment-exporter-ma-musique-en-csv-ou-json-).

Secondly, Openwhyd will only die if we ever run out of donations. So, if you really don’t want to let it die, you can help keeping our tanks full by donating through our Open Collective page:

[**Openwhyd - Open Collective**  
*Music curation platform that supports streaming tracks from Youtube, Soundcloud, Bandcamp, Deezer, Vimeo, Dailymotion…*opencollective.com](https://opencollective.com/openwhyd "https://opencollective.com/openwhyd")[](https://opencollective.com/openwhyd)

Last but not least, I backup all Openwhyd’s data every week. So, if something bad ever happens on our technical infrastructure, I will still be able to recover and provide a recent snapshot of your data.

* * *

![](/images/What-is-Openwhyd--and-what-it-s-not/1*x10kb4EuznT7R57i-voHtQ.jpeg)

<figcaption>Point FMR (Paris, France), one of the places where Tony organised a party for&nbsp;Whyd.</figcaption>

### Can we organise a party with fellow Openwhyd users?

That would be awesome! 🎵🍻🎉

If you want to organise one, I’m happy to help!

Good first steps would be to pick a place, a date, and convince at least 10 people to come. Go go go!

* * *

I hope that my answers gave you a better understanding of Openwhyd, the way we operate, and its direction!

#### If you have any question, please write a reply below! 🤗

Never stop jamming! 🔥
