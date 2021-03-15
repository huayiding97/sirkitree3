# Angular Google Plus Sign-in Button Directive


[Homepage](https://github.com/sirkitree/angular-directive.g-signin)


A good starting place for a Google Plus sign-in button. Specify your client id and you're done. Well, almost. You'll also want to set up a listener for `event:google-plus-signin-success` so you can do something once your users are authenticated.

## Usage
1. Include `google-plus-signin.js`.
2. Add `directive.g+signin` as a dependency to your app.
3. Add `<google-plus-signin clientid="your-client-id">` to your app.
4. Create a listener on your `$scope` for `event:google-plus-signin-success` to detect when your users are authenticated.
5. *Optional:* Listen for `event:google-plus-signin-failure` to handle authentication errors and sign outs.

<!-- uncomment once available
## Bower
Installable via `bower`:

```bash
bower install angular-directive.g+signin
```
-->

## Example

See the [homepage](https://github.com/sirkitree/angular-directive.g-signin) for an example.

```html
<div ng-app="directive.g+signin">
  <google-plus-signin clientid="620125449078"></google-plus-signin>
  <p>^ This is a Google Plus sign-in button</p>
</div>
```

###Handling Signin Callback from Google Plus
You can listen for `event:google-plus-signin-success` and `event:google-plus-signin-failure` and handle them appropriately.

```javascript
  $scope.$on('event:google-plus-signin-success', function (event,authResult) {
    // Send login to server or save into cookie
  });
  $scope.$on('event:google-plus-signin-failure', function (event,authResult) {
    // Auth failure or signout detected
  });
```

## License
♡ CopyHeart 2013 by [Jerad Bitner](http://jeradbitner.com) | Copying is an act of love. Please copy.
