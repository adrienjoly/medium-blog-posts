---
title: "Don’t build a back-end for your Android music app \U0001F3A7"
date: '2018-04-17T13:01:35.769Z'
subtitle: "Why it’s not a good idea, and how Openwhyd may become your best\_partner."
excerpt: 'Why it’s not a good idea, and how Openwhyd may become your best partner.'
thumb_img_path: >-
  images/Don-t-build-a-back-end-for-your-Android-music-app/1*282DJ9v6f4dzSIz6DLof6A.png
layout: post
---
![](/images/Don-t-build-a-back-end-for-your-Android-music-app/1*282DJ9v6f4dzSIz6DLof6A.png)

👋 Hi!

My name is Adrien. I’m a music lover, a drummer, and a software engineer. I started developing **Whyd** —formerly a startup product to help music lovers keep, play and share their favorite music tracks scattered across free streaming platform — in 2012. Since [Whyd became Openwhyd](https://medium.com/openwhyd/handing-back-the-keys-to-users-the-openwhyd-music-curation-platform-case-3d26fa17a2f2) (in 2016), I have been helping this product sustain as a **collaborative, non-profit, crowdfunded and open-source project**.

![](/images/Don-t-build-a-back-end-for-your-Android-music-app/1*FcYf9XPsnCtWKpAjpIUQwQ.png)

<figcaption><a href="https://openwhyd.org/" data-href="https://openwhyd.org/" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Openwhyd</a> is a platform to help music lovers keep, play and share their favorite music tracks&nbsp;online</figcaption>

Today, I’m calling out to Android app developers who are (or will be) **developing a music app**, to propose them a mutually-beneficial partnership: provide openwhyd.org’s back-end infrastructure to store their users’ music library for free, and allow Openwhyd users to play their music on Android.

**Android developers**, let me explain why I think that your app needs a back-end, and why you should consider openwhyd.org as your app’s back-end.

* * *

### **Why your music app needs a good back-end**

1.  A mobile app to search and play music on the go is cool, but many users want to **keep their favorite songs** in playlists and play them back again later. You will need a backend in order to store these playlists of songs.
2.  Storing songs in **YouTube playlists** may seem to be an obvious choice for that, but many awesome songs are only available on other streaming platforms (e.g. SoundCloud, Bandcamp…) and it’s not possible to have non-YouTube songs in your YouTube playlist.
3.  Sometimes, it’s more convenient to access your music library **from a computer**. In order to do that, your users will also need to be able to access their music library from a web app.
4.  **Hosting** people’s data is not easy nor cheap: you need to find a stable and secure solution, to pay hosting fees, to backup regularly, to let users manage their account (i.e. sign up, login, forgotten passwords…). And now, GDPR makes it ever scarier to store personal data.
5.  At some point, several users will ask for an **API** to access their music library from other services. Providing and maintaining an API is a time-consuming distraction from developing a quality music app.
6.  When your app becomes both useful and qualitative, users will probably ask for broader ways to **discover new music**. You will either have to provide a music recommendation system (i.e. it’s very very hard to do a good one) or a way to discover the music of users with similar taste.

![](/images/Don-t-build-a-back-end-for-your-Android-music-app/1*vPEQA6ze7MZkVLhAzlrWmQ.png)

<figcaption>To help your users discover new music, having a rich community of users&nbsp;helps</figcaption>

* * *

### **Considering Openwhyd as your app’s back-end**

1.  Openwhyd’s back-end was made specifically **to maintain a music library**: it handles user account management for you, it comes with [an API](https://github.com/openwhyd/openwhyd/blob/master/docs/API.md), an [iPhone app](https://openwhyd.org/iphone) and two web apps ([openwhyd.org](https://openwhyd.org/) and [sound-nuggets.xyz](https://sound-nuggets.xyz)).
2.  It’s **open source and free to use**, for both you as an app developer, and for your users. (source code available at [github.com/openwhyd](https://github.com/openwhyd/openwhyd))
3.  It officially supports music tracks from **various streaming sources**, including YouTube, SoundCloud, Bandcamp, Vimeo, Dailymotion, and any audio stream (e.g. MP3 files hosted online) accessible thru a URL. It’s also extendable to other sources (at the condition that you [provide a plugin](https://github.com/adrienjoly/playemjs#playemjs)).
4.  Our service is not a fad, we’re **here to stay**: while many startups competing with us ended up closing down for financial reasons, Whyd/Openwhyd has been running free of charge for its users since 2012, and some users are still using it from the beginning!
5.  Tens of thousands of people have already been sharing their favorite songs on Openwhyd, and a good chunk of them are [desperately looking for an Android app](https://www.facebook.com/groups/openwhyd/search/?query=android) to play them on the go. By plugging your app to our back-end, you would automatically **gain thousands of enthusiastic users**!

![](/images/Don-t-build-a-back-end-for-your-Android-music-app/1*tBcVRqoj0gl58qgtBmaBBA.png)

<figcaption><a href="https://sound-nuggets.xyz" data-href="https://sound-nuggets.xyz" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Sound-nuggets</a>, an alternative web client plugged into Openwhyd’s back-end, developed by a long-time user</figcaption>

* * *

### **Can you trust Openwhyd?**

As the main author of the Openwhyd codebase since its inception, and owner of the openwhyd.org domain, I’m blessed to have earned the **respect and trust** of its initial founders (Gilles and Jie from Whyd), of a team of talented and kind [volunters](https://github.com/openwhyd/openwhyd#contributors), and of thousands of music lovers.

I’ve shown that I take this **responsibility** seriously:

*   I have worked hard to keep openwhyd.org **up and running** while keeping operational costs low (e.g. [by optimising our infra usage](https://github.com/openwhyd/openwhyd/issues/138)), and gathered friendly volunteers to help us sustain Openwhyd and it’s community of music lovers lively for years.
*   I’ve convinced some of our users to [donate](https://opencollective.com/openwhyd), and [sponsors](https://github.com/openwhyd/openwhyd#sponsors) to **cover our infrastructure costs** without impact on the values and privacy of our community.
*   Even though [I recently announced](https://medium.com/openwhyd/openwhyd-is-open-to-new-maintainers-94d55050adb4?source=collection_home---6------0----------------) that I was not going to contribute to the development of openwhyd’s web app any longer, **I still take the time** to coordinate and help contributors, to [talk with our community of users](https://www.facebook.com/groups/openwhyd), to fix critical bugs, to enforce the privacy of our users’ data (i.e. their login credentials and email address), to make weekly backups of openwhyd’s database, and to transparently share insights from its usage data.

![](/images/Don-t-build-a-back-end-for-your-Android-music-app/1*5vBeQlQyU2kyLPbrGn1o9g.jpeg)

<figcaption>At least once a year, I share some insights from Openwhyd’s usage&nbsp;data</figcaption>

* * *

### **No strings attached**

For as long as you **act respectfully** towards Openwhyd’s platform, codebase and community of users, using our backend comes with no strings attached: **you are free** to do whatever you want with your app, with its branding and with the openwhyd users who would sign in to their Openwhyd account thru your app.

Also, the content posted by users on Openwhyd’s backend (i.e. tracks with their optional description, playlists, comments…) is public and can be freely be [downloaded in JSON format](https://github.com/openwhyd/openwhyd/blob/master/docs/FAQ.md#how-to-export-my-tracks--comment-exporter-ma-musique-en-csv-ou-json-) at any time, so **you can easily migrate data** to another back-end solution if you ever want to do so.

* * *

### **What’s next?**

If you are developing (or going to develop) a music app for Android and may be interested in using openwhyd.org to store your users’ music, **let’s talk!**

👉 Please **leave a comment below** or [contact me directly by email](mailto:adrien@openwhyd.org).

Can’t wait to know more about your project and see how we can help! 💪

#### **Never stop jamming!**

*PS: I would like to thank* [*PaulLouis Nech*](https://medium.com/u/d52dafa0fa4e) *and Constance Betinyani for their contribution to this article.*
