---
layout: post
title: How to create an optimized WordPress website 
description: Steps for creating an optimized WordPress website 
tagline: Optimized WordPress website creation
image: /assets/media/wordpress-bg-medblue.png
categories: [wordpress]
tags: [wordpress, cms]
---
<img src="{{page.image}}" width="85%"/>
<br/>
<br/>
WordPress has become one of the most popular Content Management System because of its flexibility, ease of use and simple code structure. Lot of premium themes are available with outstanding features and design most of the themes are made in way for making blogging simple for non-technical users. 
One can create a good looking website that can impress people within a short time using WordPress and a premium theme, even though you are not prominent with WordPress. Minimal Page loading time is very much important for any website as is an important part of user experience also for SEO.
 
 Below are some tips that may be followed for creating an optimized WordPress website 
 
<h3>1. Avoid Premium Themes</h3>
Even though premium themes are helpful for creating websites in a short time it has its own disadvantages. Most of the themes come up with a lot of features that we do not use in our website because each time while the site loads the themes will be loading the dependencies and customizing premium themes which can cause some validation errors and inturn will slow down your website. There may be a lot of plugins included for helping the users but it may also be a factor for slowing doen the website. 
 
<h4>What you can do?</h4>
 
Its like customizing a premium bike to your needs and customizing a usual bike to meet your needs 
You can start building your website from a bootstrap starter theme which is free for download 
{% highlight ruby %} 
	http://themekraft.com/tk-wordpress-bootstrap-starter-theme/
{% endhighlight %} 
_tk is a best option for building a custom theme. It is bundled with all the bootstrap elements which can help you learn the basics of bootstrap from their website easily and start building your theme. While doing this there wont be any unwanted features or plugins which will slow your website to slow down.
Since we are using bootsrap you dont have to be worried about responsiveness of the website.
 
<h3>2. Use an Optimization plugin</h3> 
  
There are a lot of optimization plugins available for WordPress. I would recommend to go for autoptimize as it will minify and compress your styles and scripts and will move the scripts to the footer, styles to header. Also it will minify the HTML code itself making your page really light.
 
 
<h3>3. Use google page speed insights</h3> 
 
Use google page speed insights 
{% highlight ruby %}
  	https://developers.google.com/speed/pagespeed/insights/
{% endhighlight %}
 Google page speed insight is a good friend for finding the reasons that hinders your website speed. It also provides instruction for fixing the issues.


<h3>4. Use this code in the .htaccess file</h3> 

{% highlight ruby %}
	ExpiresActive On
	ExpiresDefault "access plus 1 seconds"
	ExpiresByType text/html "access plus 1 seconds"
	ExpiresByType image/x-icon "access plus 2592000 seconds"
	ExpiresByType image/gif "access plus 2592000 seconds"
	ExpiresByType image/jpeg "access plus 2592000 seconds"
	ExpiresByType image/png "access plus 2592000 seconds"
	ExpiresByType text/css "access plus 604800 seconds"
	ExpiresByType text/javascript "access plus 86400 seconds"
	ExpiresByType application/x-javascript "access plus 86400 seconds"
{% endhighlight %}

Which will set a expiry for your cached files.
You can test its working in google page speed insights.

<h3>5. Optimize your images</h3>

Optimize all the images in your website use this code in your functions.php for generating the images for your required size 

{% highlight ruby %}
// without parameter -> Post Thumbnail (as set by theme using set_post_thumbnail_size())
the_post_thumbnail();

the_post_thumbnail('thumbnail');       // Thumbnail (default 150px x 150px max)
the_post_thumbnail('medium');          // Medium resolution (default 300px x 300px max)
the_post_thumbnail('large');           // Large resolution (default 640px x 640px max)
the_post_thumbnail('full');            // Original image resolution (unmodified)

the_post_thumbnail( array(100,100) );  // Other resolutions
{% endhighlight %}




