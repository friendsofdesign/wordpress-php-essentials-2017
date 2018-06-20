# MODULE 2 – Installing Wordpress

01. Setting up a Local Server with MAMP

02. Create a MySQL Database with phpMyAdmin

03. Understanding Databases

04. How PHP, MySQL and MAMP work together

05. Setting up a Wordpress Installation on a Live Server

06. Installation Run

07. Exercises

### 01. SETTING UP A LOCAL SERVER WITH MAMP

Wordpress is essentially just a file structure of server specific files. You can download it from wordpress.org. Once the download is finished you will see a wordpress-3-9.zip file on your hard drive, double click that to unzip and a folder will be extracted, within this folder are the wordpress core files.

**There are 3 ways to install Wordpress:**

1. Famous 5 minute install
2. Using cPanel on a live server.

We will go through these installations in training, in the notes further things need to be explained before we continue with installation, namely MAMP, MySQL and phpMyAdmin. A local server is essentially a live web server that uses your computers ip address to show websites that you build. No one can access it but you, its not a live website and it will only run when a particular program is running in the background. This program is known as MAMP. MAMP stands for:

Macintosh, Apache, MySQL, PHP. Its a stack of programs that integrate with each other to provide you with everything you need to run a virtual web server. Macintosh is your OS Platform, as you might have guessed there is a WAMP \(Windows\) and even XAMP \(pronounced ZAMP\) for Linux or Windows, or Mac. 

Apache is a type of web server. Most web servers use apache. MySQL is your database facility PHP is the server-side script that communicates with the server \(Apache\) and the database \(MySQL\) MAMP combines all these technologies into a nice user-interface for you, otherwise you’d be using the Terminal or DOS to write commands which is a language itself. You can download MAMP from www.mamp.org

It is installed on the computers, so open it up. We might have to set some preferences on first launch. Click on Ports and set Apache to 80 and MySQL to 3306. Doing this, will allow you to access your Wordpress site at the following URL http://localhost or http://localhost:8888

Next you will want to specify a folder on your computer where all the files for your site will live, click on the Apache tab and hit “Select” to open your HDD browser. I normally add this folder to Documents, so its out of the way. If you move the files from this folder, or the folder out of its default location, your site will break.

Make sure that before you save through - that your Apache and MySQL servers are both running, indicated by a “green” light - if one is red, then there is a problem with the port numbers or the network that you are connected to is blocking that particular port for security reasons.



### 02. CREATE A MYSQL DATABASE WITH PHPMYADMIN

Its now time to create a database through a program which is launched from MAMP known as phpMyAdmin. Its a simple program that runs in your web browser, and gives you control over database functions.

In MAMP click the Open Start page button - this will take you to the default MAMP welcome screen. The tabs in the top will indicate some software that is currently available for you to run

What you get next might scare you a little, but its nothing to be afraid of, click on the database tab and then type in a name for your database - call it “yourname\_db” make sure you remember it, EXACTLY how you have written it. Keep it safe somewhere, as you will need it again soon. Right now, thats all you need to get things going in terms of a database.

### 03. UNDERSTANDING DATABASES

You’ve all used Excel before...well - that is essentially a databse. A MySQL database uses tables and headings to structure information. Each cell has certain information stored with in it. In Wordpress’ case, it uses these tables and headings and structure to store information, links, media, posts, pages and settings in a central...well, database, that it can quickly access when you request it from the front end.

We will briefly go through some of the tables involved in the Wordpress installation, but its not recommended to go play around with in the database. It runs very strict protocols and can be easily broken.

Certain actions like deleting the database or exporting/importing database tables can be performed using the graphical interface, or with SQL queries, which is a language in itself that is beyond the scope of this course.

For now, understand that everything you do in Wordpress will be stored in a database table.

### 04. HOW PHP, MYSQL AND MAMP WORK TOGETHER

PHP and MySQL are part of what is known as the MAMP stack \(Macintosh, Apache, MySQL, PHP\) all these softwares are installed on your computer during installation of MAMP.

You can think of MAMP as the train tracks for a process that happens. PHP is the train, and MySQL is the important destination. PHP talks to MySQL, pulling information from the database and sending it to the server, or the browser - whatever the client can see.

Of course on our end, we see HTML and CSS - PHP is such a dynamic language that it can talk to MySQL, bring up information and then easily live along HTML and output dynamically generated HTML from queries that it makes to the database - for instance, the name of your blog.

This process is fundamental to understand - see the diagram below:

### 05. INSTALLING WORDPRESS ON LIVE SERVERS

When it comes time to setup a Wordpress installation on a live server, such as www.example.com, things are a little different. Most cPanel installations have what are known as scripts that do a lot of the hardwork for you.

MySQL is native on cPanel, meaning there is a easy wizard that will take you through the process of setting up a database, database user and password - in MAMP - your username and password is either automatically specified by the MySQL installation - normally

`UN: root`

`PW: root`

**You can change your password.**

When it comes to installing Wordpress on cPanel, a software known as Softculous manages the installation of the database and the Wordpress Core - you fill out a few settings and options and it handles it for you with out you touching any code, of course you can choose to do this manually as well. We will run this process in class to demonstrate.



### 06. INSTALLATION RUN

Lets run an installation of Wordpress. First we will do the easy way - the Famous 5 Minute Install. We’ll pick up where we left off. We’ve created a database, but now we need to get Wordpress connected! Copy the files from within the Wordpress folder you downloaded, and paste them into the folder you create as the destination for your site, or your site-folder.

Make sure MAMP is still running. Direct your browser to [http://localhost](http://localhost) or [http://**localhost:80**](http://localhost:80) **or** [**http://localhost:8888**](http://localhost:8888)

Make sure that if you want to run multiple versions of wordpress off your server, you addthese files into folders with in your site folder - for instance if you copied your files into a folder named - “installationone” then you would need to point your browser to

[http://localhost:8888/installationone](http://localhost:8888/installationone)

_If all is in order, you’ll get this_

??? Missing

This is a good sign, dont worry. You will become very familiar with this wp-config file after a short while. For this installation, you dont need to touch it.

Hit the “**Create a Configuration File**”

_Awesome, you’ll be confronted with this:_

Remember your database name? _yourname\_db_ 

Your username will be root - its the default for any MySQL installation

Your password will be root if you havent changed it in MAMP

Database Host is localhost.

The table prefix can be changed to any 3 character string -

I normally choose the first letters of my name - so dm\_

This is not necessary, but its an extra measure of security incase your website gets hacked.

Click “Submit” when you are done, if everything goes well. Then you should get the following screen:

This screen asks you for a Site Title - which you should fill in

**Username:** Whatever you like

**Password:**  Make it strong

Add your email address

The privacy option lets Google index your site - maybe not such a good idea if you’re still building it! When you’re happy - hit “Install Wordpress”

If all went well - you’ll get the screen above allowing you to log in to your site. If you got this far without any problems, you’re a genius! Well done!

### 07. EXERCISES

1. Setup MAMP and download a version of Wordpress, create a MySQL database using phpMyAdmin, then install Wordpress and open up the Dashboard.

