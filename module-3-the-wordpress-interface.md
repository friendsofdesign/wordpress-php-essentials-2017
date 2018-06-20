# MODULE 3 – The Wordpress Interface

01. The Dashboard

02. Posts

03. Media Library

04. Pages

05. Comments

06. Appearance

07. Plugins

08. Users

09. Tools

10. Settings

11. Exercises

### 01. THE DASHBOARD

So, we’ve successfully installed Wordpress, your database is connected, username and password is set, and now its time to get familiar with the Wordpress Dashboard. The Dashbaord is the main landing page for any Wordpress installation, and provides you with all of the links to get to the places you tneed to, in order to build and customize your website.

1. The Widgets

2. Sidebar

3. Admin Bar

Lets start with the Widgets. These widgets exist to provide you overall information about your site, some news from Wordpress’ blog as well as some quick editing features that you can publish posts from, the widgets can be easily re-ordered and the “Welcome” banner can be closed. If you know about the Wordpress codex, then you can jump into the functions.php file and hide some of these widgets, unfortunately there is no way of customizing them without using PHP. You will find that some plugins, like Google Analytics for instance will install their own widget on the dashboard. You can also collapse widgets so that they dont take up as much space as their default. I’ve found that I dont use this area all too often.

Next is the sidebar. This houses all the special functions and abilities contained with in Wordpress. We’ll go through them one by one in the next few sections. It should be known, that Wordpress was built for simplicity and power, each post-type, like pages or posts, portfolio or sliders are what are know as custom post types, and they all work off the same 3 tier principle: “All Posts“, “Add New”, “Categories” - you will find these options on all post types - some more customized, some not. The admin bar, which can be turned on and off on the client side of your site, helps with quick tasks, like comments and and post creation, some plugins like Jetpack also use this admin bar for settings and tracking. Its helpful to have turned on especially when you are setting up your website for easy access back to your dashboard. Lets go through each tab individually now as to get you more familiar with how Wordpress works.

### 02. POSTS

The posts tab houses your blog. Each Wordpress installation comes default with posts and you will see just how it fits together in a few lessons time. By clicking on Posts you will be sent to the posts directory.

Here you will see all posts created, deleted and published. You will also see important meta-data like title, author, categories, tags, comments and the time of publishing.

To create a new post - click the Add New link \(theres two\) and you will be redirected to a WSYWIG editor for post creation.

Here you can create new posts, as if writing in a normal text-editor, or you can write in structured HTML by switching between the Visual, and Text tabs. You can select Categories and Featured Images \(which is thumbnail image users can associate your blogpost with\) as well as Publish your posts.

You can also schedule posts and save them in Draft mode, which will save any work you’ve done without publishing it to the front of your site. We could easily spend an entire lesson on this, but I will keep it short as we have alot to ge through. Make sure you follow along in the examples in class.

### 03. MEDIA

The Media library is Wordpress’ directory for housing all your pictures associated with your blog, whether its photographs, logos, portfolio items or social media icons, it can be quite useful for custom development. The media library works by creating a folder in your default Wordpress installation within a folder called “wp-content”. Everytime you upload media, Wordpress archives the upload by year and month, which can be quite helpful. The Media Library has a different view when accessing it from the Dashboard, compared to using it from with in a post, see below:

As you can see, the two versions are very diferent. Wordpress also natively supports the creation of galleries, enabling the user to select images they have uploaded, and Wordpress doe sthe rest, rather than installing a 3rd party plugin.

### 04. PAGES

Pages are used to input custom content or even static content where you see fit, in a traditional blog or website you’d create a contact page or an about us page - the content is always the same unless you have some specific functionality. The Page view brings up the same editor as the Posts view does with one or two differences.

As may see, in the Page Attributes box, the page can be set with a specific template - you will learn more about this in the 2nd part of this course, but they are normally templates like Contact, Full-Width or Homepage. This is coded up in the development process and set by the theme developer, for you conveinience more than anything else.

### 05. COMMENTS

The Wordpress comment system unfortunately leaves a lot to be desired, although powerful, it is very seceptible to spam and bots posting irrelevant and advertorial comments on your posts, its for these reasons that reCaptcha \(the form that forces your to decipher letters or numbers\) was created so that only humans could post comments.

Wordpress doesnt support reCaptcha natively, but there is a plugin for it. The plugin Akismet - is Wordpress’ default plugin for comment spam. Nevertheless, the owner or administrator of the website has full control over commenting, you are notified when comments are made, and if you find them hurtful or slanderous, you can chose not to even show them on the blog and ban the individuals IP address for good. Be careful of clicking on spammed links and they can sometimes be phising strategies to capture your information.

Its always considered good practice to management your comments correctly, dont have 5000 pending comments outstanding as it sits in your database taking up space and slowing down your Wordpress installation.

### 06. APPEARENCE

With in the appearence tab are a few important sub-sections:

Themes are the first section. Here you can upload themes, and even search for themesthrough the Wordpress Theme depositary \(an online sources of all themes uploaded to the Wordpress.org website\) In the screen shot above, you can see which themes I have uploaded on my installation of Wordpress.

We will be coming back to the section many times in the next few weeks, so im not going to go into too much detail about it right now. If you’ve installed a theme that has the “Customize” function enabled you will see a Customize tab visible under appearence. When theme authors create themes, they normally provide 1 or 2 options to customize the theme without you needing to change code. That will either be “Customize” or “Theme Options” if they think their theme options are more poweful than the customize tab then they will leave customize out completey. When you click customize you will get a sidebar alongside the main view of your homepage.

This bar, almost always contains specific Wordpress native customizations, like which menu to use, what name to give your website and whether you would like the homepage of your website to be a static page or your latest posts. It will differ from theme to theme. This is the theme options view that come with the installed theme I have activated.

Again, this will differ for every theme you install. Powerful themes normally have this option and it takes a very skilled Wordpress developer to produce something in this regard.

**Widgets**

Widgets are another very customized addition to your currently installed theme. Some theme developers create their own widgets that provide specific functionality to their theme. Wordpress is comes packaged with its own widgets, theres quite a long list, but they are mainly blogging focused, like - Recent Posts, Recent Comments etc.

Widgets only work in areas of your theme that have been registered to support widgets - this normally includes the sidebar and header of your theme, but can also include your header.

**Menus**

Menus contain a list of all pages and categories on your site, and let you organize them into a concise navigational menu for users to navigate around your site in a traditional fashion.

Adding to pages and categories, you can also link out of your website using custom links - say to “www.google.com” Here you can add a meta-description - describing what you’re page is about. You can also add keywords that Google will match with keywords typed into the search bar so that people can find your site.

To order menus - you can just click and drag to re-arrange. You can create as many menus as you like, but theme authors sometimes only make 1 or two places with in the theme available for menus to go - normally the top of your website and the bottom, you can choose what menus you want to go where in the “Manage Locations” tab at the top of the Menus page.

**Editor**

The editor contains a list of all theme files that are available for the current theme, Im not going to go into too much detail about it now, as you will become incredibly familiar with this section later in the course. The Editor provides access to the code of each document that makes up your theme, allowing you to customize code as you please. It can be useful but very dangerous at the same time. One file you will consider editing in this section is the functions.php file for instance.

A sitemap is a simple file that contains a breakdown of all the pages on your website. Google likes these files as it can quickly tell how big your site is, as well as what the site is about to a degree. Always make sure you include it for better SEO.

### 07. PLUGINS

Plugins are ususally 3rd party files that extend the functionality of Wordpress, they have been written with Wordpress in mind of course, however some are not written with CSS that will work with your theme.

Certain plugins can course problems and sometimes even break your theme, and there are certain rules that you should follow in order to keep your site safe in the long run especially when choosing plugins to install. We will go through plugins in more detail later in the course, but for now, just know that they exist and they can add some amazing functionality to your site. You might have noticed that plugins also come with an Editor allowing you to customize the code with in them, this is an advanced feature for developers and can include files like PHP, Javascript, JSON and CSS.

### 08. USERS

Wordpress natively allows the registration of users on your blog - if you allow it. If you want interaction and for people to comment and follow your blog, this is what you need to do, that being said Administrator profiles, \(with the most privledges\) can manage all users as they see fit. If you are a author or have some form of content generation on your site you can customize your profile which includes your public name, image, social media links etc. With the new release of wordpress you can even customize your back end colour scheme. We will go through all the options in class, but know that certain parts will and wont show up on your site depending on the themes author and what the purpose of the theme is.

### 09. TOOLS

The Tools section gives you some options for miscellaneous wordpress functions. “Press This” is a bookmarklet that lets you clip content from the web and add it immediatly to your blog. There is also an Import and Export function which will allow you to export content from your site and import content into your site from other blogs like Tumblr or Blogger or even another Wordpress blog - you’ll use the Import function quite regularly if you are downloading other theme authors themes in order to replicate content, pages, pictures and posts on your own installation of Wordpress. More on that later though.

### 10. SETTINGS

Settings has a number of important options.

Il go through them individually here:

**General**

General settings include things like Site Title, address, User roles, admin details and time format, I will go through them in detail in class, but sometimes you might find the answers to your problems here. Writing settings lets you set defaults that are concerned with publishing content to your site, I will go through the settings in class individually, but some interesting sections here are the Post via Email settings where you can send an email to Wordpress with your post content. This mail can be routed through your own personal domain which means you can update your blog from anywhere.

**Reading**

You will find yourself navigating to this page alot in your Wordpress career. Most themes require you to set a specific static page for your home page. This can be set in the “Front Page displays” section, you can also changes settings for your blog page as well as your Search Engine Visibility - if it is ticked, then search engines like Google will not index your site - of course that doesnt matter if you’re on a local server, but if you arent getting Google results on your website, check if you have this box checked or not.

Discussion has a number of settings that are related to comments and interaction on your website. Its not possible to go through all of them here, but I wil make mention of them in class. One special section to point out is the Comment Moderation section which allows you to ban comments when users use certain profamities or slanderous langauge. You can even block people off of your website.

**Media** 

The Media settings sets defaults for Media sizing and uploading. Dont mess around with these settings unless you know what you’re doing as it might yield some unexpected results on the front-end of your website.

**Permalinks**

Permalinks are how your links appear in the URL bar of your browser. You can set your own structure or you can choose from one of the defaults. If for instance you wanted to get your “About” Page to read http://www.example.com/about you would need to set your Permalinks structure to “Post Name” - we will go through the different options in class.

### 11. EXERCISES

1. Familiarize yourself with the Dashboard. Change settings, apply a new theme, download and active plugins and see their effect.

