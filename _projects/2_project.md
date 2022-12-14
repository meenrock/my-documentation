---
layout: page
title: EDI Generator
description: Electronic Document Interchange using .NET to Transfer PO or Other business document
img: assets/img/PO-sections.jpg
importance: 2
category: work
---

EDI is the system that facilitates the communication between to business.
For transfer business document eg. Purchase Order (PO), Invoice
without involving paper based method

The Dot Net Framework was ultimately chosen for the project because of existed Infrastructure
and company experience with Microsoft Dot Net Products. Microsoft IIS 10.0 was chosen to be
Hosting Service. Despite no scalibility or security advantage. But being the in-house services.
The potential problem was surpassed by the benefit of software familiarity.

The web application is arranged in MVC Architectures. Model (db), View (pages), Controller (backend).

The Model use for accessing database via EntityFramework, which is written in repository pattern:

    ---
    using System;
    using System.Collections.Generic;

    namespace ExampleApps.Models
    {
        public class User
        {
            public int Id { get; set; }
            public string LastName { get; set; }
            public string FirstName { get; set; }
            public DateTime CreatedDate { get; set; }

        }
    }
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The overall apperance for the EDI Generator Web Application using Microsoft Entity Framework to connect with
    SQL Server and ODBC Drivers for IBM AS400 Database storing Banking and Company Stocks of Inventory Information.
</div>

The View pages with C# HTML Language for rendering pages:

    ---
        @{
            ViewBag.Title = "Home Page";
        }

        <div class="container">
            <h1>Nav Users</h1>
        </div>
        <div class="row">
            <div class="col-md-4">
                @Html.ActionLink("University", "Index", "Home", new { area = "" }, new { @class = "navbar-brand" })
                <div class="nav-collapse collapse">
                    <ul class="nav">
                        <li>@Html.ActionLink("Home", "Index", "Home")</li>
                        <li>@Html.ActionLink("About", "About", "Home")</li>
                        <li>@Html.ActionLink("Users", "Index", "User")</li>
                    </ul>
            </div>
        </div>

    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
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
