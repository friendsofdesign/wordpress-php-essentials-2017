# MODULE 10 – Creating Page Templates

1. Create a page.php
2. Create a single.php
3. Exercises

### 01. CREATE A PAGE.PHP

The last thing we need to do is make our theme a little more accessible. Wordpress works in such a way that if you have not provided custom-page templates for certain pages like single posts, comment, galleries or archives it will just end up using the index.php which isn’t too great an idea as layout doesn’t always lend itself in this regard.

So, we’ll create 2 templates, you can create as many as you like for the pages that you use.

Lets first create a full-width template \(without a sidebar\) for a content page:

Create a page.php file, Wordpress will use this file to display any pages with static content - at the top of the file write:

Next, include your &lt;?php get\_header\(\);?&gt;, &lt;?php get\_footer\(\):?&gt;

Great, next we’re going to want to add the following HTML:

```text
<divclass=”row”>
<divclass=”col-md-12”>
</div>
</div>
```

Remember our header.php opens our container, so its important to just add a row and whatever col-md-\* you would like to use. Im going to use 12 so my content will stretch across the middle.

Next up, we have reiterate the Wordpress Loop in order for it to pick the content that we create on any given new page:

```text
<?phpif( have_posts() ) : while( have_posts() ) : the_post();
the_content(); // displays whatever you wrote in the wordpress editor
endwhile; endif; //ends the loop
?>
```

That should do it, we could customise this a little more if we liked:

```text
<?phpget_header();?>
<divclass=”row”>
<divclass=”col-md-12”>
<?phpif( have_posts() ) : while( have_posts()) : the_post();
<h2><ahref=”<?phpthe_permalink();?>”><?phpthe_title();?></a></h2>
the_content(); // displays whatever you wrote in the wordpress editor
<?phpendwhile; endif; //ends the loop ?>
</div>
</div>
<?phpget_footer(); ?>
```

Great, go create a page, if your content spreads 12 columns and doesn’t have a sidebarwhen published, then this template is working!

### 02.CREATE A SINGLE.PHP

Next, we’ll want to create a single.php where when people click on one of our blog posts from the home page, they will be taken to the full page - we can simply duplicate the page.php and make some alterations to it. Lets get started:

We want the sidebar to appear, so lets add the &lt;?php get\_sidebar \(\);?&gt; function just before the closing div of the “row”.

Your code should look like this:

```text
<?phpget_header();?>
<divclass=”row”>
   <divclass=”col-md-8”>
       <?phpif( have_posts() ) : while( have_posts()
      ) : the_post(); ?>
       <h2><ahref=”<?phpthe_
       permalink();?>”><?phpthe_title();?></a></h2>
       <?phpthe_content(); ?>
       <?phpendwhile; endif; ?>
   </div>
   <?phpget_sidebar(); ?>
</div>
<?phpget_footer(); ?>
```

Change the “col-md-12” to “col-md-8”.

We want to display the featured image of the post, plus the full content. The &lt;?php the\_content\(\):?&gt; is already present. So lets get the thumbnail there. For now, lets just add it above the &lt;?php the\_content\(\);?&gt;

```text
<?phpget_header();?>
<divclass=”row”>
       <divclass=”col-md-8”>
           <?phpif( have_posts() ) : while( have_posts()) : the_post(); ?>
           <h2><ahref=”<?phpthe_permalink();?>”><?phpthe_title();?></a></h2>
           <?phpthe_post_thumbnail(‘large’);?>
           <?phpthe_content(); ?>
           <?phpendwhile; endif; ?>
       </div>
   <?phpget_sidebar(); ?>
</div>
<?phpget_footer(); ?>
```

Great, you should see your image there!

Lastly, we want to add a comment form so users can comment on your blogpost. Add the following:

&lt;?php comments\_template\(\); ?&gt;

Add that function just after your &lt;?php end while; endif; ?&gt;, refresh your page.

Your final code should look like this.

```text
<?phpget_header();?>
<divclass=”row”>
   <divclass=”col-md-8”>
       <?phpif( have_posts() ) : while( have_posts()
      ) : the_post(); ?>
       <h2><ahref=”<?phpthe_
       permalink();?>”><?phpthe_title();?></a></h2>
       <?phpthe_post_thumbnail(‘large’);?>
       <?phpthe_content(); ?>
       <?phpendwhile; endif; ?>
       <?phpcomments_template(); ?>
   </div>
<?phpget_sidebar(); ?>
</div>
<?phpget_footer(); ?>
```

Make sure you style these pages to your liking with CSS and other Wordpress Functions.

### 03. EXERCISES

1. Create a Single-Post and Full-Width Page Template for your Theme

