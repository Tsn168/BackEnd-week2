# Exercise 1

**Q1** - The error message that I see in the terminal is `TypeError: res.endd is not a funtion`. This is caused by the `return res.endd();`line.

**Q2** - The purpose of `res.write()`is to send chunk of the respond body to the client. And the purpose of using `res.end()`is the signal that the respond is finished and should be sent to client.

**Q3** - When the `res.end()` is not called at all, The client will keep waiting for a response. The request hangs and the connection doesn't close.

**Q4** - The reason that we use `http.createServer()` instead of just calling a function directly because `http.createServer()` create an actual HTTP server that listens for and handles incoming HTTP requests.

**Q5** - The server be made resilient to such errors during development by:
`+ Use a linter like ESLint to catch typos.`

`+ Use try-catch blocks where needed.`

`+ Use TypeScript for type checking Add logging for easier debugging.`

`+ Use a tool like Nodemon for automatic restarts and error tracking during development.`

# Exercise 2

**Q1** - When I visit a URL that doesn't match any of the three defined, the server returns 404 not found.

**Q2** - Because the same URL can behave differently depending on the method (GET, POST, etc.).

**Q3** - I woule set `Content-Type: text/html`. This tells the browser to render the response as HTML.

**Q4** - As the number of routes increases, the code becomes cluttered with nested if/else statements, making it:

-Harder to read and debug

-Prone to mistakes

-Difficult to maintain or extend

**Q5** - The benefits of framework offer to simplify this logic can: 

-Handle routing more cleanly with app.get(), app.post(), etc.

-Provide middleware support

-Offer better error handling

-Help manage templates, static files, and more

-Improve scalability and developer productivity

# Exercise 3

**Q1** - Because POST data arrives in `chunks`.

`-data: triggered when a chunk of data is received.`

`-end: triggered when all data has been received.`

**Q2** - If we didn't buffer the body correctly, We would only receive part of the data or corrupted input.
Without proper buffering, we might:

-Miss parts of the submission

-Get incomplete or malformed data

-Cause parsing errors or incorrect behavior

**Q3** -By default:

`application/x-www-form-urlencoded: Data is URL-encoded like: name=Somnang&email=test@example.com`

-If the form includes a file upload:

`multipart/form-data: Data is separated by boundaries with binary/form content.`

**Q4** - The reason that we use `fs.appendFile` instead of `fs.writeFile` because We use `appendFile` to keep a record of each submission without deleting previous ones.

**Q5** - To make this improved or more secured we should: 

`-Validate and sanitize input to prevent injections.`

`-Use HTTPS to secure data in transit.`

`-Limit the size of incoming POST data to prevent DoS.`

`-Store data in a database with access controls instead of a plain .txt file.`

`-Add error handling (try/catch or callbacks) for file operations.`