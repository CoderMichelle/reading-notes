## NODE JS

    Uses V8 JavaScript Engine

    But adds features like file system API, HTTP library, etc

Basically, Node is a program we can use to execute JavaScript on our computers = a javascript runtime

    It is recommended to use a version manager to be able to install different versions of Node and switch between them.

You can run js files straight from the terminal

(I was able to run the hello.js and index.js from the terminal using Node)

npm

The package manager for javascript

To install a package globally run  npm install -g name-of-package

You can also install packages locally to a project.

What is Node.js used for?

Installing (npm) and running (node) various build tools that are designed to automate the process of developing a modern javascript app.

Node allows us to run javascript on the server

Traditionally:

when you connect to server, like Apache, it spawns a thread to handle server request, and this blocks your code from running until the database loop-up is complete. Must be complete before code can process the result.

With Node:

Event-driven, single threaded.

When new server request comes in, server will start processing it, hits blocking I/O operation, registers callback, before continuing to process the next event. When I/O has finished (another type of event), the server will execute the callback and continue working on the original request --This is called asynchronous, non-blocking behavior.

    Node is good suited for apps that require real time interaction or collaboration - chat sites, apps like CodeShare, screenshare stuff.

    Good for building API's where you're handling lots of requests that are I/O driven

Advantages of Node

    Speed and Scalability

    Use same language (javascript) for front and back end

    Node speaks JSON

PAIR PROGRAMMING & 6 Reasons For it:

    Greater efficiency

    Engaged collaboration

    Learning from new students

    Social skills

    Job interview readiness

    Work environment readiness
