# Namaste React Notes :)

1. React is a library: library take minimum efffort to put it inside our code.

[H.W] 
Read about Emmet ??? (used by VS Code)
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

``` html
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