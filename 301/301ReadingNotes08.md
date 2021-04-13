super agent

https://visionmedia.github.io/superagent/

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

Request basics A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request. For example a simple GET request:

 request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });

HTTP method may also be passed as a string:

request('GET', '/search').then(success, failure);

Old-style callbacks are also supported, but not recommended. Instead of .then() you can call .end():

request('GET', '/search').end(function(err, res){
  if (res.ok) {}
});

Absolute URLs can be used. In web browsers absolute URLs work only if the server implements CORS.

 request
   .get('https://example.com/search')
   .then(res => {

   });

The Node client supports making requests to Unix Domain Sockets:

// pattern: https?+unix://SOCKET_PATH/REQUEST_PATH
//          Use `%2F` as `/` in SOCKET_PATH
try {
  const res = await request
    .get('http+unix://%2Fabsolute%2Fpath%2Fto%2Funix.sock/search');
  // res.body, res.headers, res.status
} catch(err) {
  // err.message, err.response
}

DELETE, HEAD, PATCH, POST, and PUT requests can also be used, simply change the method name:

request
  .head('/favicon.ico')
  .then(res => {

  });

DELETE can be also called as .del() for compatibility with old IE where delete is a reserved word.

The HTTP method defaults to GET, so if you wish, the following is valid:

 request('/search', (err, res) => {

 });
