/*
Title: Amazon Web Services
*/

Amazon Web Services (AWS) is a secure cloud services platform, offering compute power, database storage,
content delivery and other functionality to help businesses scale and grow. Explore how millions of customers
are currently leveraging AWS cloud products and solutions to build sophisticated applications with increased
flexibility, scalability and reliability.

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


## Amazon Simple Storage Service (Amazon S3)
Amazon Simple Storage Service (Amazon S3), provides developers and IT teams with secure,
durable, highly-scalable cloud storage. Amazon S3 is easy to use object storage, with a
simple web service interface to store and retrieve any amount of data from anywhere on
the web. With Amazon S3, you pay only for the storage you actually use. There is no
minimum fee and no setup cost.

Amazon S3 offers a range of storage classes designed for
different use cases including Amazon S3 Standard for general-purpose storage of
frequently accessed data, Amazon S3 Standard - Infrequent Access (Standard - IA) for
long-lived, but less frequently accessed data, and Amazon Glacier for long-term archive.
Amazon S3 also offers configurable lifecycle policies for managing your data throughout
its lifecycle. Once a policy is set, your data will automatically migrate to the most
appropriate storage class without any changes to your applications.

Amazon S3 can be used alone or together with other AWS services such as
Amazon Elastic Compute Cloud (Amazon EC2) and AWS Identity and Access Management (IAM),
as well as cloud data migration services and gateways for initial or ongoing data
ingestion. Amazon S3 provides cost-effective object storage for a wide variety of use
cases including backup and recovery, nearline archive, big data analytics, disaster
recovery, cloud applications, and content distribution.

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
