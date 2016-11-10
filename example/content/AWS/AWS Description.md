/*
Title: Amazon Web Services
*/

Amazon Web Services (AWS) is a secure cloud services platform, offering compute power, database storage,
content delivery and other functionality to help businesses scale and grow. Explore how millions of customers
are currently leveraging AWS cloud products and solutions to build sophisticated applications with increased
flexibility, scalability and reliability.

Remember you will need to restart the app after changing the template.

## Amazon Elastic Compute (EC2)
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute
capacity in the cloud. It is designed to make web-scale cloud computing easier for developers.
Amazon EC2’s simple web service interface allows you to obtain and configure
capacity with minimal friction. It provides you with complete control of your
computing resources and lets you run on Amazon’s proven computing environment.
Amazon EC2 reduces the time required to obtain and boot new server instances to
minutes, allowing you to quickly scale capacity, both up and down, as your computing
requirements change. Amazon EC2 changes the economics of computing by allowing you to
pay only for capacity that you actually use. Amazon EC2 provides developers the tools to
build failure resilient applications and isolate themselves from common failure scenarios.

It's worth noting that when customising Raneto you should always make your own files rather than customising
the existing Raneto files, so that your changes don't get lost when you
[update Raneto](%base_url%/updates/updating-raneto).

## Template Variables

Below are a list of template variables available to use in their respective templates:

**home.html**

* `config`: Holds an array of values from `config.js`
* `pages`: Structured list of categories and pages (used for navigation)
* `body_class`: Class for the `<body>` tag

**page.html**

* `config`: Holds an array of values from `config.js`
* `pages`: Structured list of categories and pages (used for navigation)
* `body_class`: Class for the `<body>` tag
* `meta`: Holds an array of values taken from the page meta comment block (e.g. `meta.title`)
* `content`: The HTML content of the page
* `last_modified`: The formatted date of the time the file was last modified

**search.html**

* `config`: Holds an array of values from `config.js`
* `pages`: Structured list of categories and pages (used for navigation)
* `body_class`: Class for the `<body>` tag
* `search`: The current search query
* `searchResults`: An array search results

## Array Structure

The `pages` array has a structure similar to the following:

* `slug`: The categoy slug
* `title`: The category title
* `is_index`: True for the top level files (ie not in a category)
* `class`: CSS class
* `sort`: The sort index for this category
* `files[]`: Array of pages in this category
* `slug`: The page slug
* `title`: The page title
* `active`: True if the current page is "active"
* `sort`: The sort index for this page

The `searchResults` array contains items which include:

* `slug`: The page slug
* `title`: The page title
* `body`: The page content
* `excerpt`: The page excerpt
