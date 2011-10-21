jQuery Last Tweet
=============

A simple jquery script (in its earliest stages) that retrieves a users latest tweet(s).
See index.html for a simple demo.
MIT License

Options
-------

screen_name: twitter handle (string)
user_id: twitter user id (number)
count: number of tweets to retrieve (number) | default: 1
include_rts: include retweets (boolean) | default: true
exclude_replies: exclude replies (boolean) | default: true
before_tweet: text/html to add before each tweet (string) | default: '<p>'
after_tweet: text/html to add behind each tweet (string) | default: '</p>'
onInit: function called when initiating plugin (function) | default: function() {$element.append('<p class="loading">Loading...</p>');}
onError: function called when request to twitter was erroneous (function) | function(jqXHR, textStatus, errorThrown) {$element.append('<p class="error">An error occured while retrieving tweets</p>');}
onSuccess: function called when request to twitter was successful (function) | function(data, textStatus, jqXHR) {}
onComplete: function called when request (error and success) to twitter is completed (function) | function(jqXHR, textStatus) {$element.find('.loading').remove();}

If both screen_name and user_id are provided the user_id will be used

Props
-------

* jQuery Plugin Boilerplate by Stefan Gabos: http://stefangabos.ro/jquery/jquery-plugin-boilerplate-revisited/
* twitterjs by Remy Sharp: http://code.google.com/p/twitterjs/source/browse/tags/1.13.1/src/twitter.js