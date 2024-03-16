Q.
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

when we are importing this files as cdn links we are importing our react  code into our project.

Q. why there are two files(script tag)? 

first file is react.development.js this is core of react.
second file is this is react library which is useful for DOM operations or this is react DOM which is need to modify DOM.

Q. why react made different files for both of them?

react does not only works on browser ,react also works on mobile and other different places.
so, there are different functions, methods which are used inside react native ,browser that is why there are two files.
here above second script file acts as a bridge between react and DOM.

----
React is built on philosphy that we want to manipulate out DOM with js.

---- 
React element is nothing just a normal js object.
it has something known as props . props are children plus attributes which are passing.
In React.createElement second argument is attributes and  third argument is children .
while element is rendering onto the DOM it converts itself to that HTML  and puts up into the DOM.

--- 
how to write more than one children in react.createElement ?
by writing array of children with key in third argument .


-------
Q: What is crossorigin in script tag?
A: The crossorigin attribute sets the mode of the request to an HTTP CORS Request. The purpose of crossorigin attribute is used to share the resources from one domain to another domain. Basically, it is used to handle the CORS request. It is used to handle the CORS request that checks whether it is safe to allow for sharing the resources from other domains. 