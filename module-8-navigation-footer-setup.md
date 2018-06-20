# MODULE 8 – Navigation, Footer Setup

01. Adding Navigation Array

02. Making Footer Dynamic

03. Adding WP\_FOOTER

04. Make the Copyright Dynamic

05. Exercises

### 01. ADDING NAVIGATION ARRAY

Next we’ll need to give the header.php some details in order to make sure the navigation picks up and listens to our selections in the backend of our website:

In your HTML, go find the  and delete everything that exists with in there:

```markup
<ul class=”nav navbar-nav navbar-right”>

    <li><a href=”#”>Home</a></li>

    <li><a href=”#”>About</a></li>

    <li><a href=”#”>Blog</a></li>

</ul>
```

Next, you will want to add the following PHP Array:

```text
<?php $defaults = array(

‘theme_location’     => ‘’,

‘menu’                 => ‘’,

‘container’         => ‘false’,

‘container_class’     => ‘’,

‘container_id’         => ‘’,

‘menu_class’         => ‘nav navbar-nav navbar-right’,

‘menu_id’             => ‘’,

‘echo’                 => true,

‘fallback_cb’         => ‘wp_page_menu’,

‘before’             => ‘’,

‘after’              => ‘’,

‘link_before’       => ‘’,

‘link_after’         => ‘’,

‘items_wrap’         => ‘<ul class=”%2$s”>%3$s</ul>’,

‘depth’              => 0,

‘walker’             => ‘’

);

wp_nav_menu( $defaults );

?>
```

This might look a bit scary, but its better to start from the bottom:

The wp\_nav\_menu accepts an argument which is the array called $defaults - this can be given any name you like as long as they match:

```php
‘theme_location’         => ‘primary’,   The location in the theme to be used--must be registered with register_nav_menu() in order to be selectable by the user

‘menu’                    => ‘’, The menu that is desired; accepts (matching in order) id, slug, name

‘container’             => ‘false’,  Whether to wrap the ul, and what to wrap it with. Allowed tags are div and nav.

‘container_class’         => ‘’, The class that is applied to the container

‘container_id’             => ‘’, The ID that is applied to the container

‘menu_class’             => ‘nav navbar-nav navbar-right’, The class that is applied to the ul element which encloses the menu items. Multiple classes can be separated withspaces.

‘menu_id’                 => ‘’, The ID that is applied to the ul element which encloses the menu items.

‘echo’                     => true, Whether to echo the menu or return it. For returning menu use ‘0’

‘fallback_cb’             => ‘wp_page_menu’, If the menu doesn’t exist, the fallback function to use.

‘before’                 => ‘’, Output text before the <a> of the link

‘after’                   => ‘’, Output text after the </a> of the link

‘link_before’             => ‘’, Output text before the link text

‘link_after’             => ‘’, Output text after the link text

‘items_wrap’             => ‘<ul class=”%2$s”>%3$s</ul>’,
```

Evaluated as the format string argument of a sprintf\(\) expression. The format string incorporates the other parameters by numbered token. %1$s is expanded to the value of the ‘menu\_id’ parameter, %1$s is expanded to the value of the ‘menu\_id’ parameter, %2$ expanded to the value of the list items. If a numbered token is omitted from the format string, the related parameter is omitted from the menu markup

```php
‘depth’                  => 0, How many levels of the hierarchy are to be included where 0 means all. -1 displays links at any depth and arranges them in a single, flat list.

‘walker’                 => ‘’ Custom walker object to use (Note: You must pass an actual object to use, not a string)
```

I have gone through what each parameter in the array does above.

In order to see a result - you will need to setup a menu in the Wordpress Dashboard.

### 02. MAKING THE FOOTER DYNAMIC

Next up is the footer. We need the jquery to work as well as the bootstrap.js - for now, remove all scripts from the footer.php.

### 03. ADDING WP\_FOOTER

Add the &lt;?php wp\_footer\(\); ?&gt; just before the &lt;/body&gt;. This will allow us to add scripts into our footer dynamically through our theme.

### 04. MAKE THE COPYRIGHT DYNAMIC

Lastly, lets use a simple PHP function that will always update the year, and grab the name of our website. We can use the following PHP function from the header.php file:

`<?php bloginfo(‘name’); ?>`

Which will add the name of our site where we need it.

You can also add:

`<?php echo date(‘Y’); ?>`

Which is a simple PHP function that will update the year for the copyright every year without us needing to change it.

Great!

Lets move on to the index!

### 05. EXERCISES

1. Create a Navigation Array with in your static HTML

2. Make the footer.php file dynamic buy adding your own PHP date\(\); function as well as the name of your blog.

