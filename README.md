# Learning Development

While learning development, a beginner needs to cover lots of topics. As a beginner myself, I decided to track the useful resources in one place.

# AngularJS

1. [Why do we use $rootScope.$broadcast in AngularJS?](http://stackoverflow.com/questions/24830679/why-do-we-use-rootscope-broadcast-in-angularjs/24831979#24831979)  
Using $broadcast we can create custom events. Using $rootScope directly is bad practice and we should create custom event handler service.

1. [AngularJS Interceptros for Logging Service Calls](http://intown.biz/2015/02/04/angularjs-interceptors/)  
Short and simple tutorial to adding interceptors to angularJS.

1. [Cookies vs Tokens. Getting auth right with Angular.JS](https://auth0.com/blog/2014/01/07/angularjs-authentication-with-cookies-vs-token/)  
Learned about using express-jwt module to authenticate routes and verifying tokens. Also, it has code on how to attach interceptors to angularjs requests.

# BootStrap

1. [Vertical Align Columns in Row in BootStrap](http://stackoverflow.com/questions/28077398/twitter-bootstrap-3-vertical-align-columns-in-a-row-middle)  
The code snippet for `v.center` works like a charm.

# Express

1. [Why can I execute code after `res.send`?](http://stackoverflow.com/questions/16180502/node-express-why-can-i-execute-code-after-res-send)  
`res.send()` simply closes the response. The function is free to continue as long as it does not attempt to call methods on `res`. So, better to use `return` where we want things to stop.

#JavaScript

1. [Immediately-Invoked Function Expression (IIFE)](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)  
Beautiful explanation on how to use closure to create IIFE along with reasons why it has that particular syntax.

1. [Promise Anti Patterns](http://taoofcode.net/promise-anti-patterns/)  
Lots of anti-patterns for Promise.

# MongoDB

1. [Checking if a document exists – MongoDB slow findOne vs find](https://blog.serverdensity.com/checking-if-a-document-exists-mongodb-slow-findone-vs-find/)  
Using `db.find().limit(1)` is faster than using `db.findOne()`. Oh well, I will still use findOne() since I don't need ultra optimization.

# Node.js

1. [Authenticate a NodeJS API with JSON Web Tokens](https://scotch.io/tutorials/authenticate-a-node-js-api-with-json-web-tokens)  
A simple tutorial that shows how to use jsonwebtoken module to use JWT with API for authentication.


# Security

1. [How to Safely Store a Password](http://codahale.com/how-to-safely-store-a-password/)  
Emphasis on use of **bcrypt** for encrypting password. Using MD5, SH1 and others is not safe as they are fast and can be broken using brute force. bcrypt is safe cause it's slow.

1. [What are rainbow tables and how are they used?](http://security.stackexchange.com/questions/379/what-are-rainbow-tables-and-how-are-they-used)  
  Seems like there is a difference between Rainbow attack and Dictionary attack

1. [Why is using salt more secure?](http://security.stackexchange.com/questions/14025/why-is-using-salt-more-secure)  
Salt does not protect a single password. All it does, in case of leak of password database, is make it harder to use dictionary attack and crack multiple passwords in one go.

1. [Stealing JWT from authenticated user](https://ask.auth0.com/t/stealing-jwt-from-authenticated-user/352)  
What happens if someone steals JWT from browser and uses from someother place?

1. [Invalidating JSON Web Tokens](http://stackoverflow.com/questions/21978658/invalidating-json-web-tokens/23089839#23089839)  
How to invalidate a JWT once user logs out. Some tips on logging out users safely. Keeping JWT expiry time short and regularly updating the token sounds good to me.
