# Shopify CLI Theme Development workflows for Online Store 2.0 Themes

## Two simple Shopify development workflows with added support for sass/scss, and Tailwind CSS

### 🎉 Works with Shopify's native Github integration

### 🛠 Requirements
- [Node](https://nodejs.org/en/)
- [Shopify CLI for themes](https://shopify.dev/themes/tools/cli)

### Dawn + Sass

### How it works:
- `sass` is included in the project to compile any `.scss` file in the assets directory, into a `.css` file with the same name. This allows basic usage of sass/scss in your theme development, while still loading minified CSS files in your theme sections.
- `.shopifyignore` is required to instruct the Shopify CLI not to interact with the additional files that are not used in a Shopify theme directory.
- A Github action is included in `.github/workflows` to allow for changes to `.scss` files from the Shopify admin code editor to be compiled to CSS. When a `.scss` file is edited and saved in the code editor, the action will run prior to the commit, and compile a `.css` file which will get picked up by Shopify's connection to Github. This Github action is only run when the user making the commit is `shopify[bot]`. This prevents unnecessary compiling on each commit from the developer.
- CSS files that have been compiled by sass should not be edited directly.
- SCSS files should not be rendered in your theme liquid.
- See the following demo files:
  - `assets/_helpers.scss`
  - `assets/_mixins.scss`
  - `assets/_variables.scss`
  - `assets/example-section.scss`
  - `assets/example-section.css`
  - `sections/example-section.liquid`

#### 🎬 Getting Started
*See installation and getting started instructions for the Shopify CLI first*
- Clone repo and push your theme up to Github
- Run `npm install` to install `sass`
- Connect your Github repo to Shopify to install the theme in your store
- Run `npm run dev` to begin development on your connected theme
- Commit and push changes to Github

### Dawn + Tailwind CSS

### 🚧 README Coming Soon