## Toast Messages

### Enable Toast Messages

For easier usage make sure you assign the coreCommand instance in the consturctor of your plugin:

```javascript
module.exports = ExamplePlugin;
function ExamplePlugin(context) {
  var self = this;
  self.context = context;
  self.commandRouter = this.context.coreCommand;
}
```

### Create Toast Message

At any place in your code you can then call the `commandRouter.pushToastMessage` method to show a toast messages to the user:

```javascript
self.commandRouter.pushToastMessage('success', "Account Login", "Login was successful");
```

There are four kinds of toast messages: `info`, `success`, `warning` and `error`:

```javascript
self.commandRouter.pushToastMessage('info', "Account Login", "Login pending....");
self.commandRouter.pushToastMessage('success', "Account Login", "Login was successful");
self.commandRouter.pushToastMessage('warning', "Account Login", "Login not possible");
self.commandRouter.pushToastMessage('error', "Account Login", "Login failed - invalid credentials");
```
