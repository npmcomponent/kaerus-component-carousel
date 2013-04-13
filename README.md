carousel
========

Simple carousel

Usage
=====
```html
<!doctype html>
<html>
<head>
	<title>Carousel test</title>
</head>
<body>
	<div id="carousel">
		<div>Hello</div>
		<div>World!</div>
		<div>You can slide anything you like</div>
		<div>in almost any html container</div>
		<div>and transition it as you want</div>
		<div>by defining only html and css.</div>
	</div>
	<style type="text/css">
		/* style the banner slide */
		#banner {
		    position: relative;
		    overflow: hidden;
		    padding: 0;
		    margin: 0;
		}

		.banner {
		    position: relative;
		    display: none;
		    width: 100%;
		    height: 100%;
		    top: 0;
		    left: 0;
		    list-style-type: none;
		    padding: 0;
		    margin: 0;
		}  

		.banner-show,
		.banner-next,
		.banner-prev {
		    display: block;
		}

		.banner-next,
		.banner-prev {
		    position: absolute;
		}

		/* add transitions */
		.banner-show, .banner-prev {
	    	transition: .4s all ease;
    		-webkit-transition: 2s all ease;
    		-moz-transition: 2s all ease;
    		-o-transition: 2s all ease;
    	}

		/* next slide from left */
		.banner-next {
    		left: -100%;
		}

		/* previous slide to right */
		.banner-prev {
    		left: 100%;
		}	

	</style>
	<script src="../build/build.js"></script>
	<script>
		var carousel = require('carousel');
		
		var container = document.getElementById('banner');
		new carousel(container,'banner').start();

	</script>
</body>
</html>
```

