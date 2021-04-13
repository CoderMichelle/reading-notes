how I explained REST to my brother

https://gist.github.com/brookr/5977550

Roy Thomas Fielding (born 1965) is an American computer scientist, one of the principal authors of the HTTP specification and the originator of the Representational State Transfer (REST) architectural style. He is an authority on computer network architecture and co-founded the Apache HTTP Server project.

Representational state transfer (REST) is a de-facto standard for a software architecture of interactive applications that use Web services. A Web service that follows this standard is called RESTful.

In a RESTful Web service, requests made to a resource's URI elicit a response with a payload formatted in HTML, XML, JSON, or some other format.

REST is intended to evoke an image of how a well-designed Web application behaves: it is a network of Web resources (a virtual state-machine) where the user progresses through the application by selecting resource identifiers such as http://www.example.com/articles/21 and resource operations such as GET or POST (application state transitions), resulting in the next resource's representation (the next application state) being transferred to the end user for their use. (wikipedia).

In this article someone explains the basis of REST to a layperson. The analogy is brought up about HTTP addresses - URLS being like nouns - like a webpage has several resources like text, images, video, audio,... and how there is a need for a common language across machines - so they all know what certain nouns mean. He then stretches the analogy further to include verbs. The most universal ones being: GET, PUT, and DELETE.

HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.

Web pages usually have images. Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.

web browsers pretty much just GET stuff. They don't do a lot of other types of interaction with resources. This is a problem because it has led many people to assume that HTTP is just for GETing. But HTTP is actually a general purpose protocol for applying verbs to nouns.

more than just GET http can POST PUT PATCH HTTP provides operations (HTTP methods) GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS and TRACE.(wikipedia)
