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

Please noted that this documentation focused on Apollo Server V2. For other version please consult
The official documentation site. <a href="https://www.apollographql.com/docs/apollo-server/">Apollo Server Docs</a>

The Architecture and Design on Server is flexible and open up
to more than just GraphQL. The Aggregation and Integration is
simple and quick to implement from REST API to Databases.

    ---

    import { ApolloServer } from 'apollo-server-express'
    import { env } from '../config'
    import { contextFireBaseAuth } from '../utils/firebase_utils/authentication'
    import { customMessageError } from '../utils/error_handler'
    import schema from './schema'

        const apolloServer = new ApolloServer({
        schema,
        csrfPrevention: true, 
        context
        })

    await server.start();

    ---

<div class="caption">
    Apollo Server starting code and type definition, resolvers for send and receive API, with context
</div>

For schema We will use the makeExecutable Schema:

---
    import { makeExecutableSchema } from '@graphql-tools/schema'
    import { resolvers, mainSchema } from './resolvers'
    import { gql } from 'apollo-server-express'

    const typeDefs = gql(mainSchema)

    const schema = makeExecutableSchema({
    typeDefs,
    resolvers,
    })

---

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


