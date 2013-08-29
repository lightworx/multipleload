Multipleload for jQuery
=======================

The plugin multipleload get one or more DOM node(s) from specified url, to replace the specified container objects.


Requirements
------------

- [jQuery 1.5.x or higher]



Configure
---------
 The first step, multipleload will to set a hidden div as a temporary container, if it does not exist.
 and the temporary container id defaults to '#filter_temp_container', just like the following:
 
 	<div id="filter_temp_container" style="display:none;"></div>
 as you can see, the attribute style value is "display:none;", means that's a hidden container,
 and you may need to redefine the container id,(e.g. may current id have naming conflicts with others).
 you should specify in the $.multipleLoad.load(), just like the following:

 @example:

	$.multipleLoad.load({container:'#another_filter_temp_container'}); // redefine a new temporary container.
 
 And the second step, we should to define the selector, the selector defined which nodes is we needed.
 you can specify one or more node(s), when you set multiple nodes, then it should use the separator ',' comma to separate every node.
 
 @example:
	 
	 $.multipleLoad.load({selector:"#main,#header"});
 
 And the next, to set the web page url.
 
 @example:
	 
	 $.multipleLoad.load({url:"/"});
 
 The final step, to set the replaceObjects, if the replaceObjects have no defined, 
 that will be replace the default selector, if it is exist.

 The following code is a complete example:
 @example:
	 
	 var replaceObjects = Array("#main","#header");
	 $.multipleLoad.load({url:'/the_page_url',container:'#another_filter_temp_container',replaceObjects:replaceObjects,selector:"#main,#header"});


Copyright
---------
Copyright (c) 2011 - 2012, Stephen Lee <stephen.lee@lightworxproject.com>



License
-------
MultipleLoad is open source software released under the terms of the MIT License.
