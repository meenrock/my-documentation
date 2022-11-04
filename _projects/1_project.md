---
layout: page
title: Backend Microservices
description: Apollo Server can house collections of API within one service for easy deployment and maintenances
img: assets\img\frontend_backend_diagram.svg
importance: 1
category: work
---

Apollo Server is an open-source GraphQL Server Project.
Running on Node.js HTTP Server. In this case Express JS.

The Architecture and Design on Server is flexible and open up
to more than just GraphQL. The Aggregation and Integration is
simple and quick to implement from REST API to Databases.

    ---
    
    const server = new ApolloServer({
    typeDefs,
    resolvers,
    dataSources: () => ({ userAPI, launchAPI }),
    context: () => ({ user: { id: 1, email: 'a@a.a' } }),
    });
    await server.start();

    ---

<div class="caption">
    Apollo Server starting code and type definition, resolvers for send and receive API, with context
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}


