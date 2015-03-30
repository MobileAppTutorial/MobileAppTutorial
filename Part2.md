Part 1 - An even nicer "Hello to you all"
====================

Introduction
------------
In our last example I showed you how to write one of the most simple mobile apps - but it is also meager as [planet Mars surface](http://marsmobile.jpl.nasa.gov/msl/images/PIA16453_sol64_from_Rocknest_WB-br2.jpg)! So today I will show you how to make the whole app look like a real app and not just like an office posting.


Looking good now
----------------
Thankfully there are libraries that make styling a mobile web page quite easy. I will use the [jQuery Mobile framework](http://jquerymobile.com/) which is tightly bound to the famous *jQuery* javascipt library for easy DOM handling.
*jQuery Mobile* supports *Widgets* like buttons, title bars or lists that can be added by using div-elements that contain special *data*-attributes. Theses data-attributes are only legal for HTML5 documents which explains why our web pages need to be compliant to this standard.
The starting point for every app in *jQuery Mobile* is a *page*, which is exactly what it sounds: one of maybe multiple pages inside one HTML document.To declare a page you add:

    <div data-role="page">
    </div>

to the documents body-tag. Every real app has a title bar that can be added easily, we'll keep it simple and use two smilies as our title text:

    <div data-role="header">
        <h2>☺ ☻</h2>
    </div>

After these two examples it's probably obvious how to add a meaning to the div-elements using *jQuery Mobile* widgets using *data*-attributes.
To add some content, we solve the mystery of the multiple "Hello World" examples and show which language that example is in. Let's use a collapsible, basically an expandable list that shows more additional information after you *click* an item.

    <div data-role="collapsible-set">
    </div>

is the code for the list and every item is styled using the following markup:

     <div data-role="collapsible">
        <h3>Visible item text</h3>
        <p>Hidden item text with additional information</p>
    </div>

Now we should not forget to add the main content which is styled inconsistently with the previous snippets:

    <div class="ui-content" role="main">
    </div>

But beside that exception we can just add the single parts together like LEGO® bricks. You find the complete document in the **Example2**-branch of the repository. Don't forget to add links to the css/js-files otherwise you'll still have an martian experience.


PhoneGap part II
----------------
In the last example I showed you how to use PhoneGap to build your mobile app, but this time we want to configure PhoneGap's build. You can either configure by opening the *settings* tab on the apps page
![Settings tab (first from the right)](Part2/Adobe1.png)
or by adding a **config.xml** file - which is exactly what we are going to do!
I will only discuss some of the preferences I added you can read further about the configuration file in [PhoneGap's documentation](http://docs.build.phonegap.com/en_US/configuring_basics.md.html).

First we want to add a customized icon, let's use a simple [world icon](Part2/earth213.png).

    <icon src="icon.png" />

It's as easy as that, add an image to your root folder and name it accordingly.

########################


Result
------
Again I will leave you with a screen shot from my phone: ![screen shot of running app](Part2/Screenshot1.jpg). Next time we will ad some functionality so your app actually does something.

1) For iPhone users there is a drawback: Unless your are willing to enroll in Apple's Developers Program ($99/yr) can't build your own iPhone apps. This is not a limitation of PhoneGap. Due to Apples developer guidelines every app running on an (not jailbroken) iPhone needs to be signed digitally with a certificate issued only to members of that program. You can enroll with your Apple ID at <https://developer.apple.com/programs/ios>.


Image copyright
---------------
The mars surface is courtesy of NASA/JPL-Caltech ([licence](http://www.jpl.nasa.gov/imagepolicy/)).

The **Grid World** Icon made by [Yannick](http://www.flaticon.com/authors/yannick Yannick) from [www.flaticon.com](http://www.flaticon.com  Flaticon) is licensed by [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/ Creative Commons BY 3.0).
