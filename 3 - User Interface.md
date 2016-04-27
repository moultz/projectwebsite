---
layout: page
title: User Interface
---
## Design Principles

Before we take our use cases and apply them to create a set of wireframes/designs, it's important to have a set of principles.

The website should represent 6 design values from Don Norman's book The Design of Everyday Things:

<ol>
  <li><strong>Visibility</strong> - The key functionality should always be obviously visible to the user</li>
  <li><strong>Feedback</strong> - The website's functionality and navigating should provide feedback via interaction in a timely way.
  </li>
  <li><strong>Affordance</strong> - The website should use UI components such as buttons, and navigation bars that are familiar to users. The website's design should feel easy to navigate and use.</li>
  <li><strong>Mapping</strong> – The website's navigation should have clear mappings between the navigation bar and the current page displayed.</li>
  <li><strong>Consistency</strong> – The website should have a consistent visual style using London Cancer's style guide.</li>
  <li><strong>Constraints</strong> – Remove choice where possible, keep things simple. </li>
</ol>


## Design Sketches & Wireframes
<!-- from using the use cases -->

<p class="message">
  Following on from the Use Cases we can now start to define what the user interface of the website will look like. Note that a full redesign was not a requirement.
</p>

While much of the interface in terms of layout will look and seem similar, its important to understand how the interface optimises to different device screens.

Below is some screenshots of the current website with wireframes created to take the best of the current design and apply it with Responsive Web Design.

Firstly we'll look at the Home Page and then a generic Content Page.

### Homepage Desktop:

 The current modular homepage with different widgets currently looks like this:

![London Cancer current](/assets/londoncancerhome.png)

The wireframe will look similar to the actual design on a desktop device:

![London Cancer homepage wireframe on Desktop](/assets/wireframe-londoncancerhome.png)

However, since the current website lacks Responsive Web Design, it is necessary to design wireframes to provide insight on how the website will look on tablet and mobile devices.

### Homepage Tablet:

Maintains the same design, however reduces whitespace.

![London Cancer homepage wireframe on Tablet](/assets/wireframe-londoncancerhome-tablet.png)

### Homepage Mobile:

Mobile, notice how the widgets snap to one per row and the navigation bar is hidden:

![London Cancer homepage wireframe on Mobile hiding menu](/assets/wireframe-londoncancerhome-mobile.png)

However when the 'Hamburger' menu icon is selected the navigation pages are revealed:

![London Cancer homepage wireframe on Mobile showing menu](/assets/wireframe-londoncancerhome-mobile-showingmenu.png)

<hr>

### Content Page Desktop

Currently the layout of most of the Content Pages employs a three column layout, here is a screenshot of the [About](http://londoncancer.org/about/) page:

![London Cancer about page screenshot](/assets/londoncancerabout.png)

Here are the key changes we're making to the content pages:

* Remove the banner
* Remove the right sidebar
* Have the left sidebar show hierarchy of pages (Home Page > Section Page > Subsection Page) and show which one is currently active/displayed.
* Increase the font sizes to make the text easier to ready

Rather than using wireframes as we did for the homepage, we used sketches to quickly create easily understandable layouts for the content pages.

Below is a print out of the current London Cancer's website [About](http://londoncancer.org/about) page with our markings on what will be removed and changed:

![Modifying the about page](/assets/sketch1.jpeg)

We then sketch what the page would look like after the changes on Desktop:

![Sketch2](/assets/sketch2.jpeg)

## User Interface Requirements
<!-- The UI specification can be seen as an extension of the design draft that provides a complete description that contains all details, exceptions, error cases, notifications, and so forth. -->
The homepage should have:

* A clear navigation system
* A call to action of explaining what London Cancer is

It should also have six widgets that can be moved around and edited:

* Pathway boards
* Directory of services
* Patients, carers and public section
* GP referral forms
* News
* Events

The content pages should have clear typography and easy to understand navigation/page hierarchy.

## Style Guide

### Logo

![Logo](/assets/logo_main.png)

The logo should not be used in a width of less than 30mm. The logo should not be cropped, changed colour, changed perspective or changed orientation.

### Colour Palette

<table>
  <tr>
    <td class="magenta" style="  background-color: #e6186c;">Magenta #e6186c</td>
    <td class="purple" style="color: #fff; background-color: #6f2977;">Purple #6f2977</td>
    <td class="light-blue" style="color: #fff; background-color: #0086d4;">Light Blue #0086d4</td>
  </tr>
</table>
