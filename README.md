# koa-vhost

Vhost middleware for Koa. Checks subdomains for 

## Example
````js
var vhost = require('koa-vhost');

// check for api.localhost:port in development
// check for api.mysite.com in production
app.use(vhost('api', someMiddleware())); 

// disable localhost support in development
app.use(vhost('api', someMiddleware(), {localhost: false}));

// glob matching (TODO)
app.use(vhost('*.api', someMiddleware()));
````

#### 

## License
[MIT](https://tldrlegal.com/license/mit-license) © [Yoshua Wuyts](yoshuawuyts.com)