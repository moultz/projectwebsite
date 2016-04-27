---
layout: page
title: Testing Strategies
---

## Automated Testing
Using a combination of WordPress' guide of [automated testing](https://make.wordpress.org/core/handbook/testing/automated-testing/) and WordPress [theme tests](http://codex.wordpress.org/Theme_Unit_Test) for automated testing of bugs.

## Cross Browser Testing

It's important to test the website in different websites to check for bugs or unexpected behavior.

For the new version of London Cancer we will be testing on Desktop:

* All Internet Explorer versions greater than 8
* Safari
* Chrome
* Firefox
* Microsoft Edge

And on Mobile:

* iOS Safari
* Android Chrome

However its quite difficult to test all these browsers manually. Fortunately there are tools that automate a bit of the process. Tools that we've looked at include [Browsershots.org](http://browsershots.org/http://46.101.80.67/) and the more premium [Sauce Labs](https://saucelabs.com/)


## Accessibility Testing

Creating a website that everyone can use should be the aim of the new website. However how do you test that the website is accessible?

You have to account for:

* Those who cannot see or use a mouse.
* Deaf users whose first language is sign language.
* Visitors whose primary language is not your language.
* People who use special assistive software or hardware to access the Web.
* People who are colour blind or can’t see low colour contrast.

Source: [WordPress Accessibility](http://codex.wordpress.org/Accessibility)

Using the [WAVE web accessibility tool](http://wave.webaim.org/) and checking off the W3C's Web Content Accessibility Guide (WCAG) which is found [here](http://www.w3.org/WAI/WCAG20/quickref/).


## Manual Performance Testing
[Google's Pagespeed Insights](https://developers.google.com/speed/pagespeed/insights/) and using a WordPress [plugin](https://wordpress.org/plugins/p3-profiler/) to determine plugin performance the site should be sufficient for determining how performant the website is.
