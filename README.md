# angularjs-login (Angular 1.6)
Techniques for authentication in AngularJS applications

A collection of ideas for authentication & access control

## Authentication
The most common form of authentication is logging in with a username (or email address) and password. This means implementing a login form where users can enter their credentials. Such a form could look like this:

```HTML
<form name="loginForm" ng-controller="LoginController"
      ng-submit="login(credentials)" novalidate>
  <label for="username">Username:</label>
  <input type="text" id="username"
         ng-model="credentials.username">
  <label for="password">Password:</label>
  <input type="password" id="password"
         ng-model="credentials.password">
  <button type="submit">Login</button>
</form>
```
(Note: there’s an extended version below, this is just a simple example)

Since this is an Angular-powered form, we use the ngSubmit directive to trigger a scope function on submit. Note that we’re passing the credentials as an argument rather than relying on $scope.credentials, this makes the function easier to unit-test and avoids coupling between the function and it’s surrounding scope. The corresponding controller could look like this:

```Javascript
.controller('LoginController', function ($scope, $rootScope, AUTH_EVENTS, AuthService) {
  $scope.credentials = {
    username: '',
    password: ''
  };
  $scope.login = function (credentials) {
    AuthService.login(credentials).then(function (user) {
      $rootScope.$broadcast(AUTH_EVENTS.loginSuccess);
      $scope.setCurrentUser(user);
    }, function () {
      $rootScope.$broadcast(AUTH_EVENTS.loginFailed);
    });
  };
})
```
The first thing to notice is the absence of any real logic. This was done deliberately so to decouple the form from the actual authentication logic. It’s usually a good idea to abstract away as much logic as possible from your controllers, by putting that stuff in services. `AngularJS controllers should only manage the $scope object (by watching and manipulating) and not do any heavy lifting.`




This tutorial focuses on using OAuth to implement Sign-In through the following providers: Facebook, Google+, LinkedIn, and Twitter. These providers use either OAuth1.0a (LinkedIn, Twitter) or OAuth2.0 (Facebook, Google+).

To use OAuth, you first have to register an application with that provider. The application will be assigned credentials, needed when performing the OAuth flow.
