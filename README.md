# ToDoApi
Tutorial: Create a web API with ASP.NET Core

This tutorial teaches the basics of building a web API with ASP.NET Core.

In this tutorial, you learn how to:

    Create a web API project.
    Add a model class and a database context.
    Scaffold a controller with CRUD methods.
    Configure routing, URL paths, and return values.
    Call the web API with Postman.

At the end, you have a web API that can manage "to-do" items stored in a database.

# Problems encountered in the tutorial

## Routing and URL paths
In the TodoItemsController.cs you should change the routing [Route("api/[controller]")] and replace [controller] with [Route("api/[TodoItems]")].
Including the [] is not working which took me a while to figure out. The correct route is: [Route("api/TodoItems")].

## The DTO approach
When implementing the DTO. To verify that you can post and get the Secret field, you need to include that in the controller routing and TodoItemDTO.cs: Secret = todoItem.Secret

![Image of javascript front end](https://github.com/ulfsv/ToDoApi/blob/master/2020-12-17.png)
