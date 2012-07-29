#RunUO Vendor Search

##Intro

RunUO Vendor Search is a library consisting of C# and Html/Javascript that exposes a webservice on your RunUO server that returns Player Vendor items in json format.
The webservice supports queries including simple + and - operators. Paging is also supported.


##Installation
The directories in the cs folder must be dropped into your Scripts directory. The contents of the web directory will need to included in a location that is available
to your webserver. The webservice + client use JSONP so the client and webservice/server do not have to run on the same domain. 

In vendor-grid.js there is a url property that will need to be updated to match the server url. By default both the client and server are
set to use port 2595. 

The server side port can be modified in HttpServer.cs.

This library includes a minimal Http Server that can support other web services. Other Handlers must extend the Handler class and implement
the abstract methods. Extra Handlers can be added in the ServerStarted method of HttpServer.

