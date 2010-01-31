---
layout: default
title: Home
---

# jQuery Message Slider Plugin
by [Henrik Joreteg](http://joreteg.com)

This plugin provides a cool way to temporarily display messages to the user.

## Demo
<script src="http://github.com/HenrikJoreteg/jquery-sliding-message/raw/master/jquery.slidingmessage.js"></script>
<script>
    $(function() {    
        // on first button click, use all the defaults
        $('#button1').click(function(){
            $.showMessage("This is the default behavior");
            return false;
        });
        
        // this time use ALL the options
        $('#button2').click(function(){
            var options = {id: 'message_from_top',
                           position: 'top',
                           size: 50,
                           backgroundColor: 'rgba(200, 70, 70, 0.8)',
                           delay: 1500,
                           speed: 500,
                           fontSize: '30px'
                          };
                           
            $.showMessage("This is with options!", options);
            return false;
        });
    });
</script>

<button id="button1">See default behavior</button>
<button id="button2">See with options</button>

## Basic Usage
Using it couldn't be simpler:

This almost goes without saying, but make sure you have jQuery and the plugin imported (jQuery first). Something like:


{% highlight html %}
<script src="jquery.js"></script>
<script src="jquery.slidingmessage.js"></script>
{% endhighlight %}


Then you can just call it like this anywhere in your javascript:


{% highlight javascript %}
$.showMessage("message to display");
{% endhighlight %}    


A box with your message will slide into view from the bottom of the page (by default) with your message and will hide itself after a short pause.


## Available options
The following are optional paramaters:

In the following example where we're setting all available options, but you can do as few as you want, or of course, none:


{% highlight javascript %}
var options = {id: 'message_from_top',
               position: 'top',
               size: 50,
               backgroundColor: 'rgba(70, 70, 70, 0.8)',
               delay: 1500,
               speed: 500,
               fontSize: '30px'
              };
               
$.showMessage("This is with options!", options);
{% endhighlight %}


## Additional Styling
Some styles such as font size and height make sense to set in the javascript. But you can set font family or whatever else you want by writing a rule in your CSS to match the sliding box div. By default the div `id` attribute is `sliding_message_box`. But you can set the id to be whatever you want by passing that in through the options.

## Compatibility Note
This plugin uses the CSS property `position: fixed;` in order to support messages from the bottom of the viewport. However, it uses `position: absolute` as a fall-back. So if you have to have support in earlier versions of IE or on an iPhone you can simply set the option to slide in from the top. As long as the user isn't scrolled down it should work just fine.

## License
[BSD License](http://projects.joreteg.com/licenses/BSD.html)

