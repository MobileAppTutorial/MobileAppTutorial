Writing mobile apps Part 1
==========================

Everything is about going mobile today and so are we. We'll start with the mother of all computer programs: "Hello World". For these of you who are unfamiliar with the concept: To get to know a new programming language or style it has common to introduce a minimal example that just prints the words "Hello World!".

While "writing a mobile app" may sound like a complicated task there is in fact a simple but effective way: PhoneGap/Cordova. The project lets you create a mobile app from a mobile web app, which is what we are going to do right now!
Web apps exploit modern browser technologies like HTML5, CSS3 and ES6 (better known as JavaScript).

Let's write the most simple web app known to mankind:

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset=utf-8 />
        <title>Hello World!</title>
        <style>
            .rtl {
                direction: "rtl";
            }
        </style>
    </head>
    <body>
        <h1 class="rtl">مرحبا بالعالم</h1>
        <h1>你好世界</h1>
        <h1>Hallo Welt</h1>
        <h1>Hello World</h1>
        <h1 class="rtl">שלום עולם</h1>
        <h1>हैलो वर्ल्ड</h1>
        <h1>Hola Mundo</h1>
        <h1>Sawubona Mhlaba!</h1>
    </body>
    </html>

This is it (I used some other languages to let you test the Unicode capabilities of your smart phone). Now you copy that code into your favorite editor, save it under *index.html*. You may peek at it in your preferred browser.

In the next step we create a ZIP file from all components of our app. Currently that is only the index.html file, but don't worry, it will make more sense as soon as we add more source files. On my linux system I can create that file using

    zip ex1 index.html

as I'm in the folder containing the file.
