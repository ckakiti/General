# MDF Project Spring '21
Displaying student projects on a website with Gatsby. The project builds upon [this tutorial](https://hackmd.io/pBPs96b-Q_KdkYm1Dc3ZyQ).

- Goal: to display student work (stored in Airtable) on a website
- Tools: Airtable, Gatsby, graphql
- Languages: HTML, CSS, javascript

## Useful resources
- [Starting point: getting AT data to a website](https://hackmd.io/pBPs96b-Q_KdkYm1Dc3ZyQ)
- [Gatsby tutorial](https://www.gatsbyjs.com/docs/tutorial/)
- Daily start up:
    1. open atom (text editor)
        - open current project (located at `~/Development`)
        - open main files (see below)
    2. open new terminal window and type
        - `cd ~/Development/PROJECTNAME`
        - `gatsby develop` (takes some time, may throw errors)
    3. To view website in browser, open http://localhost:8000/ and http:/localhost:8000/__graphql

## Key files
The website was built with a [Gatsby starter template](https://github.com/gatsbyjs/gatsby-starter-default). Within that template, there are several files that contain information critical to website function:
### 1) gatsby-config.js
- contains metadata for website (e.g. title, plugins, etc.)
- modifications:
    - gatsby-source-airtable (plugin)

### 2) .env.development
- added file which stores Airtable-specific variables for additional level of privacy (e.g. API key, BaseID)

### 3) index.js
- contains
- key modifications:

### 4) gatsby-node.js
- contains
- modifications:

### 5) project_template.js
- contains
- modifications:
