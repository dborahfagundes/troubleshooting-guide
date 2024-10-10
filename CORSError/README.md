# Projeto - Soluções Comuns para Problemas Web

## CORS Error 🌐

### The Problem ❌
Cross-Origin Resource Sharing (CORS) issues occur when a web application makes requests to a different domain (or origin) than the one the application was served from. This can happen when a frontend tries to communicate with an external API or a server hosted on another domain. By default, browsers block these types of requests for security reasons, unless the server explicitly allows cross-origin requests through the proper CORS headers.

### Why It Happens 🔍
Browsers enforce CORS policies to protect users from malicious websites attempting to interact with servers that are not configured to accept requests from outside sources. Without CORS, a malicious site could abuse a user's credentials to make unauthorized requests to other servers.

### Solution ✅
To resolve this, the server must include specific HTTP headers that allow browsers to make cross-origin requests. In a Node.js application using Express, you can use the `cors` middleware to simplify the configuration of these headers. This middleware allows you to control which origins, HTTP methods, and headers are permitted in the requests, ensuring the application communicates securely while avoiding the CORS error.

#### Example Implementation 🛠️

##### CORS Middleware in Express.js

```javascript
const cors = require('cors');

app.use(cors({
  origin: 'http://example.com',
  methods: 'GET', 'POST',
  allowedHeaders: 'Content-Type', 'Authorization',
}));


app.use(cors());
