---
description: The post-user-registration extensibility point for use with Hooks
---

# Extensibility Point: Post-User Registration&nbsp;<span class="btn btn-primary btn-sm">BETA</span>

For [Database Connections](/connections/database), the `post-user-registration` extensibility point allows you to implement custom actions that execute after a new user registers and is added to the database. Hooks associated with the `post-user-registration` extensibility point execute asynchronously from the actions that are a part of the Auth0 authentication process.

This allows you to implement scenarios including (but not limited to):

* Sending notifications to Slack or via e-mail about the user's new account;
* Creating a new user record in a CRM system.

## Starter Code

```js
module.exports = function (user, context, cb) {
  // Perform any asynchronous actions, e.g. send notification to Slack.
  cb();
};
```

:::panel-warning Response Object
The Post-User Registration extensibility point ignores any response object.
:::
