# angularjs-login (Angular 1.6)
Techniques for authentication in AngularJS applications


## What is OAuth?
```
OAuth is an open protocol to allow secure authorization in a simple and standard method from web, mobile, 
and desktop applications. As an application developer, services that provide HTTP APIs supporting OAuth, 
let you access parts of their service on behalf of your users. For example, when accessing a social network 
site, if your user gives you permission to access his account, you might be able to import pictures, friends 
lists, or contact information to your application.
```

```HTML
<html>
    <head>
        <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.27/angular.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/angular-ui-router/0.2.13/angular-ui-router.min.js"></script>
        <script src="js/app.js"></script>
    </head>
    <body ng-app="example">
        <div ui-view></div>
    </body>
</html>
```

This tutorial focuses on using OAuth to implement Sign-In through the following providers: Facebook, Google+, LinkedIn, and Twitter. These providers use either OAuth1.0a (LinkedIn, Twitter) or OAuth2.0 (Facebook, Google+).

To use OAuth, you first have to register an application with that provider. The application will be assigned credentials, needed when performing the OAuth flow.
