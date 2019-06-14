# Node Basic Server

- create a package.json file: `npm init`

## Basic server
- create a `server.js` file 
    - import the http module
        ```javascipt
        const http = require('http')
        ```
    - create an http server and listen on a port
        ```javascript
        http.createServer().listen(8080, () => console.log('listening'))
        ```
- start the server
    ```
    $ npm start
    ```

## Server Using the Response Object
```javascript
const server = http.createServer((req, res) => {  
    res.statusCode = 200  
    res.setHeader('Content-Type', 'text/plain')  
    res.end('Hello there\n')
})
server.listen(3000, () => console.log('running'))
```
- `res.statusCode = 200` indicates a successful response
- `res.setHeader('Content-Type', 'text/plain')` sets the type of content
- `res.end('Hello there\n')` closes the response and adds content

## Frameworks and Tools
- Express
- Koa
- Next.js
- Micro
- Socket.io

## Resources
- https://www.freecodecamp.org/news/the-definitive-node-js-handbook-6912378afc6e/