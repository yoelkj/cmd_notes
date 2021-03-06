# 🚀 GATSBY COMMANDS

# Set Up Your Development Environment

INSTALL CLI:
```sh
npm install -g gatsby-cli
```

SHOW VERSION:
```sh
gatsby --version
```

SHOW HELP:
```sh
gatsby --help
```

CREATE PROJECT FROM GITHUB HELLO WORLD:
```sh
gatsby new gatsby_tutorial https://github.com/gatsbyjs/gatsby-starter-hello-world
```

RUN DEVELOP MODE:
```sh
gatsby develop
```

CLEAN CACHE:
```sh
gatsby clean
```

INSTALL STYLED COMPONENT TO CSS
```sh
npm install gatsby-plugin-styled-components styled-components babel-plugin-styled-components
```
```sh
module.exports = {
  plugins: [
    {
      resolve: `gatsby-plugin-styled-components`,
      options: {
        // Add any options here
      },
    },
  ],
}
```

INSTALL PLUGIN IMAGE
```sh
npm install gatsby-plugin-image gatsby-plugin-sharp gatsby-source-filesystem gatsby-transformer-sharp
```
```js
module.exports = {
  plugins: [
    `gatsby-plugin-image`,
    `gatsby-plugin-sharp`,
    `gatsby-transformer-sharp`, // Needed for dynamic images
  ],
}
```

INSTALL SOURCE FILE SYSTEM
```sh
npm install gatsby-source-filesystem
```
```js
module.exports = {
  plugins: [
    // You can have multiple instances of this plugin
    // to read source nodes from different locations on your
    // filesystem.
    //
    // The following sets up the Jekyll pattern of having a
    // "pages" directory for Markdown files and a "data" directory
    // for `.json`, `.yaml`, `.csv`.
    {
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `pages`,
        path: `${__dirname}/src/pages/`,
      },
    },
    {
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `data`,
        path: `${__dirname}/src/data/`,
        ignore: [`**/\.*`], // ignore files starting with a dot
      },
    },
  ],
}
```

INSTALL CONTENFUL PLUGIN (external source data) 
```sh
npm install gatsby-source-contentful
```
```js
module.exports = {
  plugins: [
    {
      resolve: `gatsby-source-contentful`,
      options: {
        spaceId: `your_space_id`,
        // Learn about environment variables: https://gatsby.dev/env-vars
        accessToken: process.env.CONTENTFUL_ACCESS_TOKEN,
      },
    },
  ],
}
```

INSTALL slugify to slug url 
```sh
npm i slugify
```

INSTALL webfonts
```sh
yarn add gatsby-plugin-webfonts
```
```js
{
  resolve: `gatsby-plugin-webfonts`,
  options: {
    fonts: {
      google: [
        {
          family: "Roboto",
          variants: ["300", "400", "500"],
        },
        {
          family: "Open Sans Condensed",
          variants: ["300", "700"],
        },
      ],
    },
  },
},
```

INSTALL gatsby SEO
```sh
npm install gatsby-plugin-react-helmet react-helmet
```
```js
{
plugins: [`gatsby-plugin-react-helmet`]
```