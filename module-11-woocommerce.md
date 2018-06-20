# MODULE 11 – WooCommerce

01. Installing a Compatible Theme

02. Installing Demo Content

03. Understanding Orders

04. Understanding Products

05. Understanding Coupons

06. Setting Up Your Store with Settings

07. Managing Payment Gateways & Logins

08. Setting Up an Effective Product Page

09. T&C’s



### 01. INSTALLING A COMPATIBLE THEME

If you decide on a theme. Best it be optimised for WooCommerce. Most theme developers, for instance those on Themeforest, will spend a lot of time integrating WooCommerce / Wordpress hooks and CSS into their themes to give theme buyers and users complete peace of mind when it comes to installing WooCommerce into the theme.

Themes can be found all of the internet. Make sure you find a theme that most suits what product your selling as authors will write extra functionality, or include extra product specific plugins that will enhance the functionality of your store with little effort.

If you’re looking for a free theme, WooThemes \(the creators of WooCommerce\) is the best bet. As they created WooCommerce, they naturally can provide the best theme possible from their side that is optimised for the plugin.

Careful of installing themes that you don’t find in reputable locations on the internet. They can cause problems and are usually sabotaged with strange glitches that don’t make pro grammatical sense.

For a practice theme, you can download MyStile free from [www.woothemes.com](file:///Volumes/UserData/rlochner/Desktop/www.woothemes.com) - you will need to create an account, but checkout is free.

### 02. INSTALLING A COMPATIBLE THEME

If you need to install dummy data in order to get a better idea of how your shop functions and works you can use the Wordpress Importer. To access the Importer, you need to go to Tools &gt; Import, and select Wordpress at the bottom of the list. This will prompt you to install a plugin called “Wordpress Importer”. Once installed and activated. You can navigate to:

htdocs &gt; wp-content &gt; plugins &gt; woo commerce &gt; dummy-data

In the dummy data folder, select the dummy-data.xml - make sure you click the “Download file attachments” checkbox. It should import all product data and images and setup a quick dummy store for you, filling out content pages like Shop and Product pages respectively.

As mentioned above, this can be very useful when setting up your store. However, you will need to delete all of this manually before uploading your real products and testing your stores payment gateway.

### 03. UNDERSTANDING ORDERS

Orders are key to understanding WooCommerce, and the backbone to how the entire plugin works. When a customer places an order, a number of things occur:

1. The Payment Gateway is contacted
2. An email is sent to the store owner
3. An email is sent to the customer
4. An order is placed in the “Orders” section of WooCommerce.

Orders have a number of states that they exist in.

**On-Hold**

An on-hold order normally means that the user has placed an order but payment hasn’t been verified.

**Cancelled**

This normally indicates that payment has been verified, but the user has asked for the garnet to be returned or monies refunded.

**Completed**

Completed indicates that there was a successful exchange of goods for money.

It is up to the store manager/owner to manage orders and their statuses. Buyers will get a notification when their order stat changes via email.

Woocommerce also has an alternate way of placing orders. Manually. Store Managers can create order from scratch, assign products and discounts as well as configure payments and order statuses.

You might want to use this functionality if say for instance, you had a private client ordering bulk and they required an invoice and separate/custom shipping quotes.

In order for a buyer to place an order, they generally should create an account to help protect their information and private details. You will gain access to these details and can export them to a database for further marketing efforts or direct mail marketing which will help strengthen your brand.

In the Orders overview, you will get a list of all orders on your site, the payment methods used as well as their status. More importantly, each order has a unique number \#8950. Which helps you distinguish customers if they have a complaint or query. Order numbers are provided on both your notification\(as the store manager\) as well as the customers receipt of purchase. Products can be as simple or as complicated as you want in WooCommerce. There are few things you need to consider when it comes to setting up products.

1. Categories
2. Shipping Classes
3. Attributes

Categories help you distinguish between groups of products.For instance, if you look at the Apple Website:

* Mac is a category
* OS X is a category
* iOS is a category etc, etc

You should group your products into categories so your user can decide if his/her product resides in a particular section which would be easier to find on your site.

### 04. UNDERSTANDING PRODUCTS

Shipping Classes allow you to apply different shipping rates to different products. The most important thing to determine here is really; “What is my most expensive product to ship”. When you need to courier or ship products from your store, your local post office or courier will measure the length, height and breadth of the parcel as well as how much it weighs and reference that with a chart.

Basically, the more difficult it is to transport, the more expensive it becomes. If you were selling an array of products, you might want to classify them according to this very predicament. Lets take the example of a 27” iMac computer versus say an iPad Air Cover - two totally different products, with totally different dimensions and weightings. You might also want to consider where these products are going to as well. Shipping overseas can be seriously pricey and you might have to pay import/export duties on the products depending on the rules of the particular country. They all differ.

Lastly, Attributes are used for products with variation. Woocommerce has 3 types of products. Simple - like a generic product, say a Moleskin Notebook. Variable - so a dress with many different sizes and colours, and Digital, like software or an app or ebook.

Digital Content doesn’t require shipping.

Variable products require a number of attributes to work. Your attributes may be; size, colour, shape, range, etc etc. Its good to know this before adding content as it can get a little tricky. All products on your store must have their own SKU. An SKU is a generated code that helps you identify particular products. They normally show up on orders and on product pages, and can be very helpful in a scenario like:

“Hi There, Im looking at your website and I really like the white t-shirt with the feather on it. Does that item come in XL?”

Hmm, you may have multiple t-shirts with feathers on them, some big, some patterned. You have no idea what the customer is talking about. This is where the SKU can come into play. Ask the customer to provide you with the SKU of the product and BOOM! You know exactly what he’s talking about.

On a Products page, there are quite a few settings that we need to take a look at. Heres the basic outline though:

We need to choose type of product first. Lets go with Variable as the most options will be utilised here.

**General:**

Add you SKU - this can be any unique number. Make sure that they are all different.

**Inventory**

If you check “Enable Stock Management at a Product Level”, you will tell WooCommerce how much available stock you have available for trade. You can also allow or disallow back orders. If you run out of stock, your product usually is removed from the store, however if backorders are enabled, the user will be able to purchase the item and it will be up to you to order more stock.

**Shipping**

The weight and dimensions for the product can be added here, as well as a particular shipping class that can apply to the product.

**Linked Products**

This section is really about trying to gain more sales for your website. A Cross-Sell is for related products, maybe a pair of jeans. An Up-Sell would be something like you’re considering buying an iPhone 5, but an iPhone 6 is available for purchase as well.

**Attributes**

Ah, we’re back to attributes. These attributes can be applied to products that require them. When you create an attribute. Say “Size” you will also need to configure “terms” which would be the XS,S,M,L,XL.

In the attributes tab, select the Attribute you want to display. You can hit “Select All” for to grab all the terms, make sure “Visible on Product Page” and “Used for Variations” are both checked. Click Save

Attributes will need to be applied to a product, and then the product will need to be “Published” before continuing with Variations

**Variations**

In the variations tab, you can select “Link All Variations”. This will pull all attributes and their grouped terms across.

We now have a whole lot of extra options and field we can fill out, its important to fill out the price - only if the variation governs a different price. The stock quantity is also important. Once you’re done hit Publish/Update

**Advanced**

The advanced tab has a Reviews checkbox. This can be useful if you would like people to leave reviews of your product on a product page.

Make sure you also set a featured image for the product, you will also be allowed to upload to a product gallery. You can add a description for the product as well as a short description and finally the layout of the page. These pages normally work better as full-width pages.

There are also a few WooCommerce Plugins that aid with some extra product functionality:

**Accepted Payment Methods**

This adds the preferred or accepted payment methods to your site, like Visa, MasterCard etc. The very fact that this appears on your site will gain some trust from the user.

### 05. UNDERSTANDING COUPONS

Coupons are used for competitions or marketing promotions to provide cart or product based discounts for user that provide a particular code. Like products, theres many options that apply to Coupons. Give the coupon a name like FOD\_Discount and description so that you know what its for.

**General**

Coupons can be applied to a static price based on the total of your cart, a cart discount in percentage. A static product discount or a product discount percentage. You can specify the amount statically or in % if need be too. Its important to set a n expiry date otherwise customers will always be able to apply the coupon code.

**Usage Restrictions**

This section can get a bit technical, so we’ll go over it in class. Make sure you take lots of notes.

**Usage Limits**

Allow you to set the number of times a coupon is used in general or per user. This can be extremely helpful when trying to control marketing campaigns.

### 06. SETTING UP YOUR STORE WITH SETTINGS

The Settings tab is extremely important when it comes to WooCommerce. Its basically the guts of all the plugin.

**General**

**Product Options**

**Base Location**

You need to set a base location for the store. i.e South Africa, this wont necessary show up on the front of your store, but it is required, as well as for tax reasons.

**Selling Locations**

Here, you will want to tell the plugin what countries the store sells to. Some products aren’t allowed in certain countries. You will need to be aware of this.

**Currency**

Make sure you choose a currency that integrates with your payment gateway. You can also choose its format.

**Products**

Its important to choose the “Shop” page here as you want all your products to be archived on this page. This is generally setup automatically, if WooCommerce has asked you to

“Install WooCommerce Pages”

**Add to Cart**

You’ll want to use AJAX here so that your site doesn’t need to refresh once you add a product to the cart.

**Product Data**

Make sure you’re using whatever measurements the country of your store or courier uses.

**Product Ratings**

These can work for you and against you. Its up to you if you want to implement this functionality.

**Product Image Sizes**

These settings can get a little complex. Its generally better to leave them on the default unless you really understand your layout and the CSS.

**Inventory**

Stock Management is important when selling products online.Make sure its always checked so WooCommerce can do the hard work dynamically.

Hold Stock, allows for those situations where customers are in the buyers process and have technically “bought” an item of stock, but haven’t paid. This will open up the stock to others after the default 60 minutes.

WooCommerce will also send you an email when you are low on stock and out of stock. Its a good idea to set those thresholds below as well.

Lastly, you can check the “Hide out of stock items from the catalog”.

This will hide any items that are out of stock, but you can use back orders if you run a popular store and know you will be getting stock sooner rather than later on a given date.

**Checkout**

Coupon codes can be applied at checkout, if this option is checked it will display the box. If you would like customers to be able to checkout and pay without creating an account, you should check “Enable Guest Checkout”.

The “Cart” Page and “Checkout” pages must have physical pages to work and be set here, Terms and Conditions is advised, but optional.

Payment Gateways will display in the order of those which are active. The Checkout section also contains all settings for active payment options.

**Shipping**

Shipping needs to be thought out well. Theres a number of ways to handle shipping.

One way is to use a Flat Rate - the same rate for every product and destination no matter where or what. If for some reason you don’t ship overseas or to certain countries you must specify this as well. You don’t want to confuse customers to the point where they get to checkout and find that they cannot purchase.

You can also offer Free Shipping on all products, and rather build the actual courier rate into your margins, which can appear to be quite a clever marketing technique, as long as prices don’t become too exorbitant. Free Shipping is also advisable on minimum order amounts which can be set here too.

For International Delivery, a completely separate fee can be charged. International Delivery is more complicated. It also takes longer so client will want to be able to track their packages around the world. Its considered good practice to set the cost as well as apply a minimum handling fee. This will allow you to keep a relatively firm grasp on profit as you don’t want international delivery to be too expensive for you or the client.

Local Delivery can also be set, depending on where your office or depot is located, normally stores will have a radius within which they will deliver too free of charge, or for a reduced rate.

_If we had to collate all of this info it would look something like this:_

Flat Rate: R150 \(Anywhere and Everywhere\)

Free Shipping: R0

International Delivery: R200 + R100 \(Handling\)

Local Delivery: R50 \(10km Radius\)

**Accounts**

When users want to buy a product, they will be prompted to create an account. This does two things:

* Add the customer to your database
* Provides them for easy buying access the next time they purchase.

**Emails**

Emails are the backbone of communication for WooCommerce. Its one of the few ways that you can actually communicate with your customer. There are quite a few emails that can be sent out:

New Order

Processing Order

Completed Order

Customer Invoice

Customer Note

**Reset Password**

New Account

Some of these you will receive as the store manager. Others the customer will receive to confirm their order has been placed and processed.

WooCommerce allows you to customise the email templates that get sent out. You can choose the colours from the this particular section. In order to customise these templates you will need to copy the folder emails, found in:

woocommerce/templates/

to

mystile/woocommerce/emails

Each email can be copied across manually and through the tabs at the top of the Email section inside Settings. The email files are actually PHP files, so be careful about what you’re editing. HTML Emails can be quite challenging to get right and display correctly.



### 07. MANAGING PAYMENT GATEWAYS AND LOGINS

One of the most stable Payment Gateways is Paypal. Paypal comes pre-built into WooCommerce. Paypal can also be embedded on your website, so your user doesn’t have to be redirected somewhere else to pay. This can help build trust and security for the user.

Paypal however does not accept the ZAR and many other African Countries. Payfast is the other free alternative. You will need to setup and account with them and submit some documentation. They will provide you with a Merchant ID and Key which you will need to use and save before you store can go live.

Most payment gateways offer a sandbox. A sandbox is a “testing-environment” which enables you to make dummy payments to make sure your orders and system is working okay.

Remember, if you are going to charge tax or VAT. You will need to get registered and probably get an accountant to help you with this part, especially from an auditing/business/SARS perspective. Make sure you get some advice first before tackling this.

**Logins**

When a customer buys a product and creates an account, they default to a customer user role. They can see certain parts of the backend, mainly their user profile. Its up to you to keep this information safe. Remember to ask permission from your clients, or include it in the registration process if you are to add it to a MailChimp Community list or something similar.

### 08. SETTING UP AN EFFECTIVE PRODUCT PAGE

**Information**

The more information you can provide on a per product basis, the better. Customers want to be equipped with as much knowledge about the product that they are buying as possible. Remember, some one who is online and search for products is already halfway through the buying cycle. They just need to put their faith in the right brand/store. Its your job to convert them.

Its always considered good practice to give a solid description of the product. This can be written in a brand tone for instance that will make it more interesting. Short Descriptions act as summaries which can also help the user gain a quicker understanding as to what the product is about.

If the product has variants like size and colour, then that needs to be communicated in a compact way. SKU’s are also important to show. Customers also like to know how much stock is left or how much stock has been sold which can be shown quite easily with Woocommerce.

Information can be displayed in many ways, like modals and charts, so you should be as creative as possible in order to show what you think should be made aware of about the products nature, colour, washing instructions, longevity etc.

**Imagery**

We all know a picture can tell a thousand words. So what about 6 pictures. Shots of your product in many different ways can help the user gain a perspective. Side, Front, Back, 3/4, Full-Body, Close-Up etc etc. Providing lightbox functionality is also useful to gain a better idea of detail without taking up too much space.

6 Images will be enough. You don’t want to overwhelm the users senses and confuse them otherwise they will simply leave your site.

**Reviews**

Reviews can be positive and negative. Good reviews will increase your brand loyalty and positioning while bad reviews will make other customers change their minds. Nothing is more powerful than human opinion. Reviews act like comments, so they can be suspended for review until you commit it to the front of your site or product page. Use them with care.

**User Experience**

Layout and typography can be a great asset to converting a possible lead into an actual buyer. Make sure to use columns and lead the eye around where you want to the user to move around the page. Use colour to distinguish between sections of importance and font size for information that is more crucial than other information. Certain layout elements like tabs and accordions can also work to your advantage.

**Related Products**

Displaying related products below the main product can help the user add to their cart, maybe extra accessories or garments that will complete an outfit. Its a psychological marketing technique that have been proven to work time and time again.

To really nail this concept down, always display a model with a full outfit that accentuates the garnet you’re trying to sell, then sell those extra items below the product so the user can find them quickly and easily.

### 09. T&C'S

Terms and Conditions not only protect the user, but you as a store owner as well. You should always add a T&C’s on your store so customers know what they are getting themselves into in the event of something unforeseen or untoward happening.

Its good to get a lawyer to construct a T&C’s for you as they will be aware of any loopholes you may run into.

