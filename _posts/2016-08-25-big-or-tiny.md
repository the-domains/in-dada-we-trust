---
description: Tiny AdForm API
dateModified: '2016-08-25T16:20:25.433Z'
datePublished: '2016-08-25T17:39:46.146Z'
title: Big or Tiny?
author: []
publisher: {}
via: {}
starred: false
sourcePath: _posts/2016-08-25-big-or-tiny.md
inFeed: true
hasPage: false
inNav: false
_type: MediaObject

---
# Big or Tiny?
![Big or tiny?](https://the-grid-user-content.s3-us-west-2.amazonaws.com/23964010-8323-4851-94fc-0c1aa29b7bc5.jpg)

    // Adform Micro API v0.1 var AdFormMicroAPI = function(caller){ 	try{ 		function merge(a,b){var c={};for(var d in a)c[d]=a[d];for(var d in b)c[d]=b[d];return c}; 		// Turn object into URL search string 		function serialize(a){var b=[];for(var c in a)a.hasOwnProperty(c)&&b.push(encodeURIComponent(c)+"="+encodeURIComponent(a[c]));return b.join("&")}; 		// Create image as a transport method 		function createImage(a){var b=new Image;b.src=a}; 		// Get Random ID 		function getRandomInt(a,b){return Math.floor(Math.random()*(b-a+1))+a}; 		// Get AdForm custom String1 		function getBrowserInfo(){function d(a){var b;if(a)b=a.width+"x"+a.height;else if(!a&&window.java)try{var c=window.java.awt.Toolkit.getDefaultToolkit().getScreenSize();b=c.width+"x"+c.height}catch(a){}return b}var a=window,b=a.screen,c=a.navigator,e=c&&c.language?c.language:c&&c.browserLanguage?c.browserLanguage:"";return (e+"|"+e+"|"+d(b)+"|"+(b?b.colorDepth:""))}; 		// Constants for ADF 		var signals = {	 		 "ord": getRandomInt(10000000000,999999999999), 		 "ADFtpmode" : "2", 		 "loc" : caller || window.location.href, 		 "Set1" : getBrowserInfo() 		}; 	} 	catch(e){} 	// Request server for image 	this.track = function(custom_data){ 		var c = "https://track.adform.net/Serving/TrackPoint/"; 		if(custom_data){signals = merge(signals,custom_data)}else{console.log("AdForm Custom Tracker called with incorrect parameters");return !1;} 		var src = c+"?"+serialize(signals); 		createImage(src); 	} };

Tiny AdForm API

# No mama hu Baba

Chapter II is about philosophy.