# ToDoApi

I have built a basic a web API with ASP.NET Core 3.1.

I have learned how to:

    Create a web API project.
    Add a model class and a database context.
    Scaffold a controller with CRUD methods.
    Configure routing, URL paths, and return values.
    Call the web API with Postman.

The web API can manage "to-do" items stored in a database.

# Problems encountered

## Routing and URL paths

The ![web api tutorial](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio) mentioned that
the routing in the TodoItemsController.cs should be changed. In the route [Route("api/[controller]")] replace [controller] with [Route("api/[TodoItems]")].
Including the [] is not working which took me a while to figure out. The correct route is: [Route("api/TodoItems")].

## The DTO approach
When implementing the DTO. To verify that you can post and get the Secret field, you need to include that in the controller routing and TodoItemDTO.cs: Secret = todoItem.Secret

# Call an ASP.NET Core web API with JavaScript

In this section, you'll add an HTML page containing forms for creating and managing to-do items. Event handlers are attached to elements on the page. The event handlers result in HTTP requests to the web API's action methods. The Fetch API's fetch function initiates each HTTP request.

I added the wwwroot folder, index.html, site.js and site.css. Configured the Startup.cs to show static files and enabled default file mapping.

![Image of javascript front end](https://github.com/ulfsv/ToDoApi/blob/master/2020-12-17.png)


