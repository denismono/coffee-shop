<!-- AUTO-GENERATED-CONTENT:START (STARTER) -->
<p align="center">
  <a href="https://www.gatsbyjs.org">
    <img alt="Gatsby" src="https://www.gatsbyjs.org/monogram.svg" width="60" />
  </a>
</p>
<h1 align="center">
  Gatsby's hello-world starter
</h1>

Kick off your project with this hello-world boilerplate. This starter ships with the main Gatsby configuration files you might need to get up and running blazing fast with the blazing fast app generator for React.

_Have another more specific idea? You may want to check out our vibrant collection of [official and community-created starters](https://www.gatsbyjs.org/docs/gatsby-starters/)._

## 🚀 Quick start

1.  **Create a Gatsby site.**

    Use the Gatsby CLI to create a new site, specifying the hello-world starter.

    ```shell
    # create a new Gatsby site using the hello-world starter
    gatsby new my-hello-world-starter https://github.com/gatsbyjs/gatsby-starter-hello-world
    ```

1.  **Start developing.**

    Navigate into your new site’s directory and start it up.

    ```shell
    cd my-hello-world-starter/
    gatsby develop
    ```

1.  **Open the source code and start editing!**

    Your site is now running at `http://localhost:8000`!

    _Note: You'll also see a second link: _`http://localhost:8000/___graphql`_. This is a tool you can use to experiment with querying your data. Learn more about using this tool in the [Gatsby tutorial](https://www.gatsbyjs.org/tutorial/part-five/#introducing-graphiql)._

    Open the `my-hello-world-starter` directory in your code editor of choice and edit `src/pages/index.js`. Save your changes and the browser will update in real time!

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in a Gatsby project.

    .
    ├── node_modules
    ├── src
    ├── .gitignore
    ├── .prettierrc
    ├── gatsby-browser.js
    ├── gatsby-config.js
    ├── gatsby-node.js
    ├── gatsby-ssr.js
    ├── LICENSE
    ├── package-lock.json
    ├── package.json
    └── README.md

1.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

2.  **`/src`**: This directory will contain all of the code related to what you will see on the front-end of your site (what you see in the browser) such as your site header or a page template. `src` is a convention for “source code”.

3.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

4.  **`.prettierrc`**: This is a configuration file for [Prettier](https://prettier.io/). Prettier is a tool to help keep the formatting of your code consistent.

5.  **`gatsby-browser.js`**: This file is where Gatsby expects to find any usage of the [Gatsby browser APIs](https://www.gatsbyjs.org/docs/browser-apis/) (if any). These allow customization/extension of default Gatsby settings affecting the browser.

6.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. (Check out the [config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

7.  **`gatsby-node.js`**: This file is where Gatsby expects to find any usage of the [Gatsby Node APIs](https://www.gatsbyjs.org/docs/node-apis/) (if any). These allow customization/extension of default Gatsby settings affecting pieces of the site build process.

8.  **`gatsby-ssr.js`**: This file is where Gatsby expects to find any usage of the [Gatsby server-side rendering APIs](https://www.gatsbyjs.org/docs/ssr-apis/) (if any). These allow customization of default Gatsby settings affecting server-side rendering.

9.  **`LICENSE`**: Gatsby is licensed under the MIT license.

10. **`package-lock.json`** (See `package.json` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(You won’t change this file directly).**

11. **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

12. **`README.md`**: A text file containing useful reference information about your project.

## 🎓 Learning Gatsby

Looking for more guidance? Full documentation for Gatsby lives [on the website](https://www.gatsbyjs.org/). Here are some places to start:

- **For most developers, we recommend starting with our [in-depth tutorial for creating a site with Gatsby](https://www.gatsbyjs.org/tutorial/).** It starts with zero assumptions about your level of ability and walks through every step of the process.

- **To dive straight into code samples, head [to our documentation](https://www.gatsbyjs.org/docs/).** In particular, check out the _Guides_, _API Reference_, and _Advanced Tutorials_ sections in the sidebar.

## 💫 Deploy

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gatsbyjs/gatsby-starter-hello-world)

[![Deploy with ZEIT Now](https://zeit.co/button)](https://zeit.co/import/project?template=https://github.com/gatsbyjs/gatsby-starter-hello-world)

<!-- AUTO-GENERATED-CONTENT:END -->

This project is created from the template at https://github.com/joeattardi/coffee-shop-starter via Use this templat eoption in Github
gatsby develop

Set up a new site in Netlify
Chanhe the site time in Site settings, Site details-site information

npm install netlify-cms-app@2.12.15 gatsby-plugin-netlify-cms@4.3.5

Change the config.yml in static/admin

Add this to gatsby-config.js
plugins: [
'gatsby-plugin-netlify-cms'
]

Configure Netlify Identity and Git Gateway (page 51)

npm install gatsby-source-filesystem@2.3.14

Change gatsby-config.js (page 72)

plugins: [
'gatsby-plugin-netlify-cms',
{
resolve: 'gatsby-source-filesystem',
options: {
name: 'blog',
path: 'src/blog'
}
}
]

npm install gatsby-transformer-remark@2.8.19 (page 72)

plugins: [
'gatsby-plugin-netlify-cms',
{
resolve: 'gatsby-source-filesystem',
options: {
name: 'blog',
path: 'src/blog'
}
},
'gatsby-transformer-remark'
]

Implement blog post component
implement blog list component
Add gatsby-node.js

handle onCreateNode to create blog pages to add slug field
Create blog page template in src/templates
Implement createPages in gatsby-node.js

Add pagination (page 100)

Add support for other content types in the config.yml via contentKey (page 114)

Add another filesystem source for sourcing page data (page 126)

{
resolve: "gatsby-source-filesystem",
options: {
name: "pageData",
path: "src/pageData",
},
}

Add support for images
npm install gatsby-plugin-sharp@2.6.17 gatsby-transformer-sharp@2.5.10 gatsby-remark-relative-images@0.3.0 gatsby-remark-images@3.3.17 gatsby-background-image@1.1.1

gatsby-config

{
resolve: "gatsby-source-filesystem",
options: {
name: "images",
path: "static/img",
},
},

    ...

    {
      resolve: "gatsby-transformer-remark",
      options: {
        plugins: ["gatsby-remark-relative-images", "gatsby-remark-images"],
      },
    },
    "gatsby-plugin-sharp",
    "gatsby-transformer-sharp",

gatsby-node.js

const { fmImagesToRelative } = require('gatsby-remark-relative-images');
exports.onCreateNode = function({ node, getNode, actions }) {
fmImagesToRelative(node);

change usage of images in GraphQL - index.js

heroImage {
childImageSharp {
fluid {
...GatsbyImageSharpFluid
}
}
}

Customize Netlify istelf
gatsby-config.js

{
resolve: 'gatsby-plugin-netlify-cms',
options: {
modulePath: `${__dirname}/src/cms/cms.js`
}
},
