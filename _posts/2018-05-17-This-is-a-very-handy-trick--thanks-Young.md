---
title: 'This is a very handy trick, thanks Young!'
date: '2018-05-17T13:21:57.945Z'
excerpt: 'In my project, I created a jest.config.js file that contains the following:'
layout: post
---
This is a very handy trick, thanks Young!

In my project, I created a jest.config.js file that contains the following:

jest.setMock(

‘@mycompany/some-package’, // initial package

require(‘@mycompany/mocks/some-package’) // mocked package

);
