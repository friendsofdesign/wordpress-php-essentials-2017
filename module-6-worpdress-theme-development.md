# MODULE 6 – Worpdress Theme Development

01. Introduction

02. Preparing Static Files

03. Setting up the Theme Hierarchy and Templates

04. Splitting Up Markup into Respective Files

05. Exercises

### 01. INTRODUCTION

Building a Wordpress theme can be a tough challenge. Theres many things to consider, and the rabbit hole can go very very deep. Just about any kind of system is possible with Wordpress from ticketing systems, to learning management, portfolio sites and job placement portals. As long as you know how to program and tap into the Wordpress API, you can do just about anything!

I will take you through a simple setup of a Wordpress theme from a static Bootstrap Responsive site. We will need to focus on a few areas to make it dynamic.

All Wordpress themes start off as static HTML/CSS & Javascript sites like you are used to creating. However, these sites need to make the shift from static to dynamic. As you know, PHP is the language of choice here. You will need to keep the Wordpress Codex open for this tutorial. You can find it at:

{% embed data="{\"url\":\"http://codex.wordpress.org\",\"type\":\"link\",\"title\":\"Main Page « WordPress Codex\",\"icon\":{\"type\":\"icon\",\"url\":\"https://s.w.org/favicon.ico?2\",\"aspectRatio\":0}}" %}

### 02. PREPARING A STATIC FILES

First off, we need to get a really simple HTML/CSS Template going. For the purpose of efficiency and practicality, I’ve put together a quick prototype of a responsive site with Bootstrap to get us started.

Open up the folder “Bootstrap to Wordpress”. I have included a very simple responsive template, which we will convert into a wordpress theme. We can identify the following places in the theme:

**Header -** which includes the navigation and banner

**Body -** which includes the blogposts

**Sidebar -** which includes the sidebar

**Footer -** which includes the copyright

This will be enough for us to gain a nice understanding of the wordpress codex and the PHP functions we need to use. Make sure you make a backup of this Bootstrap site on your computer incase you break something and you can’t go back.

Generally, you’ll always want to keep this quite a simple process. As we’re only doing one page, we aren’t going to have too much of a rough time, but if you had multiple pages and lots of layouts, this process would requite a lot of planning. First off, we need to get a really simple HTML/CSS Template going. For the purpose of efficiency and practicality, I’ve put together a quick prototype of a responsive site with Bootstrap to get us started.Open up the folder “Bootstrap to Wordpress”. I have included a very simple responsive template, which we will convert into a wordpress theme. We can identify the following places in the theme:

### 03. SETTING UP THEME FILE HIERARCHY

To begin, create the following files in a folder called “Bootstrap Theme”:

* header.php
* index.php
* footer.php
* sidebar.php
* style.css \(just copy your original one\)

Go grab your index.html file that we created in the last section and copy and paste all the code into the index.php file.

Make sure you have a working version of Wordpress installed in a directory with the htdocs folder in MAMP. Drag your theme folder into the wp-content &gt; themes folder.

According to the Wordpress Codex, your theme is not classified as a theme unless

Wordpress can find 2 files:

* index.php
* style.css

We need to add some comments into the style.css to get Wordpress to pick up the meta data - I know its weird to include CSS Comments as meta-data, but just bare with me.

Paste the following at the top of your style.css \(IT MUST BE CALLED style.css\):

```css
/*
Theme Name: Bootstrap Theme
Theme URI: http://friendsofdesign.net/bootstraptheme
Author: Daine Mawer
Author URI: http://dainemawer.com/
Description: An easy base theme built with Twitter Bootstrap
Version: 1.0
Tags: bootstrap, clean, minimal, style, 1140px
*/
```

Your theme folder should look like:

bootstraptheme /

    - index.php

    - header.php

    - footer.php

    - sidebar.php

    - style.css

You should have pasted your entire index.html into your index.php and copied all your styles into a style.css with the addition of your commented section above. You might also want to add an image file for your theme which will appear under the themes section. You MUST name this file “screenshot.png” and make the file the following dimensions: 300px X 255px

Place this along with your files in the root of your “bootstrap theme” folder. Great, place this whole folder in the wp-content &gt; themes folder and check Appearance &gt; Themes in your Wordpress Dashboard.

Okay great. On activating you will see your theme present with your screenshot, and the details coming through that we included in the style.css 

If you view the front of your theme, you might be confronted with a bit of shock. The HTML is present because we’ve included all the markup in the index.php 

We know our style.css is working because its picking up the metadata, what we still need to include is the css, fonts, img, and js folders that we left behind. Lets add those to the root of our theme folder now.

Remember to delete the style.css in your css folder incase it conflicts with the style.css that Wordpress is using. Refresh your browser. Not much of a difference. Check Chrome developer tools - Errors Galore! None of our stylesheets are linked appropriately and neither are our scripts or images. Problem!

### 04. SPLITTING UP MARKUP INTO RESPECTIVE FILES

We need Wordpress to stitch all of our files dynamically, the header, index, footer and sidebar all need to put pulled together when we request the front-end of our site. This concept can take a little bit of time to understand, so just follow through the steps below:

Cut the following out of your index.php into your header.php:

ut the following out of your index.php into your header.php:



```text
<!DOCTYPE html>
<html lang=”en”>
    <head>
        <meta charset=”utf-8”>
        <meta http-equiv=”X-UA-Compatible” content=”IE=edge”>
        <meta name=”viewport” content=”width=device-width,initial-scale=1”>
        <title>Bootstrap 101 Template</title>
        <!-- Bootstrap -->
        <link href=”css/bootstrap.min.css” rel=”stylesheet”>
        <link href=”css/style.css” rel=”stylesheet”>
        <!-- HTML5 Shim and Respond.js IE8 support of HTML5
        elements and media queries -->
        <!-- WARNING: Respond.js doesn’t work if you view the page via file:// -->
        <!--[if lt IE 9]>
        <script src=”https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js”></script>
        <script src=”https://oss.maxcdn.com/respond/1.4.2/respond.min.js”></script>
        <![endif]-->
    </head>
<body>
    <nav class=”navbar navbar-default” role=”navigation”>
        <div class=”container”>
            <!-- Brand and toggle get grouped for better mobile display -->
            <div class=”navbar-header”>
                <button type=”button” class=”navbar-toggle collapsed” data-                                toggle=”collapse” data-target=”#bs-example-navbarcollapse-1”>
                    <span class=”sr-only”>Toggle navigation</span>
                    <span class=”icon-bar”></span>
                    <span class=”icon-bar”></span>
                    <span class=”icon-bar”></span>
                </button>
                <a class=”navbar-brand” href=”#”>Wordpress</a>
            </div>
            <!-- Collect the nav links, forms, and other content for toggling -->
            <div class=”collapse navbar-collapse” id=”bs-examplenavbar-collapse-1”>
            <ul class=”nav navbar-nav navbar-right”>
                <li><a href=”#”>Home</a></li>
                <li><a href=”#”>About</a></li>
                <li><a href=”#”>Blog</a></li>
            </ul>
            </div><!-- /.navbar-collapse -->
        </div><!-- /.container-fluid -->
    </nav>

    <div class=”container”>
        Then, cut the following from your index.php and add it to your footer.php:
    </div>
    <div class=”row”>
        <div class=”col-md-12”>
            <p class=”text-center”>&copy; Copyright 2014. All Rights Reserved. Wordpress</p>
        </div>
    </div>
    </div>
    <!-- jQuery (necessary for Bootstrap’s JavaScript plugins) -->
    <script src=”https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js”>        </script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src=”js/bootstrap.min.js”></script>
</body>
</html>
```

You may have noticed that we contain the opening &lt;div class=“container”&gt; in our header.php and then all the closing tags for the &lt;div class=“container”&gt; and &lt;/body&gt; and &lt;/html&gt; with all of our scripts as well in the footer.php.

This is because we want Wordpress to open and close the container and html document on every page so we can focus only on the content in the middle and manipulate it how we see fit.

The sidebar.php also becomes separate because we want to widgets that area later on with pre-built Wordpress widgets.

 Awesome! You have officially created a semi-dynamic Wordpress theme. Now we need to go through every file and add some Wordpress functions to get the functionality working nicely and dynamically so we can add and take away content using the Wordpress Backend. You may have noticed that the navigation, sidebar and footer of our website are all missing…

### 05. EXERCISES

1. Create a simple Bootstrap Responsive Homepage, cut the header, index, footer and sidebar sections up and add them respectively to their own .php files. Create a style.css with the relevant meta-data and a screenshot.png and upload your theme to your Wordpress installation.

