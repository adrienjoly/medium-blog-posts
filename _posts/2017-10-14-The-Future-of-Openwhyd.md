---
title: "The Future of Openwhyd \U0001F3B5"
date: '2017-10-14T16:17:46.202Z'
subtitle: "The vision for Openwhyd 2.0, work in progress, and how to\_help."
excerpt: 'The vision for Openwhyd 2.0, work in progress, and how to help.'
thumb_img_path: images/The-Future-of-Openwhyd/1*ShVCeS30asKUfFrDuPwBqA.jpeg
layout: post
---
![](/images/The-Future-of-Openwhyd/1*ShVCeS30asKUfFrDuPwBqA.jpeg)

> Note: This is a translation of “[L’avenir d’Openwhyd](https://medium.com/openwhyd/lavenir-d-openwhyd-818b0f34196c)” (🇫🇷)

As you may already know, [Openwhyd](https://openwhyd.org) is a free and independent platform that enables you to **create playlists** of songs from several music streaming sources (*e.g. Youtube, Soundcloud, Bandcamp, Deezer…*), to share them, and to discover **hidden gems** hand-picked by our community of music lovers.

[**Openwhyd — Discover and collect the best music tracks from the web**  
*The place for music lovers. Collect and share the tracks you love.*openwhyd.org](https://openwhyd.org/ "https://openwhyd.org/")[](https://openwhyd.org/)

I started developing this platform in 2012, when I was the lead developer of the Parisian start-up company **Whyd**. During summer of 2016, Whyd offered the platform to its community of users, in order to focus on the development of their new product. With their blessing, I took the responsibility of turning this Whyd’s ex-product into an **open-source project**, re-baptised “Openwhyd.”

Read more about this story in the article below:

[**Music, amongst other topics**  
*The story of Openwhyd*medium.com](https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d "https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d")[](https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d)

* * *

### Opportunities for improvement

Overall, [openwhyd.org](https://openwhyd.org) still works quite well. That being said, some users and contributors expressed their **frustration** on a few recurring topics. Examples:

*   Many are waiting for an Android app;
*   Several users reported that the iPhone app is broken;
*   The look and feel could be more modern, especially on the player that can be embedded on external websites;
*   “Openwhyd” is quite a weird and unattractive name for newcomers;
*   Music discovery is mostly done by manually exploring profiles;
*   It’s still hard for developers to help us improve Openwhyd and fix bugs;
*   Last but not least, it’s hard for developers to create alternative clients that connect to our API, while making sure that all existing features will be working.

Most of those issues are caused by the fact that our platform was developed in a very iterative — and rushed — way during its start-up years (2012–2014), leading to what we call **technical debt**. Also, it’s developed upon now-obsolete technologies and practices.

* * *

#### How to fix those issues, and improve Openwhyd ? 🤔

[As suggested by Serdar](https://github.com/openwhyd/openwhyd/issues/101), one of our contributors on Github, modernising Openwhyd is a wide and complex project. So we need to plan it in a thoughtful and well-coordinated manner:

*   First, by defining our **objectives** for Openwhyd’s next version;
*   Then, by **consolidating** the foundations of the current version *(e.g. bug fixing, documentation, automated tests)* **without adding features**, before transitioning to the next version.

Let’s propose a vision for the next version of Openwhyd!

* * *

![](/images/The-Future-of-Openwhyd/1*DJ_wHetrMNVts3mGNflWsA.png)

<figcaption>Design concept proposed by Claire&nbsp;Marion.</figcaption>

### My vision for Openwhyd 2.0

For **users**, it’s important that Openwhyd becomes more attractive, easy and fun to use. From various **mobile devices**: iPhones, Android phones, and tablets. Music discovery should be made easier thanks to editorial content (*e.g. blogs, interviews…*), the possibility to join **genre-centred groups**, and/or **personalised discovery** features. (e.g. based on machine learning.) Also, why not think of a new brand identity!

Our **partners** (*e.g. festivals, music venues, clubs and magazines that embed Openwhyd playlists onto their own website to publish their programme*) would benefit from a better design and customisation options for our **embedded player**. We also imagine that some of our partners could contribute to sustaining Openwhyd financially, e.g. by providing a more seamless integration into their websites.

![](/images/The-Future-of-Openwhyd/1*kQVsTXVyfNR2m4dJj8VdfQ.png)

<figcaption>Re-design of our embedded playlist player, proposed by Claire&nbsp;Marion.</figcaption>

Last but not least, we’ll need to **modernise our technical architecture**, to ease contributions from developers who want to join our effort:

*   Move towards a **modular** architecture in which the API is separated from our web application; (*jQuery-based front-end*)
*   A pure API server with **3rd-party authentication** (*e.g. OAuth*), so that any developer can build their own Openwhyd app and allow their users to access their account from those apps.
*   A progressive **re-design** of Openwhyd’s front-end, implemented using a modern component-based technology stack (*e.g. React or Vue.js*) and connecting to the new API server.
*   Finally, move from continuous integration (*i.e. automated tests are run to check the quality of all contributions*) to **continuous production**, so that any contributor can have their changes immediately visible on openwhyd.org, without requiring any validation from me.

![](/images/The-Future-of-Openwhyd/1*OsQBgFYFwf5HVUzJwASJTQ.png)

<figcaption>Proposed architecture for Openwhyd 2.0: apps connecting to a pure API&nbsp;server.</figcaption>

Isn’t that promising? 😎

* * *

### Work in progress, a 12-month recap

Since its transformation into an open-source project, Openwhyd’s technical infrastructure has improved. It’s now more mature, robust and accessible.

[**Openwhyd has become a mature project, releasing v1.0! 🎉**  
*Dear music lovers,*medium.com](https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75 "https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75")[](https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75)

Contributors (including myself) have given dozens of hours of their spare time to:

*   Write **automated tests** to make sure that Openwhyd’s features keep working as expected after each contribution to its source code;
*   Setup **continuous integration**, so that those tests are run automatically;
*   Remove deprecated modules to prevent **security holes**;
*   Fix **bugs** related to playback and detection of tracks from external streaming platforms (*e.g. Youtube*), and new sign-ups;
*   Improve the relevance and speed of **search results**, thanks to our partner: [Algolia](https://www.algolia.com/);
*   And **help young developers** along their first contribution to Openwhyd’s source code.

It’s been a pleasure for me to coordinate these efforts, and to get my hands dirty! I learned a lot thanks to our contributors and their wise suggestions. Thank you! 🙌

I know that some of these efforts did not turn into **visible benefits** for you, dear users… But rest assured that they are important steps towards sustaining and evolving Openwhyd for the longer term. They contribute to **reinforcing its foundations**, as explained above. So they bring us closer to version 2.0!

* * *

### How to support the development of Openwhyd 2.0?

There are various ways to help Openwhyd sustain and evolve, whatever your skills are!

For instance:

*   **Spread the word** about openwhyd.org, e.g. by sharing your playlists on social networks;
*   Save volunteers some time, by **replying to users** who share their problems (*e.g. misunderstandings, bugs…*) in the [Music Lovers’ Club](https://www.facebook.com/groups/openwhyd/), on Facebook;
*   Save developers some time, by **gathering detailed information** about bugs found by users, into [Github Issues](https://github.com/openwhyd/openwhyd/issues);
*   Or, if **you’re a developer** (*beginners are welcome too!*), come give us a hand after having read [our contribution FAQ](https://github.com/openwhyd/openwhyd/blob/master/docs/FAQ.md#id-love-to-contribute-to-openwhyd-how-can-i-help).

That being said, what Openwhyd needs most right now is funds, to pay for platform hosting costs. Openwhyd is not owned and managed by a company anymore. It’s maintained by a community of volunteers and **crowdfunded** thru its community of users.

Unlike Wikipedia, the donations we collect are solely used to **pay the bills** that are necessary to keep openwhyd.org online. Once again, volunteers are not paid to participate, and neither am I!

![](/images/The-Future-of-Openwhyd/1*X4WvbcfIaCivgU9FhmCUqg.jpeg)

<figcaption>Our Open Collective page, to collect donations: <a href="https://opencollective.com/openwhyd/" data-href="https://opencollective.com/openwhyd/" class="markup--anchor markup--figure-anchor" rel="nofollow noopener noopener noopener noopener" target="_blank">https://opencollective.com/openwhyd/</a></figcaption>

So, if you’re a regular user of Openwhyd, that you hope to be able to keep using it for the following years, and that you would like to see it evolved as proposed in this article, please [**donate now**](https://opencollective.com/openwhyd/order/313)! We’d appreciate it a lot!

There are **two ways** to donate:

*   If you want Openwhyd to sustain in the long term: [**become a backer**](https://opencollective.com/openwhyd/order/313). It consists of donating the amount of your choice every month, like a subscription. You can stop it anytime. (starting at $1/month)
*   Otherwise, you can give a [one-off donation](https://opencollective.com/openwhyd/donate). The amount is also up to you.

**Don’t wait** for others to do it before you. It would take 600 donations of $1 to cover one year of bills! Be part of this movement, or stay out. It’s up to you!

**International users**, your bank will automatically convert your currency into US Dollars, so don’t worry about that. [Ask Google](https://www.google.fr/search?q=1+usd+to+eur) for the current rate.

<figcaption>Let me recap everything in a video! (English subtitles are available)</figcaption>

If you have any **question or issue**, please let me know by email at contact@openwhyd.org, I’ll do my best to help you quickly!

### Thanks for your support! 💪

#### Never stop jamming! 🎵
