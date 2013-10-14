# Application

The application class offers the following methods:

## dialog(body, options, buttons)

Example usage:

```JS
greppy.app.dialog(
  'Logout every user?',
  {
    ok: function(callback) {
      logoutAllUsers();
      callback && callback();
    }
  }
);
```

Here, we provide only two paramerters: The body of the modal and an option for
the "ok"-button.

This basically says: If the user clicks the "ok"-button, call the function
we provided. The provided function's main purpose is to call the
"logoutAllUsers" function. But we also need to take and call the callback, so
the modal internals work.

We could also extend the second parameter to provide a function for the
"cancel"-button:

```JS
greppy.app.dialog(
  'Logout every user?',
  {
    ok: function(callback) {
      logoutAllUsers();
      callback && callback();
    },
    cancel: function(callback) {
      goBack();
      callback && callback();
    }
  }
);
```

So now, if the user clicks "cancel", our "goBack"-method will be called.


