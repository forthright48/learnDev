# Learning Development

While learning development, a beginner needs to cover lots of topics. As a beginner myself, I decided to track the useful resources in one place.

# AngularJS

1. [Why do we use $rootScope.$broadcast in AngularJS?](http://stackoverflow.com/questions/24830679/why-do-we-use-rootscope-broadcast-in-angularjs/24831979#24831979)  
Using $broadcast we can create custom events. Using $rootScope directly is bad practice and we should create custom event handler service.

1. [AngularJS Interceptros for Logging Service Calls](http://intown.biz/2015/02/04/angularjs-interceptors/)  
Short and simple tutorial to adding interceptors to angularJS.

1. [Cookies vs Tokens. Getting auth right with Angular.JS](https://auth0.com/blog/2014/01/07/angularjs-authentication-with-cookies-vs-token/)  
Using express-jwt module to authenticate routes and verifying tokens. Also, it has code on how to attach interceptors to angularjs requests.

1. [AngularJS Best Practices and Tips by Toptal Developers](http://www.toptal.com/angular-js/tips-and-practices)  
How to set watchers, One time binding, making ng-click conditional and more.

1. [Angular Function Declarations, Function Expressions, and Readable Code](http://www.johnpapa.net/angular-function-declarations-function-expressions-and-readable-code/)  
We spend more time reading our code than writing them. Using function declaration approach, we can keep our exposed variables at top and hide implementation below.

1. [Route Resolve and Controller Activate in AngularJS](http://www.johnpapa.net/route-resolve-and-controller-activate-in-angularjs/)  
Where to put the logic that populates variables of controller. Using `activate()` vs route resolve.

1. [$scope vs scope](https://thinkster.io/a-better-way-to-learn-angularjs/scope-vs-scope)  
What's the difference between $scope in controller and scope in link function of directive.

1. [Accessing The View-Model Inside The Link Function When Using Controller-As In AngularJS](http://www.bennadel.com/blog/2896-accessing-the-view-model-inside-the-link-function-when-using-controller-as-in-angularjs.htm)  
How to access controller from link function of directive.

# BootStrap

1. [Vertical Align Columns in Row in BootStrap](http://stackoverflow.com/questions/28077398/twitter-bootstrap-3-vertical-align-columns-in-a-row-middle)  
The code snippet for `v.center` works like a charm.

# Express

1. [Why can I execute code after `res.send`?](http://stackoverflow.com/questions/16180502/node-express-why-can-i-execute-code-after-res-send)  
`res.send()` simply closes the response. The function is free to continue as long as it does not attempt to call methods on `res`. So, better to use `return` where we want things to stop.

# HTML

1. [HTML5 History API ](http://diveintohtml5.info/history.html)  
Changing browser location without refreshing the full page.

# HTTP

1. [Choosing an HTTP Status Code — Stop Making It Hard](http://racksburg.com/choosing-an-http-status-code/)  What should be the http status code for a response?

# JavaScript

1. [Immediately-Invoked Function Expression (IIFE)](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)  
Beautiful explanation on how to use closure to create IIFE along with reasons why it has that particular syntax.

1. [Promise Anti Patterns](http://taoofcode.net/promise-anti-patterns/)  
Lots of anti-patterns for Promise.

1. [How to Encode and Decode Strings with Base64 in JavaScript](https://scotch.io/quick-tips/how-to-encode-and-decode-strings-with-base64-in-javascript)  
Sometimes API sends their content base64 encoded, so decodnig them is necessary.

# JQuery

1. [Automatic Table of Contents](https://css-tricks.com/automatic-table-of-contents/)

# Markdown

1. [Cross-reference (named anchor) in markdown](http://stackoverflow.com/questions/5319754/cross-reference-named-anchor-in-markdown/7335259#7335259)  
How to create table of contents and other cross-reference inside markdown.

# MongoDB

1. [Checking if a document exists – MongoDB slow findOne vs find](https://blog.serverdensity.com/checking-if-a-document-exists-mongodb-slow-findone-vs-find/)  
Using `db.find().limit(1)` is faster than using `db.findOne()`. Oh well, I will still use findOne() since I don't need ultra optimization.

# Node.js

1. [Authenticate a NodeJS API with JSON Web Tokens](https://scotch.io/tutorials/authenticate-a-node-js-api-with-json-web-tokens)  
A simple tutorial that shows how to use jsonwebtoken module to use JWT with API for authentication.

1. [Node.js, Require and Exports](http://openmymind.net/2012/2/3/Node-Require-and-Exports/)  
NodeJS by default isolates codes inside a file from the global space. We need to use `module.exports` explicitly to tell node what we want to share and `require()` to get what we want.

1. [jsonwebtoken doesn't expire](http://stackoverflow.com/questions/28874915/jsonwebtoken-doesnt-expire)  
Dumping user info in an object before signing does the trick.

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

# Testing

1. [Unit testing with Karma and Jasmine for AngularJS](https://blog.logentries.com/2015/01/unit-testing-with-karma-and-jasmine-for-angularjs/)  
A simple tutorial on importance of testing from beginng. Suggested method for testing is to use Karma + Jasmine.

1. [The Difference Between TDD and BDD](https://joshldavis.com/2013/05/27/difference-between-tdd-and-bdd/)  
I thought there would be significant difference. They seem same to me. BDD looks nice since it sounds like normal sentence.

# Tools

## Bower

1. [How to change bower's default components folder?](http://stackoverflow.com/questions/14079833/how-to-change-bowers-default-components-folder)  
Basically, just set `.bowerrc` file.

## Grunt

1. [What is Grunt Wiredep?](http://stephenplusplus.github.io/grunt-wiredep/)  
Install with bower and then running `grunt wiredep` will inject scripts and css into html file.

1. [The HUGE Grunt.js Guide to a Better Frontend Workflow (Part 1: Coding)](https://blog.srcclr.com/huge-grunt-js-guide-better-frontend-workflow/)  
Little notes and codes for common grunt services used.

1. [<%= yeoman.app %> and <%=yeoman.dist %> variables for a gruntfile](http://stackoverflow.com/questions/21420593/yeoman-app-and-yeoman-dist-variables-for-a-gruntfile)  
What are those <%= yeoman.app %> variables inside grunt files?

# Uncategorized

1. [Top 18 Most Common AngularJS Mistakes That Developers Make](http://www.toptal.com/angular-js/top-18-most-common-angularjs-developer-mistakes)  
