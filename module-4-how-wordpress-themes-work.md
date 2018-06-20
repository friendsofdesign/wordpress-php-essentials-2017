# MODULE 4 – How Wordpress Themes Work

01. What are Wordpress Themes

02. Theme File Structure

03. Required Theme Files

04. Downloading and Installing Themes

05. Exercises

### 01. WHAT ARE WORDPRESS THEMES

Themes in Wordpress is a multi-million dollar industry at the moment, they have gone far beyond just “skinning” the Wordpress installation and now actually provide some serious functionality. Major websites like Envato have created an entire sub website dedicated to buying themes for your particular need. Everything from restaurant themes, to photography/portfolio, app-showcase and online learning platforms exist with in theme functionality now and thats just the tip of the ice-berg.

When its comes to using Wordpress.org - naturally web designers wanted to start moving their static HTML and CSS designs to Wordpress, enabling their clients or themsleves to be able to update content with ease and efficiency. What is commonly termed as Wordpress Theme Development is a very deep rabbit hole indeed.

Whether its a personal blog or a theme that adds some very custom funtionality like portfolios, sliders and classifieds, web designers have to make the transition to web developer, essentially learning to program, create conditional statements, and understand the logic of a computers brain.

This might seem challenging, but like anything it just takes a bit of getting used to. Like we’ve discussed before - a frontend designer/developer will use HTML, CSS and Javascript as those languages are used by the browser. A good understanding of these langauges will only get you halfway however. As Wordpress is open-source, naturally one of the best langauges to choose for server-side interaction from the browser to a database is PHP. Thus, all of our special functions and practicality use PHP to speak to server and the database.

By the end of this course, you will have put together your own personal blog and have an understanding of how static HTML and CSS can integrate with PHP to provide some very dynamic functionality.

### 02. THEME FILE STRUCTURE

As you can see above, the theme structure looks incredibly complicated. However, in saying that it is a very complicated theme.

According to the Wordpress Codex, for Wordpress to be classified as a theme, it only needs 2 important files:

1. Index.php 
2. style.css

### 03. REQUIRED THEME FILES

Yup...that simple. But, thats not going to give you much of a theme. You might be surprised to find out, and its not known exactly why - but the style.css actually holds alot of the information about your theme, like name, author and some other needed info.

Ideally - your theme strucutre should look like this:

* index.php - similiar to index.html - this file is used as a default of you dont have a page.php, it also contains “The Loop”
* header.php - You guessed it, your header information and your opening &lt;HTML&gt; tag goes here
* footer.php - You want a cookie for getting this one by yourself? Any footer information and &lt;/HTML&gt; goes here. 
* page.php - used as a template for a static page template.
* single.php - used for a single blog post
* search.php - used to deliver search results when a user performs a search on your site.
* sidebar.php - If you have registered widgets for your sidebar...they go here.
* style.css - Theme meta-data as well as base CSS styles for your site.
* screenshot.png - used as a preview for your theme when activating/installing.

With that file structure you would be able to create a reasonably dynamic theme. Ive broken down above what each file does, then view the image below to understand what it is that Wordpress is actually doing and you’ll start to understand how this genius CMS works. Obviously any images or Javascript will be placed in this root directory. All themes are encompassed by a folder with the theme name, which can be zipped and uploaded to wordpress through the “Themes &gt; Upload” section under Appearence. Wordpress will unzip the contents and place it in the correct directory for the CMS to find it. That directory is wp-content &gt; themes &gt; yourtheme

### 04. DOWNLOADING AND INSTALLING THEMES

Like we’ve discussed before, themes come in many shapes and sizes, some even include documentation to setup the theme in a specific way, some include the psd files from the author so you can change particular elements and upload. Some themes also come with what is known as “Dummy Content” this is a very special XML file - you dont need to understand the code, it is a manifest of sorts of everything from the authors installation of the theme which you can import into your installation and theme install.

The dummydata.xml can contain posts, portfolios, sliders, pages, comments, users, settings, menus etc and can even contain external links to images that the original author has used. Normally theme developers will couple a tutorial document with the xml to help you set up the theme as they have set up on their showcase site. This gives you a good starting point for customization.

We will go through this process during class, however just be ware that sometimes the import process which uses Wordpress’ Importer plugin doesnt always work when working on a local server.

### 05. EXERCISES

1. Download a free Wordpress theme and open it up in Sublime Text, try to figure out or dissect how it has been put together and how it works

