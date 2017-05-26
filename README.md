# bower-web-tool
Web sites are made of lots of things — frameworks, libraries, assets, and utilities. Bower manages all these things for we.
Bower is a package manager for the web. If you’re not sure what package managers are, you’re gonna learn what they are and how useful they can be.
Installing Bower
To install bower, you need to have node.js installed on your computer. To check whether you have it or not, open up your command line interface (CLI) and type

node -v

Keeping track of all these packages and making sure they are up to date (or set to the specific versions we need) is tricky. Bower to the rescue!
Bower can manage components that contain HTML, CSS, JavaScript, fonts or even image files. Bower doesn’t concatenate or minify code or do anything else - it just installs the right versions of the packages we need and their dependencies.

To get started, Bower works by fetching and installing packages from all over, taking care of hunting, finding, downloading, and saving the stuff we’re looking for. Bower keeps track of these packages in a manifest file, bower.json. How we use packages is up to we. Bower provides hooks to facilitate using packages in wer tools and workflows.
Bower is optimized for the front-end. If multiple packages depend on a package - jQuery for example - Bower will download jQuery just once. This is known as a flat dependency graph and it helps reduce page load.

In this repository we will explore Bower to enable us to automatically fetch Bootstrap and Font Awesome files. Then we will make use of the files fetched by Bower in our web page. At the end of this repository we will be able to:
Use Bower to fetch web packages and assets from global repositories automatically
Use the Bower components in wer web page

Installing Bower

Install Bower as a global node module. To do this, type the following at the command prompt:

     npm install -g bower


Note: Precede this command with sudo on Mac or Linux
Creating bower.json File
Create and initialize a bower.json file by typing the following at the command prompt:


     bower init


Bower will ask several questions which we should answer as follows:
Name: Project (the default)
version: 1.0.0
description: Website for an awesome restaurant
main file: index.html
what type of modules does this package expose? (leave all unselected, just hit enter)
keywords: Project, Fusion Restaurant
author: (Your own name)
license: (MIT)
Say yes to the remaining questions except the last one.
Looks Good? Y
Have a look at the contents of the bower.json file that was created.
Installing Bower Components
We will first install Bootstrap using Bower. To do this type the following at the command prompt:


     bower install bootstrap -S


This will install Bootstrap to our project, and since Bootstrap depends on jQuery, it will automatically install jQuery. The "-S" flag indicates that Bootstrap should be saved as a dependency for our our project in the bower.json file.
Next, to install Font Awesome, we need to type the following at the command prompt:


     bower install font-awesome -S


Examining Bower Components
In the Project folder, we will find a bower_components folder that Bower created. The components that Bower fetched for we are stored in this folder. Browse the folder and the sub-folders therein to see the contents.
Back in the Project folder, examine the contents of the bower.json file to see that Bower has added in new information about dependencies. This specifies that the current project is dependent on Bootstrap and Font Awesome.
Using Bower Components

To make use of the Bower components, we will update the CSS and JS links in our web pages to use the files in the Bower components folder. Update the CSS links in the index.html, aboutus.html and contacts.html page as follows:


    <link href="bower_components/bootstrap/dist/css/bootstrap.min.css" rel
      ="stylesheet">
    <link href="bower_components/bootstrap/dist/css/bootstrap-theme.min.css" rel
      ="stylesheet">
    <link href="bower_components/font-awesome/css/font-awesome.min.css" rel
      ="stylesheet">

Similarly, update the JS links in the files as follows:

    <script src="bower_components/jquery/dist/jquery.min.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as 
      needed -->
    <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>


The project now makes use of the files fetched by Bower in the web pages.
Conclusions
In this project we learnt about Bower and how we can make use of Bower to fetch the web components. Thereafter we learnt how to make use of the web components in our project.
