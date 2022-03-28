# Code 301 Reading Notes 
### 12. Read: 12 -   CRUD

####  source: Kay Ploesser, "Which HTTP Status Code to Use for Every CRUD App" [link](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

1. 100s - the request has been recieved and is now being processed
   200s - the request was a success
   300s - redirection codes, i.e. the requested resource has been moved 
   400s - invalid client requests 
   500s - server error codes, such as too many requests 
2. 202 - the async request met all validation requirements 
3. 308- permanent re-direct 
4. 204 - no content - no data returned to the client 
5. 401 - gone - the resource no longer exists 
6. 403 - forbidden - the client has no permissions to access a resource 

#### source: Web Dev Simplified, "Build A REST API With Node.js, Express, & MongoDB - Quick" [link](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

1. we need to pull our database string out of server.js and put in the .env file because of privacy. 
2. middleware is code that is run after a request has started but before it gets sent to your route 
3. app.use(express.json()) allows the server accept JSON in a request body 
4. in a route, the /:id means request parameter, and you can access it on a request object with request.params.myParamOneEtc 
5. PUT and PATCH difference: PUT updates a whole object in memory, PATCH updates just the part that you pass in 
6. to make a default value in a schema - 

```javascript 
const subscriberSchema = new mongoose.Schema({
  name: {
    type: String, 
    required: true
  }, 
  subscribeDate: {
    type: Date, 
    required: true, 
    default: Date.now
  }
})

module.exports = mongoose.model('Subscriber', subscriberSchema); 
```
7. a 500 error code means error on the server
8. the difference between error codes 200 and 201 - 201 means you have successfully created an object, which is more specific than the general 200 code  


## Things I want to learn more about: 
- connecting a mongo database to a node/express server 
 