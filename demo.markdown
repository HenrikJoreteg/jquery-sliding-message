---
layout: default
title: jQuery Sliding Message Plugin Demo
---

<script src="jquery.slidingmessage.js"></script>
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
                           backgroundColor: 'rgba(70, 70, 70, 0.8)',
                           delay: 1500,
                           speed: 500,
                           fontSize: '30px'
                          };
                           
            $.showMessage("This is with options!", options);
            return false;
        });
    });
</script>

# Sliding Message Plugin Demo

<button id="button1">See default behavior</button>
<button id="button2">See with options</button>
