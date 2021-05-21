###### tags: `mdf` `gatsby` `airtable`
# MDF Project Spring '21
Displaying student projects on a website with Gatsby. The project builds upon [this tutorial](https://hackmd.io/pBPs96b-Q_KdkYm1Dc3ZyQ).

- Goal: to display student work (stored in Airtable) on a website
- Tools: Airtable, Gatsby, GraphiQL
- Languages: HTML, CSS, Javascript
- Useful resources:
    - Project starting point: [getting AT data to a website](https://hackmd.io/pBPs96b-Q_KdkYm1Dc3ZyQ)
    - [How to use Gatsby (general)](https://www.gatsbyjs.com/docs/tutorial/)
    - [Daily start up instructions](https://github.com/ckakiti/General/blob/master/akiti_mdf21_startup.md)

## Key project files
The website was built with a [Gatsby starter template](https://github.com/gatsbyjs/gatsby-starter-default). Within that template, there are several files that contain information critical to website function:
### 1) gatsby-config.js
- contains metadata for website (e.g. title, plugins, etc.)
- location: `PROJECTFOLDER/gatsby-config.js`
- modifications:
    - gatsby-source-airtable (plugin)

### 2) .env.development
- new file storing Airtable-specific variables for additional level of privacy (e.g. API key, BaseID)
- variables referenced in `gatsby-config.js`
- location: `PROJECTFOLDER/.env.development`
- modifications: 
    - AIRTABLE_API_KEY ([how to find](https://support.airtable.com/hc/en-us/articles/219046777-How-do-I-get-my-API-key-))
    - AIRTABLE_BASE_ID ([how to find](https://www.basegenius.com/airpower/help/how-to-find-airtable-base-id/))

### 3) index.js
- organizes project information on the landing page
- location: `PROJECTFOLDER/src/pages/index.js`
- modifications:
    - **query** (fetching airtable data from graphql)
    - **IndexPage** (formatting the display of the landing page)
    - **Card** (defining how information about each project will look on the landing page)
    - **Tag Link** (defining how the associated project tags will look and directing them to individual project pages)

### 4) gatsby-node.js
- contains instructions for how to build site (e.g. what pages to create, what data to use, etc.)
- location: `PROJECTFOLDER/gatsby-node.js`
- modifications:
    - const projectResult (data from graphql)
    - createPage (make a new page for each project entry using template from `project_template.js`)

### 5) project_template.js
- new file with template for how each  project page should look
- location: `PROJECTFOLDER/src/templates/project_template.js`
- modifications:
    - query (fetching data from Airtable)
    - project_info (displays project name and description as headers)

## Still working on:
- add class image to landing page
- arrange cards on landing page side-by-side, 2-3 per row
- add first 1-2 sentances of project description under each card
- add project links to each page (if any)
- stylize project pages (make it look prettier)
- basically make the formatting similar to [this template](https://gatsby-casper.netlify.app/)