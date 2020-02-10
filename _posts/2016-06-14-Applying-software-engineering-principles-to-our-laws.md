---
title: Applying software engineering principles to our laws
date: '2016-06-14T02:13:11.115Z'
excerpt: >-
  I think that the French political system is outdated and has become too
  complex.
layout: post
---
I think that the French political system is outdated and has become too complex.

As a software engineer, I believe that some of our best practices could (and should?) apply to the way our laws are written. Because laws can be considered as the source code of a democratic system.

Here are a few Software Development principles that could also be applied to our laws:

*   Separation of concern: The code should be divided in well-designed modules that have only one purpose. Each module has publicly visible interfaces that can be used by other modules, describing its features/functionalities, and thus, a contract that they agree to fulfil towards these modules.
*   Modularity; each file defines a module that relies on other modules. Each module can be implemented in various ways, as long as it respects it’s interfaces with other modules.
*   Versionning: If an interface is to be changed, the codebase’s version increases. It should be easy to visualize differences between two versions, and to revert back to a previous version, if a later version does not work as expected.
*   Readability: each file should be less than 200 lines of code. Otherwise, you can probably refactor/redesign your code.
*   Complexity: The more complex the code, the less people will be able to use / exploit it, and the less people will accept to maintain it. And thus, the more bugs will occur from this code.
*   Bug: unexpected behavior of a code base in a specific context/situation. Happens when rules to be implemented were not clear enough, of if the code incorrectly implement these rules.
*   Technical debt: when too many shortcuts and workarounds (a,k,a quick hacks) were made in the source code, the complexity of the code increases, thus its maintainability decreases very quickly. Some time must be planned ahead for regular refactoring, in order to clean and simplify the code.
*   Automated testing consists of a list of scenarios with an expected outcome (or behavior) that can be used to check that the source code behaves as expected, even after changes. If expected outcomes change, it means that rules have changed.
*   Test-driven development consists of writing tests (rules) first, and then writing the code that complies to these tests. It ensures that rules prevail, and that implementation can change safely over time.
*   Legacy code: code on which expected behaviors (i.e. rules) can not be tested automatically, and thus, has become too complex to understand and maintain. At some point, even refactoring can not be applied without the risk of breaking expected behaviors of the new implementation, because these expected behaviors (rules) were not defined in the first place.
*   Open-source collaboration: consists of sharing the source code freely with the world, so that anyone can read, copy, and propose contributions by creating an alternative version out of the original source code: a “fork”.
*   Pull request: If the changes proposed by a contributor in their alternative version (the “fork”) benefit to the users of the original source code, they can request to integrate them back into the original source code. So-called “Pull requests” can be refused or approved by the trusted maintainers of the original source code, after they typically check that this contribution complies to expected behaviors (rules, or “automated tests”).

*Note: This was written in the middle of the night as a draft, using my Android device. I published it as is, because I had no idea how to save it as a draft using Medium’s Android app. I’m sorry for the lack structure, references, and formatting. Please consider this as a work in progress. Nevertheless, I welcome your suggestions and comments that would help me elaborate further on these ideas. Thank you for your understanding! :-)*
