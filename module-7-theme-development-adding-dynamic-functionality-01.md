# MODULE 7 – Theme Development: Adding Dynamic Functionality 01

01. Make the header.php file dynamic

02. Make all the files come together

03. Include Bootstrap CSS

04. Add WP\_HEAD Function

05. Enabling Navigation Support

06. Exercises

### 01. MAKE THE HEADER.PHP FILE DYNAMIC

First of all, lets get rid of some of these errors that we’re getting. Most of them are due to unused files anyhow, we can delete the un-minified versions of the bootstrap.js and bootstrap.css - check your header.php and footer.php to make sure you haven’t linked to them.

You can also delete the img/thumbnail.jpg that is missing as we will correct that later. Lets get accustomed to what we need to do now, lets first replace the &lt;html lang=“en”&gt; with a PHP function - replace the whole attribute with:

&lt;?php language\_attributes\(\); ?&gt;

Next, find the &lt;title&gt;&lt;/title&gt; and in-between the tags replace it with:

`<?php wp_title(‘|’,1,’right’); ?> <?php bloginfo(‘name’); ?>`

This code contains two functions:

`<?php wp_title(‘|’,1,’right’); ?>`

and

`<?php bloginfo(‘name’); ?>`

The wp\_title contains 3 arguments: 

**Seperator -** You could use a \| or / or -

**Display -** which will format the output as text

**Location -** This determines where the title and or name of your site appears, either right or left

Refresh the front-end of your theme and see whats happened. Oops…nothing has happened. Now why is that?

### 02. MAKE ALL THE FILES COME TOGETHER

Well, what we haven’t done is told the index.php file to include the header.php, right at the top of your index.php file type:

`<?php get_header(); ?>`

And at the bottom type:

`<?php get_sidebar(); ?>`

`<?php get_footer(); ?>`

Now, we should see our entire theme back in its boring HTML form with all its elements. You may have noticed that the title in the browser tab has now changed to the name that you provided for your site in your Wordpress setup.

Its always a good idea to go systematically through your document and see what the best Wordpress PHP function is that will make your theme more dynamic, theres no need to go overboard, however there are some important tags you will need to add in order to get your theme functioning well.

Lets get our base Bootstrap CSS working:

Find the link tag to your

`<link href=“css/style.css” rel=“stylesheet” />`

Replace the `href=“”` with the below:

`<?php bloginfo(‘stylesheet_url’);?>`

So:

`<link href=“<?php bloginfo(‘stylesheet_url’);?>”rel=“stylesheet” />`

If its worked, you can check Chrome Developer Tools, if theres no error, saying the browser can’t find “style.css” then you’ve got it right! The function, we go grab your style.css in your root folder and append it to the head of your document.

www.friendsofdesign.net 72

### 03. INCLUDE BOOTSTRAP CSS

Now, how do we link up the base Bootstrap styles? We’re going to use the @import rule in our style.css

Just below the commented meta-data, add the following:

`@import url(‘css/bootstrap.min.css’);`

The CSS included in the bootstrap.min.css file will be included before we begin adding the styles from our style.css. We have linked stylesheets here, quite a nifty trick.

You will then need to remove the:

`<link href=”css/bootstrap.min.css” rel=”stylesheet”>`

From your header.php

We should only have on error left - which is the bootstrap.min.js file that Wordpress can’t find.

### 04. ADD THE WP\_HEAD FUNCTION

The last thing we’ll need to do is add a special function within the &lt;head&gt; of our header.

php called:

`<?php wp_head(): ?>`

This function allows us to register more stylesheets and scripts and places them dynamically inside of our file for us.

Your finished header.php should look like this:

```markup
<!DOCTYPE html>
<html>
    <head>
        <meta charset=”utf-8”>
        <meta http-equiv=”X-UA-Compatible” content=”IE=edge”>
        <meta name=”viewport” content=”width=device-width,initial-scale=1”>
        <title><?php wp_title(‘|’,1,’right’); ?><?php bloginfo(‘name’); ?></title>


        <link href=”<?php bloginfo(‘stylesheet_url’);?>”rel=”stylesheet”>
        <?php wp_head(): ?>
        <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
        <!-- WARNING: Respond.js doesn’t work if you view thepage via file:// -->
        <!--[if lt IE 9]>
        <script src=”https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js”></script>
        <script src=”https://oss.maxcdn.com/respond/1.4.2/respond.min.js”></script>
        <![endif]-->
    </head>
<body>
    <nav class=”navbar navbar-default” role=”navigation”>
        <div class=”container”>
        <!-- Brand and toggle get grouped for better mobiledisplay -->
            <div class=”navbar-header”>
                <button type=”button” class=”navbar-toggle collapsed” data-                                    toggle=”collapse” data-target=”#bs-example-navbarcollapse-1”>
                    <span class=”sr-only”>Toggle navigation</span>
                    <span class=”icon-bar”></span>
                    <span class=”icon-bar”></span>
                    <span class=”icon-bar”></span>
                </button>
                <a class=”navbar-brand” href=”#”>Wordpress</a>
            </div>
        <!-- Collect the nav links, forms, and other content fortoggling -->
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
```



### 05. ENABLING NAVIGATION SUPPORT

Alrighty, lets get the Wordpress navigation working. This requires us to create a functions.php file. This file adds functionality to our Wordpress theme. Create one and add it to the root of your theme folder.

In that file, add the following:

`<?php register_nav_menu( ‘primary’, ‘Primary Menu’ ); ?>`

As you can see, this function holds two arguments, and location and description. This will be our primary menu at the top of our site, you’ll see “Primary Menu” appear in the Menu’s section of your theme too.

### 6. EXERCISES

1. Make the header.php file dynamic buy replacing static content with Wordpress PHP functions, make sure you reference the codex and what we covered in class.
2. Create a functions.php and enable navigation support.

