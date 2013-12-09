#Chrome DevTools Tips I wish I had known when I began my journey as a web developer
  
<br>

Learning how to use the Google Chrome dev tools marked the inflection point in my journey towards becoming a web developer. When I started learning web development, I had heard vague rumblings of these tools, but didn't put in too much time researching them, as I believed it was more important to first learn the "basics." What is the DOM? How does it relate to HTML? How does CSS style an HTML element? And how does Javascript fit into all of this? I regret to report that I spent a lot of time reading through w3schools articles. 

I don't think it's an exaggeration to say that if I had just dove right in and started learning and playing with the dev tools, I would have learned so much more about all of these topics, and in a much more powerful, experiential way to boot.
The dev tools don't just *tell* you how the DOM works, they *show* you.

For today's post, I'd like to walk you through some of the tips I learned after having used dev tools for a while that I'd wish I'd been shown on day one.

First, we have the "Toggle Element State" feature. This is an incredibly helpful feature which allows you to force the state of a particular element. For example, let's says your style sheet contains the following rule:

    .magical:hover{
      color: red;
      outline:  ridge thick violet;
    }

What if we want to see how elements with the magical class behave when we hover over them, but also want to interact with dev tool's incredibly useful representation of the element's box model at the bottom of the "elements" panel? Well, normally we would lose the hover state styling when we move our mouse off the element, but with the dev tools, we can simply right click on the element, and select ":hover" from the "Force Element State" drop down menu.

![Hover](http://i.imgur.com/UZxJ2t7.png)

The diversity of devices to develop for has proliferated profusely over the last decade. Thankfully, in the Canary build, Dev Tool's Screen Emulation feature provides an effective way to test your website on multiple screens wihout needing to continuously move from device to device. Even cooler, the emulator contains a number of common device presets, which will automatically enable the following settings:
   + **User agent**
   + **Screen Resolution**
   + **Device Pixel Ratio**
   + **Emulate Viewport**
   + **Text Autosizing**
   + **Touch Screen**
 
A [brand new feature](https://plus.google.com/u/0/+FrancoisBeaufort/posts/MxybHsjLjU6?cfem=1), currently only available in Google's cuttng edge browser, Chrome Canary, can also emulate touch events, which is incredibly useful to avoid needing to push out code to a server and then load the new site on the device every time you make a change. To enable support for this feature:
  1. Open the emulation panel in the DevTools
  2. Enable "Emulate touch screen" in the Sensors pane.

Now the relevant touch events: `touchstart`, `touchmove`, and `touchend`, will now be triggered by your mouse action!

![Touch](https://developers.google.com/chrome-developer-tools/docs/mobile-emulation/viewport-emulation.gif)

One of my favorite features, hands-down, is the FPS Counter/HUD Display tool, which is fantastic for being able to measure in real-time how your site is performing. You can enable this by navigating to the Settings Menu and checking "Show FPS meter" You will then see the following display appear in the top-right corner of your page. This is especially great if you are working on a an app which involves a lot of user-interaction- you can see what actions slow the page down as the user peforms them, instead of having to switch back and forth with the Timeline view.

![FPS](https://developers.google.com/chrome-developer-tools/docs/tips-and-tricks/image_8.png)

I hope you enjoyed the Chrome Dev Tool Tips we covered in this post. There are so many more amazing ones out there- Google itself has an [extensive list](https://developers.google.com/chrome-developer-tools/docs/tips-and-tricks). Happy Hacking, and may the Chrome DevTools work forever in your favor!







