# MODULE 5 – Theme Customisation

01. Understanding Theme Customisation

02. The Wrong Way to Customise Themes

03. The Right Way to Customise Themes

04. Creating Child Themes

05. Practical Exercise

06. Exercises

### 01. UNDERSTANDING THEME CUSTOMIZATION

So its at that point now, where we’ve got a great theme thats providing us the functionality we need, however certain things you want to change, maybe you want certain elements to disappear or change position.

There are right and wrong ways of doing this. Some are more counter-productive than others, so we will look at both today and be able to put into practice the best, most time effective workflows we possibly can for your future Wordpress career.

### 02. THE WRONG WAY TO CUSTOMIZE THEMES

Theme authors normally provide a Custom CSS box in their theme options, this is very useful as it has more “importance” than other CSS in other parts of your theme, however there are problems with this method. There is no way to add Custom PHP or HTML. Sometimes, but very rarely you will get a Custom Javascript box as well.

You could also edit the CSS or PHP directly with in the core theme files. This means that you will have no issue with changing the css and it updating on the live site. You could also custom edit JS files as well the functions.php and other theme template files.

Seems all well and good and its not that it doesnt work! It works great.

Specially if you know what you’re doing. BUT. Themes get updated right? Bug fixes, glitches and redundent code get removed and replaced, if new features are added then code is replaced and changes and manipulated to make your theme that much better. However, the author hasnt taken into account your theme changes in the CSS/PHP/JS files nor does he know what you have added to your Custom CSS boxes. PROBLEM. As soon as you update. Its gone. Back to zero, all that time you spent looking for complicated CSS classes and nested divs is for nothing.

### 03. THE RIGHT WAY TO CUSTOMIZE THEMES

So after hearing all that, you’re probably wondering, well how on earth do I get around this? The solution is really simple. You create what is called a child theme. So what does a child theme do? Not much really, it just allows you to change code without changing your core themes code, which means that when you update your parent theme, none of your hardwork is effected. It also means that you dont go hacking away at the theme authors hardwork, possibly end up deleting something you really need but dont understand and starting from square one all over again.

I like to start off with child themes as they give you a good insight into the foundations of Wordpress theme development. If anything, if you dont understand how Child Themes work, then you will find true Theme Development a bit hard to digest, so pay attention in this section, it will help you a lot down the way!

### 04. CREATING CHILD THEMES

Its time to get into the nitty gritty now. It will be the first time you open up the code editor in this course, Sublime is installed on the computers so get it up and going. Before you do that however, you’re going to want to create a folder. For your own sanity - take your currently installed theme and name it “yourthemename-child” This will keep your mind on tracking when uploading and installing. In Sublime create a style.css and add the following text in CSS comments /\*...\*/ if you cant remember.

```text
/*
Theme Name: YourTheme Child
Theme URI: http://www.yourname.com
Description: YourTheme Child
Author: YOU
Author URI: www.you.com
Template: YourTheme (this one is important, it tells Wordpress what your parent theme is!)
Version: 1.0
*/
```

Then close your comments!

You then want to add a @import CSS property that will import the existing style sheet of your parent theme, heres the syntax:

`@import url(“../YourTheme/style.css“);`

This property should not be in comments, its a live CSS rule. Remember, everything is case-sensitive, so write your them name and file names exactly as they appear in your directory.

Now, go to your Worpdress Dashboard, Appearence &gt; Themes and upload your child theme,you can zip it on your harddrive first and select it through Wordpress Theme upload dialog, or if you’re on MAMP you can just drag the unzipped folder into your wp-content &gt; themes directory.

The most dynamic thing about Child-Themes is that you can replicate any file and change it around with out effecting the original themes installation. I wont get into this now - but try create a functions.php file and uploading it - your parent themes functions will be loaded after your new functions in the child themes functions.php.

Just remember to keep all file paths the same - so if your parents theme file path to the style.css is in a folder - yourtheme &gt; css &gt; style.css then keep the same structure in your child theme for good measure.

### 05. PRACTICAL EXERCISE

**Welcome to Prac Day.**

Today I expect you to cover everything in the last two weeks. Please adhere to the following instructions.

**You have 3 hours:**

1. Delete your current installation of Wordpress

2. Delete your database through MySQL

3. Copy the latest version of Wordpress to your local web server directory

4. Create a new database in phpMyAdmin.

5. Run the Wordpress install - or - edit the wp-config-sample file yourself

6. Create a site title/name/description etc, login in to your site afterwards.

7. Activate Twenty Twelve

8. Create a Child Theme that consists of a:

* screenshot.png
* style.css
* functions.php
* a folder called page-templates
* with full-width.php located inside

9. Add the following piece of PHP to your child themes full-width template in order for it to display a dynamic copyright:

`<p class=”copyright-footer”>&copy; Copyright 2010 - <?php echo`

`date(‘Y’); ?><?php bloginfo(‘name’); ?>`

`</p>`

Write a CSS style within your style.css file in your child theme that will make the following properties true:

**Font size = 14pts**

**Font Colour = black**

**Text Align = right**

If you can easily get through this exercise, you are ready for the next part of the course. Goodluck, remember to ask if you have any questions.

### 06. EXERCISES

1. Create a child-theme by creating your own folder and style.css, custom sections as you may with your own Wordpress PHP functions and CSS styles. Remember to use Chrome Developer Tools to help you.

