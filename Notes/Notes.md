# Namaste React Notes :)

1. React is a library: library take minimum efffort to put it inside our code.

CDN : Content Dilivery Network -> If we need to inject any required library in our project then we can get it through CDN links.
For Example: We are calling CDN links of React library to use React in our Project.

``` js
-> This line tell us the Latest versin of React
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>

-> This line tell us the Web version of React. ( As we already know there are other Version as well like React Native)
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
```
CrossOrigin - ???

2. Creating H1 tag with HTML and JS

``` HTML
<div id="root"> 
    <h1>Namaste EveryOne from HTML</h1>
</div>
```

``` js
<script>
    const heading = document.createElement("h1");
    heading.innerHTML = "Namaste Everyone from JavaScript";
    const root = document.getElementById("root");
    root.appendChild(heading);
</script>
```

3. Creating H1 tag with Pure React ( No JSX used).
``` js
<script>
    const reactHeading = React.createElement("h1",{},"Nmaste EveryOne from React");
    const reactRoot = ReactDOM.createRoot(document.getElementById("root"));
    reactRoot.render(reactHeading)
</script>
```
3 (a) -> what is {} in createElement : This object is use to Pass in attributes to the react elements.
React.createElement("h1",{},"Nmaste EveryOne from React") == <h1>Namaste EveryOne from React</h1>
but we want to put any attributes then.
React.createElement("h1",{id = "title"},"Nmaste EveryOne from React") == <h1 id = "title">Namaste EveryOne from React</h1>

4. if we console(reactHeading) -> createElement: React element is nothing but just plain js object of type h1.

5. Passing a react elemnet inside root : [ reactRoot.render(reactHeading) ]

6. Everytime we have only 1 root in our react project and 1 render method.

7. We can have a Header and footer and even after thatReact can run in between.
``` HTML
<html lang="en">
<head>
    <title>Namaste React</title>
</head>
<body>
    <div>Header</div>
        <div id="root"></div>
    <div>Footer</div>
<script>
    const reactHeading = React.createElement("h1",{},"Nmaste EveryOne from React");
    const reactRoot = ReactDOM.createRoot(document.getElementById("root"));
    reactRoot.render(reactHeading)
</script>
</body>
</html>
```

8. React will override everything inside the Root with whatever passed inside the render method 
``` HTML
<html lang="en">
<body>
    <div id="root">
        <div id="title">1</div>
        <div id="title">1</div>
        <div id="title">1</div>
    </div>
<script>
    const reactHeading = React.createElement("h1",{},"Nmaste EveryOne from React");
    const reactRoot = ReactDOM.createRoot(document.getElementById("root"));
    reactRoot.render(reactHeading)
</script>
</body>
</html>
```
1 1 1 will get override and replace by Nmaste EveryOne from React

