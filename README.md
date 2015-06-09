#MEAN Session Two

##Assignment

Recreate the Image Gallery that we created in class using jQuery. Upload it to a Github repo and send me the link.

See http://api.jquery.com for the code explanations.

Step 1 - add the link to jQuery in the ```<head>``` of the HTML file.
```
<script type="text/javascript" charset="utf-8" src="js/jquery-1.4.2.js"></script>
```
Step 2 - Add the document ready function inside the ```<script>``` tags
```
$(document).ready(function() {

});
```
Step 3 - Add a jQuery selector to grab all the anchor tags in the ```#imageGallery``` and disable the default behavior of links using ```return false```. Also try sending the click event to the console.
```
$(document).ready(function() {
	$("#imageGallery a").click(function(){
	  console.log(this);
		return false;
	});
});
```
Step 4 - Create a selector for the ```#placeholder``` and call the attr jQuery function to change the ```src``` attribute to the ```href``` attribute stored in 'this'.
```
$(document).ready(function() {
	$("#imageGallery a").click(function(){
		$("#placeholder").attr("src", this.href);
		return false;
	});
});
```
Step 5 - Create a reference to the ```#desciption``` and call the html jQuery function to set the contents of the paragraph to the title attribute of 'this'.
```
$(document).ready(function() {
	$("#imageGallery a").click(function(){
		$("#placeholder").attr("src", this.href);
		$("#description").html(this.title);
		return false;
	});
});
```
Step 6 - Just for giggles set the alt attribute of the placeholder graphic to the title as well (best practices).
```
$(document).ready(function() {
	$("#imageGallery a").click(function(){
		$("#placeholder").attr("src", this.href);
		$("#description").html(this.title);
		$("#placeholder").attr("alt", this.title);
		return false;
	});
});
```
Step 7 - find and read the ready(), attr(), and html() documentation on http://api.jquery.com. And add a style sheet using the following code as a starting point only (you can add as much CSS as you want and design the page in any way you see fit)
```
body { color:#666; background-color:#ccc; margin:1em 0; }
#wrapper { width:740px; margin:0 auto; }
#head h1 { color:#333; }
#mainNav a { color: #c60; font-weight:bold; text-decoration:none; }
#mainNav ul { padding:0; list-style:none; }
#mainNav li { float:left; padding:1em; }
#mainNav li a img { border:0; }
#mainNav li:first-child { padding-left:0; }
```

##Tools of the trade - continued

Github
* [Github forking](https://help.github.com/articles/fork-a-repo/) 
* [Github commenting](https://help.github.com/articles/markdown-basics/)

Git  
* [Git checkout](http://git-scm.com/docs/git-checkout)
* [Git branch](http://git-scm.com/docs/git-branch)
* [Git push](http://git-scm.com/docs/git-push)
* [Gitup.co](http://gitup.co/) - new new app for OSX that simplifies Git branching

Other
* [Google fonts](https://www.google.com/fonts)
* [SASS features](http://sass-lang.com/guide): nesting, operators and the difference between SASS and SCSS
* Responsive design: breakpoints and images
* CSS pseudo selector: before
* CSS clearfix, sprites and animation 

##Objectives

Understand the basic principles of web development and its evolution. This session will cover:

* The Chrome Web Developer tool
* [Package control](https://packagecontrol.io/) and [Emmet](http://emmet.io/) for [Sublime Text](http://www.sublimetext.com/)
* Git branching and other workflow issues
* CSS structure
* Basic JavaScript DOM manipulation 

##Essentials
```
git config --global user.name "username"
git config --global user.email "you@email.com"
python -m SimpleHTTPServer
```
