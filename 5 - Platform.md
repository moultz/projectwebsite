---
layout: page
title: Platform
---


- [Hardware](#hardware)
- [Operating System](#operating-system)
- [Tools](#tools)
- [Libraries](#libraries)
- [Services](#services)


<!-- Define your platform - that is the hardware, operating system, libraries and tools on which your PoC design will run.

You should aim for a minimal, clean platform to limit dependencies, complexity and cost. -->

London Cancer's development environment and workflow is a low cost, easy to understand platform that uses tried and tested tools, libraries and 3rd Party services to abstract away complexity. At the same time, the toolchain and development environments are designed to employ best practices and write code that will go from local to staging to production.

This was important as the website will be handed over to developers to maintain the website and possibly develop the website further.

A key principle was that the website should be able to be developed locally using version control and to be tested on a staging environment that was similar to the production environment. We used this principle when we reviewed our options for hardware, operating system, libraries and tools.

We didn't need to review our choice of programming languages since WordPress was specified it uses PHP and MySQL meaning we have to develop using those languages. On top of the website's front end is developed in using web technologies including HTML, CSS and JavaScript.

## <a name="hardware"></a>Hardware

While we have no actual hardware device, we recommend the server on which the website runs has at least 1GB of RAM and a Solid State Disk.

However this would preferably be done by using a 3rd Party Provider, for our staging server we used Digital Ocean which we cover below.

## <a name="operating-system"></a>Operating System

Due to the website running WordPress as a requirement which requires PHP and MySQL, Linux made the most sense due to the common server stack of Linux, Apache, MySQL and PHP (LAMP). Using Linux rather than Microsoft or OS X due to its free licensing is also a bonus.

The Ubuntu distro (Linux distribution) version 14.04 was chosen due to it having Long-Term Support (LTS) by Ubuntu's developers. Using the 14.04 LTS release means that bugs, security issues and compatibility issues are fixed until 2019.

![Ubuntu LTS support diagram](/assets/ubuntu-lts.png)
Source: [LTS | Ubuntu Wiki](https://wiki.ubuntu.com/LTS)

This was a tradeoff over Debian which is what the current website's server runs on, however the the tipping point was that Serverpilot (a 3rd-party service described later) requires Ubuntu.

## <a name="tools"></a>Tools
<!-- Git, Atom, MAMP, WP-CLI, Wordmove -->

###  <a name="git"></a>Git
We use Git for version control of the code developed locally. We develop on a development branch and then push to master once it passes staging tests.

Alternative version control systems were SVN and Mecurial, however due to the simplicity of Github and our previous experience using it, Git was preferable.

### <a name="atom"></a>Atom
We use Atom as a text editor to write all the code. Atom has a set of installable 3rd party packages that help us keep our code clean and readable including [Atom Linter](https://github.com/atom-community/linter) and [Atom Beautify](https://atom.io/packages/atom-beautify).

The Linter **automatically** runs to ensure that we write correct code.

Atom was chosen over other text editors such as Sublime, Vim, Emacs, Textmate due to its ease of use and out of the box features.

### <a name="mamp"></a>MAMP
MAMP is an acronym for (Mac, Apache, MySQL, PHP) provides a one-click installation process for setting up a local development environment. This enables local development of WordPress with the ability to also make SQL queries and execute PHP code through phpMyAdmin. It has a Graphical User Interface (GUI) which also makes it easy to install and use.

Through using MAMP, we can **automatically** setup and run an Apache web server and MySQL database.

MAMP is an extremely popular solution due to it being free, easy to install and use on both OS X and Windows. Alternatives we looked at included Desktop Server Pro (paid), setting up our own development environment using the command-line (inefficient use of time), and AMPPS which had a less user friendly GUI and had functionality that we didn't need.


![Screenshot of MAMP running](/assets/mamp.png)
Above: A screenshot of the MAMP GUI showing that Apache and MySQL are running in the background.

### <a name="WP-CLI"></a> WP CLI
"WP-CLI is a set of command-line tools for managing WordPress installations. You can update plugins, set up multisite installs and much more, without using a web browser." Source: [WP-CLI.org](http://wp-cli.org/).

WP-CLI is not a necessary part of our development environment however is helpful quickly and efficiently all within the command-line rather than having to use the WordPress backend. We recommend it to developers that are comfortable with both WordPress and the CLI.

![Screenshot of WP-CLI documentation](/assets/wp-cli.png)
Above: A screenshot of WP-CLI's commands and what they do.

### <a name="wordmove"></a> Wordmove
We use Wordmove to deploy from our local environment to our staging environment.

At the same time as being used as a deployment tool, it also allows us to pull any changes we make on the staging server back down to local.

Wordmove's benefit comes from not only **automatically** deploying the WordPress files but also the MySQL database too. This means that we don't have to manually dump the local database and upload it to the staging server.

An alternative to [Wordmove](https://github.com/welaika/wordmove) would be purchasing [Desktop Server Pro](https://serverpress.com/get-desktopserver/) for $99.95 to gain the benefit of the "Direct Deploy WordPress to Live Server" feature. However due to the cost we decided to stick with Wordmove assuming that any developer that is in charge of maintaining the website is familiar with the command-line.

![Wordmove Screenshot](/assets/wordmove.png)
Above: An overview of Wordmove's command-line's functionality


## <a name="libraries"></a>Libraries
<!-- Bootstrap -->

### <a name="bootstrap"></a>Bootstrap
We use [Bootstrap](http://getbootstrap.com) version 3.3 as a front-end framework to quickly develop a WordPress theme while also using it for its Internet Explorer 8 compatibility and its responsive web design capabilities.

The tradeoffs for Bootstrap are written in the Research section.

### <a name="jquery"></a>jQuery

Bootstrap's JavaScript components have [jQuery](https://jquery.com/) as a dependency. jQuery is a JavaScript library that simplifies writing JavaScript code for browser interactivity.

Due to requiring jQuery for running Bootstrap, there wasn't really an alternative choice.

## <a name="services"></a>Services

### <a name="digitalocean"></a>Digital Ocean
We use [Digital Ocean's](http://digitalocean.com) hosting infastructure to **automatically** setup a Virtual Private Server (VPS) for our staging server to run Ubuntu 14.04 which we identified as an ideal operating system (OS) for our staging server to run on.

Digital Ocean was chosen due to its low cost ($5/month), easy to use control panel, simple server setup/provisioning, great underlying hardware, and compatibility with Server Pilot (covered next).

While looking at alternatives we only considered options that were compatible with Server Pilot which included Linode, Amazon Web Services and Rackspace Cloud Hosting.

Linode and Rackspace both had the ease of use but not the cost effective benefit with Digital Ocean being about half the price.

Amazon Web Services had too much complexity and was not necessary for a staging server.

### <a name="serverpilot"></a>Serverpilot
[Serverpilot](http://serverpilot.io) is free secure control panel that:

* **Automatically** installs Apache, NGINX, PHP and MySQL, and keeps those packages updated automatically
* Configures a firewall to secure the server
* Provides a simple control panel to manage databases
* Optimised for PHP websites, especially WordPress

These benefits mean that neither we, nor whoever we hand the servers over to for maintenance need to worry about system administration. We recommend to use this setup for production due to its ease of use and speed. We recommend looking at Serverpilot's [feature overview](https://serverpilot.io/features-overview.html) for additional reasons to use Serverpilot.

Alternatives to Serverpilot's control panel included using either cPanel or Plesk, which have expensive licenses.

Alternatives to Serverpilot's configuration and optimisation meant trying to manually configure, install, and automatically update the server by writing scripts which would be too complex and take up too much time.

## How they all connect

![Our toolchain diagram](/assets/toolchain.png)


To setup:

1. Local development environment: Install MAMP for Mac or XAMPP for Windows
2. Optionally install WP-CLI locally and/or on staging.
3. Install sshpass, an open-source Wordmove dependency
4. Setup a Wordmove file and enter your local development information and our staging server information.
5. Use Wordmove to pull from the old staging server
6. New staging server: Provision a Ubuntu 14.04 VPS on Digital Ocean and set it up with Serverpilot. Setup a database on Serverpilot using the control panel.
7. Create a new Wordmove file with the new database information that you used on Serverpilot.
8. Use Wordmove push to push the local site to your new staging server.
9. Edit the wp-config.php file to use your staging server's database name, database username and database password.
9. Setup a new git repository to track changes if you use it for development.

Although this setup is not automated fully, once completed, the staging server's updates will be automated as well as deployment.

Improvements would be to automise the dependency installs, and when handed over to a new maintainer, rather than pulling from the old staging server using Wordmove, cloning a Github repository and importing a MySQL dump of the database.

A potential alternative to this would be to use Vagrant or Docker.

Furthermore the toolchain does not include any testing frameworks so far, however we seek in to include them in our toolchain next term. You can find out more in the Testing Strategies section.
