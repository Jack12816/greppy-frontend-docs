# Controller

The controller is currently only used to generate links.

Simply pass an options object as an argument to it's constructor:

    myController = new greppy.Controller({
        basePath: 'my/path/',
        actions: {
            show: {
                path: 'show/:id'
            }
        }
    });

Now you can generate links with the `link()` method:

    var link = myController.link('restore', {id: 23});

The first parameter names the action, which we are referring to. The second one
is an object containing the desired parameters for our generated url.

The method will automatically recognize the parameter(s) in the path and replace
them with the passed values.

So in our case, `link()` would equal: `my/path/show/23`

