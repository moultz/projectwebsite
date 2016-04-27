---
layout: page
title: Research
---

<!-- Carry out research into the ideas and concepts relevant to your system, using all available resources (e.g., online services, Science Library services, books, research papers, client expertise). -->

<!-- Your research, what you investigated, why it is relevant, what you did to discover. Results of the research done. What were your sources, what did you find out, what conclusions or decisions did you reach?  -->

<p class="message">
  This section includes research into how to solve the problems included in the Background & Context section, as well as researching how best to implement the Requirements & Use Cases.
</p>

## 1. Website Responsiveness

>Challenge: **The website is not responsive, which means that it is not optimised to be used with mobile devices such as tablets and mobile phones.** At the same time, finding a framework that supports browsers back to Internet Explorer 8 is still necessary.

>Solution: **Use a popular open-source front-end development framework while also being well documented and used for any developer to pick up and use.** We chose Bootstrap version 3.4 due to its ability to support older browsers such as Internet Explorer 8.

### What We Researched
To get to the solution of choosing Bootstrap, understanding what it meant for a website to be "responsive", why it's important and how to easily implement this feature into a browser.

### Why This is Relevant
This research was relevant because having the website responsive and compatible back to Internet Explorer 8 is one of the key deliverables of this project, not to mention it being part of our problem statement.

### What We discovered/Results/Decisions

![Responsive Internet Trends Chart](/assets/responsive.png)

The above graph is from the famous Internet Trends made by Kleiner Perkins Caufield Byers which shows how time spent on Mobile (green) has overtaken Desktop/Laptop in 2014 and 2015.

Website's were originally developed for desktop screens but with the prevalence of mobile and tablet computing, it is now important to design the website in such a way that is optimal for viewing, navigating and interacting with the website's content.

The way that websites achieve this is by using a technique called Responsive Web Design, which uses web browser technologies such as HTMl, CSS and JavaScript and a set of principles:

* Fluid, Proportion-based grids, so that rather than sizing website page elements in pixels they are sized in percentages.

* Images are able to be sized relatively, to ensure that they do not display outside their containing element.

* Media queries allow the page to use different Cascading Style Sheet (CSS) selectors based on the screen size of site visitor.

We found out this and more about Responsive Web Design (RWD) from the following sources:

* [http://www.w3.org/TR/css3-mediaqueries/](The W3 Specification for CSS3 Mediaqueries)
* [http://alistapart.com/article/responsive-web-design](Responsive Web Design by Ethan Marcotte from 2010, considered the original informative piece on Responsive Web Design)

Below is a video that succinctly explains Responsive Website Design from Treehouse, a provider of informative technology tutorial videos:

<iframe width="560" height="315" src="https://www.youtube.com/embed/iSY38POjLYc" frameborder="0" allowfullscreen></iframe>


Now that it's understood what are the key components of Responsive Website Design, it was important to understand how to best implement them.

While we could as a team have done further research and written our own styling sheets and JavaScript files this would have been extremely inefficient due to the big open-source community that creates libraries and frameworks to enable web developers to write websites in a responsive way.

We therefore researched and discovered the following templates/frameworks that were popular, maintained and well documented:

* [HTML5 Boilerplate](https://html5boilerplate.com/) calls itself a  *"professional front-end template for building fast, robust, and adaptable web apps or sites"*. With almost 32,000 Stars on its [Github Respository](https://github.com/h5bp/html5-boilerplate) we found it to be a really great starting point that followed some of the Responsive Web Design rules, however it's CSS files did not contain the media queries that we could have to handle different device sizes, neither did it have a grid.

* [Skeleton](http://getskeleton.com) describes itself as a *"dead simple, responsive boilerplate"*. It has over 10,000 stars on [Github](https://github.com/h5bp/html5-boilerplate) and includes a grid and media queries for different device sizes. Skeleton would have made an excellent choice however it does not support Internet Explorer 8, something that is covered in the Browser Compatibility research section.

* [Foundation](http://foundation.zurb.com/sites.html) is a *"responsive front-end framework in the world. Quickly create prototypes and production code for sites that work on any kind of device."* Despite having its user friendly set of components and JavaScript plugins, Foundation shares the same issue of browser compatibility that Skeleton has with the current supported version of Foundation not supporting Internet Explorer 8. Foundation has over 21,000 stars on its [Github](https://github.com/zurb/foundation-sites) repository.

* [Bootstrap](http://getbootstrap.com) is *"The most popular HTML, CSS, and JavaScript framework for developing responsive, mobile first projects on the web."* The [Github](https://github.com/twbs/bootstrap) repository has almost 90,000 stars. We chose Bootstrap due to its popularity, community, documentation, responsive grid system, and Internet Explorer 8 compatibility which is covered in the next section.

**Decision:** Use Bootstrap to enable the website to be used on multiple devices by it enabling Responsive Web Design. Implementing Bootstrap is covered in our Platform section.

**Sidenote:** An additional benefit we found during our research is that not having a mobile friendly website now affects Google’s search engine rankings for mobile searchers effective from April 2015. From this is it clear that having a responsive website has tangible benefits for both the website user and London Cancer. Source: [Rolling out the mobile-friendly update | Google Webmaster Cental Blog](http://googlewebmastercentral.blogspot.co.uk/2015/04/rolling-out-mobile-friendly-update.html)

We can use Google's [Mobile-Friendly Testing Tool](https://www.google.com/webmasters/tools/mobile-friendly) to ensure that the website we develop is mobile friendly.

## 2. Browser compatibility

>Challenge: The website is not responsive, which means that it is not optimised to be used with mobile devices such as tablets and mobile phones. **At the same time, finding a framework that supports browsers back to Internet Explorer 8 is still necessary.**

>Solution: Use a popular open-source front-end development framework while also being well documented and used for any developer to pick up and use. **We chose Bootstrap version 3.4 due to its ability to support older browsers such as Internet Explorer 8.**

### What we researched

After selecting to use Bootstrap 3 due to its easy implementation of Responsive Web Design, we needed to ensure that the end website we created was compatible with Internet Explorer 8.

### Why This Is Relevant

Having the website being compatible with Internet Explorer 8 was part of our requirements set by the client.

While Bootstrap 3 is compatible with Internet Explorer 8, not all the code of the website will be Bootstrap code as we intend to write additional code and stylings on top of Bootstrap's framework.

This made it important to understand the nuances of cross-browser compatibility.

### What We Discovered/Results/Decisions

Bootstrap's benefit of the easy implementation of Responsive Web Design is coupled with its cross-browser compatibility of browsers dating back to Internet Explorer 8.

![Browser Compatibility Table ](/assets/browsercompatibility.png)
Source: [Bootstrap Docs](http://getbootstrap.com/getting-started/#support-browsers)

Internet Explorer 8 does not support the features of:

* Styling HTML5 elements
* CSS Media Queries.

These are two key features, especially CSS Media Queries, without which, our website would not be responsive! Bootstrap uses 'workaround' JavaScript files which are loaded if a web browser is of a version less then 8.

The two workaround JavaScript files that Bootstrap 3 uses are:

* [HTML5Shiv](https://github.com/afarkas/html5shiv)
> "HTML5Shiv enables use of HTML5 sectioning elements in legacy Internet Explorer and provides basic HTML5 styling for Internet Explorer 6-9, Safari 4.x (and iPhone 3.x), and Firefox 3.x."

* [Respond.js](https://github.com/scottjehl/Respond)
> "A fast & lightweight polyfill for min/max-width CSS3 Media Queries (for IE 6-8, and more)."

With the use of these two files, the functionality of Bootstrap that is intended for modern browsers, can be supported by older browsers.

A tool that we found really useful during our research was the website [Can I Use](http://caniuse.com/). Can I Use allowed us to compare web technology features across browsers, and highlights CSS and JavaScript features that we shouldn't while supporting Internet Explorer 8. For instance we can compare the browser features that [Internet 7, 8 and 9 support](http://caniuse.com/#compare=ie+7,ie+8,ie+9).

## 3. Umbraco & WordPress

>**Challenge:** The current website uses a highly niche CMS (Content Management System) called Umbraco which is made using technologies that few developers possess the skill set of. For this reason, the current website is difficult to redevelop.
<br>
**Solution:** Change from using the Umbraco CMS to WordPress, a highly popular WordPress CMS.

### What We Researched

* What is a CMS
* What is Umbraco and its underlying technologies and popularity
* What is WordPress and its underlying technologies and popularity
* Is it possible to migrate the content from an Umbraco installation to a WordPress installation

### Why This Is Relevant

Understanding how the existing website works and all of its features would be helpful when redeveloping the website. In addition, having a high understanding of the Content Management System is imperative to the success of the project.

### What We Discovered/Results/Decisions

[Umbraco](http://umbraco.com/) is a fully-featured open source ASP.NET (a Microsoft technology) content management system. The website of London Cancer is currently uses Umbraco. Most of the code of londoncancer.org is written by CSHTML and contents are mostly written in XSLT.

[WordPress](http://wordpress.org) was selected by our client as the Content Management System to be used during the redevelopment of the website. This is due to the need to update frequently the website when adding, new, events and other content. Furthermore, WordPress is a far more popular Content Management System with more resources for developers and is consistently updated.

![Image of WordPress and Umbraco Usage](/assets/wordpressumbraco.png)
Source: [W3Techs.com](http://w3techs.com)

## 4. PHP & MySQL

>**Challenge:** Building a new website requires a lot of new functions and needs to assess MySQL Database with PHP.
<br>
**Solution:** Learn PHP and MySQL!

### What We Researched

* Basic PHP syntax
* PHP functions and object
* PHP arrays
* Querying a MySQL database with PHP

### Why This Is Relevant
Using PHP to write functions in a new website is a preferable way and it would be helpful to understand PHP to develop a new webpage. In addition, having a good understanding of PHP will allow us to develop a high quality website while connecting PHP with MySQL Database can create logins for users of London Cancer.

### What We Discovered/Results/Decisions
From the book: [Learning PHP, MySQL & JavaScript: With jQuery, CSS & HTML5](http://www.amazon.co.uk/Learning-PHP-MySQL-JavaScript-Javascript/dp/1491918667) we discovered every essential element of PHP, such as Basic PHP syntax, PHP functions and object, PHP arrays, Querying a MySQL database with PHP. Also, we discovered the importance of javascript and HTML5 for a high quality website.

## 5. Accessibility

>**Challenge** Since LondonCancer is a website designed for cancer patients, professional and GPs. Some patients may have difficulties when browsing our website.
>**Solution:** Use best practices of accessibility when building the site

### What We Researched

* What is accessibility?
* Why Web Accessibility is Important
* Making the Web Accessible

### Why This Is Relevant

Having an accessible website for London cancer can help more disabled and having difficulties on browsing website to understand what services london cancer is providing and also understand treatment, prevention of cancers and also refer them to a GPs in order to receive appropriate treatments.

### What we Discovered/Results/Decisions

It is essential that the website is accessible in order to provide equal access and equal opportunity to people with disabilities. Web accessibility means that people with disabilities can perceive, understand, navigate, and interact with the Web, and that they can contribute to the Web. Web accessibility also benefits others, including older people with changing abilities due to aging.

A guideline to make an accessible website is provided by [BBC](http://www.bbc.co.uk/accessibility/best_practice/what_is.shtml). For people who can’t see well, text size and colour should be adjustable and text-to-speech feature should be available for some important text.
For people can’t hear well, subtitle should be available for every video and audio, for some important content, British Sign Language should be available.
