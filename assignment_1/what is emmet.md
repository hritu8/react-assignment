what is emmet?
Emmet is a plugin for many popular text editors which greatly improves HTML & CSS workflow.
---------------

Difference between a Library and Framework?

framework is an application and it helps in building a kind of application.ex: for making web application.
library is not a software but framework is a software.
in library already codes are written and we calls them and decide the program flow .
in framework ,we write a code and  framework calls the code and  decide the flow.
framework provides generic fuctionalities and we add-on some features.

ex: express,django,flask.

--------------------------------

What is CDN? Why do we use it?

A CDN, or Content Delivery Network, is a network of geographically distributed servers that work together to deliver internet content to users more efficiently. CDNs store cached copies of content (such as web pages, images, videos, scripts, and other multimedia) in multiple locations around the world, known as points of presence (PoPs). When a user requests content from a website, the CDN serves the content from the nearest PoP rather than from the origin server where the content is hosted. This reduces latency and improves loading times for users, leading to a better overall user experience.

There are several reasons why CDNs are used:

Faster Content Delivery: By serving content from servers located closer to the end-users, CDNs reduce the physical distance that data needs to travel, resulting in faster loading times for web pages and other online content.
Security: Some CDNs offer security features such as DDoS protection, web application firewalls, and SSL encryption.
Scalability: CDNs help websites handle traffic spikes and surges in user demand by distributing the load across multiple servers.
https://www.youtube.com/watch?v=NNqVbVO566Q
----    

Why is React known as React?

React, the JavaScript library for building user interfaces, is known as "React" because of its core concept of reacting to changes in data. When data changes in a React application, the user interface automatically updates to reflect those changes without the need for manual intervention.

--------------------------------
Q: What is crossorigin in script tag?
A: The crossorigin attribute sets the mode of the request to an HTTP CORS Request.
 The purpose of crossorigin attribute is used to share the resources from one domain to another domain. 
 Basically, it is used to handle the CORS request. 
 It is used to handle the CORS request that checks whether it is safe to allow for sharing the resources from other domains.



----------------------------------------------------------------
What is diference between React and ReactDOM?

React is a JavaScript library designed for building user interfaces.
It provides tools and abstractions for creating reusable UI components, managing state, handling lifecycle events, and more.
You use React to define and create your elements, manage component lifecycles, and handle application logic.

ReactDOM is a complementary library to React that glues React to the browser DOM.It handles the rendering of React components in a browser environment.
Specifically, it bridges the gap between React’s virtual representation (React elements) and the actual DOM.ReactDOM.render(): Used for mounting React components into the DOM.

React and ReactDOM were split into two libraries to accommodate platforms like React Native.
React contains functionality for both web and mobile apps, while ReactDOM is specific to web apps.

In summary, React is the core library for creating components, and ReactDOM handles the rendering of those components in the browser environment.

----    

What is difference between react.development.js and react.production.js files via CDN?

react.development.js:
Purpose: This file is intended for development purposes.
Characteristics:
Developer-Friendly: It contains additional code, comments, and debugging information.
Readable: The code remains human-readable, which aids in development and troubleshooting.
Larger Size: Due to the extra information, it tends to be larger in file size.
Hot Module Replacement (HMR): Supports features like HMR for faster development cycles.
Usage:
Use this version during development to take advantage of tools like React Developer Tools and diagnostics.

react.production.js:
Purpose: This file is optimized for production environments.
Characteristics:
Minified and Optimized: It focuses on minimizing file size and improving performance.
No Debugging Information: Strips out comments, whitespace, and unnecessary code.
Efficient Execution: Designed for faster execution in production.
Not Developer-Friendly: Not meant for direct human reading or debugging.
Usage:
Deploy this version to production servers.
It ensures better performance by reducing the payload sent to clients.

----------------------------------------------------------------

What is async and defer?

async and differ are boolean attributes which are used along with script tag to load the external scrpits efficiently into our web page.
 
when we load our web page then two things are happening one is HTML parsing and second is the loading of the scripts.
Loading of the script contains two parts one is the fetching the script from the network and second the actually execution the script line by line.

normal case:
suppose browser is parsing html line by line and suddenly encounter a script tag .
so,browser pause or stops the parsing at that point of time and then sees the script tag and then fetch the script from the network and gets into the browser and runs or execute it then and there .parsing will only continue to start after the script is fully executed .
actually, js are blocking the rendering of HTML.

async case:
meanwhile, the HTML parsing is going on any of script with async tag are fectched from the network asyncronusly along with the HTML parsing .
as soon as the script are fetched and available in the browser the HTML parsing stops and scripts are executing then and there.
and once the execution is completed then HTML parsing continue to starts as regular.
applications: async can be used when :
                                  Third-party scripts arerequired, ex:ads .because we dont mind when the scripts runs(asnychronously).

defer case:
HTML parsing continue to goes on and the script are fetched in parallel and the HTML parsing are continues are goes on and these scripts are only executed after when the HTML parsing are fully completed.
- maintains the relative order of the scripts. 

note:
async attribute doesn't guranteed the order of execution of the scripts but defer does.


when to use what:
suppose if we have multiple scripts which are dependent on each other then using async tag will not gurantee the order of execution and as a result it will break the code.
so,in that case we should use defer.

