# Nodejs

## Init Project

*   Create folder `API`

*   inside `API` folder `npm init` (entry point server.js)

*   Install express `npm install express`

*   Install nodemon `npm install nodemon`

*   Enable ES6 with `  "type": "module"` in package.json

*   Add `"start": "nodemon server.js"` in script parts of package.json

## server.js

*   import express

*   Create instance of express with `const app = express()`

*   Start HTTP server on specified port with

```js
app.listen(port,()=>{
    console.log("Hello World")
})
```

*   `npm start` Hello World should be display in the terminal