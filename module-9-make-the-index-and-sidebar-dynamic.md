# MODULE 9 – Make The Index & Sidebar Dynamic

01. Make the index.php file dynamic

02. The Wordpress Loop

03. Post Thumbnail Support

04. Adding Custom Style & Script Support

05. Making the Sidebar Dynamic

06. Exercises

### 01. MAKE THE INDEX.PHP FILE DYNAMIC



For now, until we understand custom post types, we will just add what is known as the Worpdress Loop so it can pick all of our blogposts. The Jumbotron at the top will just stay static for now.

The Wordpress Loop cycles through a given piece of code and then replaces that content with content stores in your database - in this case, we will loop through all the blog posts that we have.

In the index.php, delete 2 out of the 3 blogposts that we already have. Your file should look like this:

```markup
<?php get_header(); ?>
<div class=”jumbotron”>
    <h1>Hello, world!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <p><a class=”btn btn-primary btn-lg” role=”button”>Learn more</a></p>
</div>
</div>

<div class=”container”>
    <div class=”row”>
        <div class=”col-md-8”>
            <h1>Latest News</h1>
            <div class=”media”>
                <a class=”pull-left” href=”#”>
                    <img class=”media-object” src=”” alt=”...”>
                </a>
                <div class=”media-body”>
                <h4 class=”media-heading”>Blog Post 1</h4>
                <p><small>Posted by Daine | September 18th | In General</small></p>
                <p class=”text-left”>Lorem ipsum dolor sit amet, consectetur adipisicing                     elit, sed do eiusmod tempor incididunt ut labore et dolore magna                         aliqua. Ut enim ad minim veniam,quis nostrud exercitation ullamco                        laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor 
                   in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla                    pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa                    qui officia deserunt mollit anim id est laborum.<a href=”#”> Read                        More</a></p>
            </div>
        </div>
        <hr>
    </div>

<?php get_sidebar(); ?>

<?php get_footer(); ?>
```



### 02. THE WORDPRESS LOOP

The Loop used a if statement coupled with a while loop to cycle through posts in your database and present them on the front of your site:

This is what it looks like, and you can paste this straight into your index.php:

```text
<?php if ( have_posts() ) : while ( have_posts() ) : the_post(); ?>

        <?php the_content(); ?>

<?php endwhile; else: ?>

        <p><?php _e(‘Sorry, this page does not exist.’);

?></p>

        <?php endif; ?>
```

We do need to customise it a little though:

```text
<?php if ( have_posts() ) : while ( have_posts() ) : the_post(); ?>

<div class=”media”>
    <a class=”pull-left” href=”#”>
        <?php the_post_thumbnail(‘thumbnail’); ?>
    </a>
    <div class=”media-body”>
        <h4 class=”media-heading”><?php the_title(); ?></h4>
        <p><small>Posted by <?php the_author(); ?></small></p>
        <p class=”text-left”>
            <?php the_content(); ?>
        </p>
    </div>
</div>
<hr>
<?php endwhile; else: ?>
<p><?php _e(‘Sorry, this page does not exist.’); ?></p>
<?php endif; ?>
</div>
```

The first function, grabs the featured image from the post-editor.

Then we grab the title of the blog post and apply it to the h4.

Next, we ask wordpress to find out who wrote the post, and finally, we grab the content of the post.

We must close off the while and if statement so Wordpress doesn’t loop forever and disrupt the content.

### 03. POST THUMBNAIL SUPPORT

In order to get wordpress to support the “featured-image” box in the post editor we mustadd the following function to our functions.php:

`add_theme_support( ‘post-thumbnails’ );`

### 04. ADDING CUSTOM STYLE AND SCRIPT SUPPORT

You may have noticed that our site responds well, but our drawer isn’t working… thats because wordpress can’t find the bootstrap.min.js. We need to dynamically tell. Wordpress where to find this file. Its not good enough just adding a script tag before our closing  tag, thats why we added our wp\_footer\(\); function.

Go to your functions.php file and write the following function:

```php
function bootstrap_scripts()

{

// Register the script like this for a theme:

wp_register_script( ‘bootstrap-script’, get_template_

directory_uri() . ‘/js/bootstrap.js’, array( ‘jquery’ ),

“1.0”, true );

// For either a plugin or a theme, you can then

enqueue the script:

wp_enqueue_script( ‘bootstrap-script’ );

}

add_action( ‘wp_enqueue_scripts’, ‘bootstrap_scripts’ );
```

Lets break this down:

We create a function - which executes a block of code.

In this function is the wp\_register\_script function which accepts 5 arguments:

1. The name of the script \(you can choose this\)
2. The source or file path of the script we use the get\_template\_directory\_uri\(\) and thenconcatenate the rest of the file path to show wordpress where to go from the root of the folder.
3. Dependants, so in our case jQuery would be a dependant of the Bootstrap.min.js so we need to tell the function that we need jQuery to be placed before this script before the closing body tag.
4. The version we’re using
5. Finally, the last argument tells Wordpress whether to place this script in the  or before the closing  tag. It require the wp\_footer\(\); function to be present in your footer.php however.

This is what a typical wp\_register\_script function will look like

```php
   wp_register_script( ‘bootstrap-script’, get_template_directory_uri() . ‘/js/bootstrap.js’, array( ‘jquery’ ), “1.0”, true );
```

Then, we have another function called wp\_enqueue\_script, which accepts the same parameters as above, theres no need to state them twice, so all you need to write is:

`wp_enqueue_script( ‘bootstrap-script’ );`

We then close off the function and use the

`add_action(); function:`

`add_action( ‘wp_enqueue_scripts’, ‘bootstrap_scripts’ );`

The add\_action function is way of hooking into the Wordpress core and getting functions to work.

We add the ‘wp\_enqueue\_scripts’ as the first function to add, and then pass through the ‘wp\_register\_scripts’ function name so that Wordpress can execute the code.

### 05. MAKE THE SIDEBAR DYNAMIC

The sidebar.php is great for adding widgets. Wordpress comes with a few default widgets like Recent Posts and Recent Comments, so lets make that sidebar dynamic so we can just drag and drop widgets in there as we like.

First off, go to the sidebar.php and replace the content with:

```php
<?php if ( !function_exists(‘dynamic_sidebar’) || !dynamic_sidebar() ) : ?>

<?php endif; ?>
```

Quite simple - make sure you just comment out the other content, and make sure you keep your  so it can be contained.

Next up, we’ll need to register the widget support inside of our functions.php:

```php
// Add Sidebar Functionality

if ( function_exists(‘register_sidebar’) )
    register_sidebar(array(
        ‘before_widget’ => ‘’,
        ‘after_widget’ => ‘’,
        ‘class’ => ‘’,
        ‘before_title’ => ‘<h3>’,
        ‘after_title’ => ‘</h3>’,
));
```

Another array with-in an if statement.

Il go through what each property =&gt; value means:

```php
‘name’             => ‘Blog’, Name of Sidebar

‘before_widget’ => ‘’, HTML to place before every widget

‘after_widget’     => ‘’, HTML to place after every widget

‘class’         => ‘’, CSS class name to assign to the widget
```

HTML

‘before\_title’ =&gt; ‘’, HTML to place before every title

‘after\_title’ =&gt; ‘&lt;/h3&gt;’, HTML to place after every title

Pretty simple. You’ll now see that the the widgets have been registered in Appearance tab, and the name you assigned will be present on the draggable area. You can drag and drop widgets with ease and they will appear in your sidebar on the front of your site.

You will need to add some extra CSS depending on how Wordpress generates the markup and styles.

### 06. EXERCISES

1. Add the Wordpress Loop to your Theme
2. Enable Post Thumbnail Support
3. Add Custom Style & Script Support using the WP\_REGISTER SCRIPT FUNCTION
4. Make the Sidebar dynamic using the functions.php and adding the required loop to the sidebar.php

