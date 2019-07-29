# We Make Websites - Advanced Technical Test
> This is an advanced level test that we require selected Shopify front-end developers to partake. We do not pay or use any of the work produced on a commercial environment. 

If you have come directly to this repository without a reference and curious to trial out this technical test - then please contact daniel@wemakewebsites.com to get yourself started!

## Brief
You will have been provided a [link](https://www.figma.com/file/Iv2wyzwS8fxFDhhusJYHLA/WMW-Technical-Test-2?node-id=48%3A0) to a design of a basic Shopify homepage on Figma accompanied with an export of all icons and images used in the designs - including product content. 

We have supplied both mobile and desktop designs but we would like you to have a think about how each of the components respond to the sizes in between. The solution is open for interpretation.

The Figma prototype also includes a simple style guide and component library for reference. We recommend using the spacing and layout variables to define the proximity between elements.

We require the build to be produced on a Shopify development store.

> 🗒 **Collaboration account**
> 
> You will need to have been invited to the Figma design file in order to inspect elements on the design. If you have not received an invite - please request an invite from the interviewer or daniel@wemakewebsites.com.


### Tips
**Modular scale**

We have provided a base font size and a scale to be used during build in the style guide, labeled at the top, for reference. We suggest using a Sass plugin to create a typographic scale, [Modularscale](https://modularscale.com). However, this is optional.


**User interactions**

One of the most important things in eCommerce design is user experience through interactions. We would like you to have a think about how you could improve the experience by adding a layer of interaction. 
An example for this test would be on the user feedback after adding a product in the quick view modal.


**ES6**

We like to have our Javascript written without any Javascript frameworks or large dependencies that would impact the overall performance. This is an enforced standard in our agency as it keeps our codebase lean and clear of any conflicts with third-party apps and integrations. Babel and Webpack have been configured as part of the workflow when you run `yarn start:dev`.


**Shopify settings**

Although we have a focus on design on the front-end, we also will be looking at how the schema structure will be set up. The settings structure should follow a thoughtful admin experience accompanied.


## Requirements
**Quick view**

You will have been supplied a design of the quick view modal, we would like this to have the following functionality.

* When user's hover over a product card, the quick view button will appear (shown in the design).
* When the button is clicked, a modal will appear with the active product data.
* Clicking add to cart will dismiss the modal and successfully post a response to the cart.


**Meganav**

The meganav component to be built using Shopify link lists and to activate on hover/focus on the Shop menu item.


**Mobile navigation**

The navigation should collapse like a basic accordion, with one panel active at a time.

**Featured collection**

This section should be pulling through an active collection. The content for these products have been included as an importable CSV file - however - the collection will need to be manually created.

This section should initialise a carousel when there are 4 items and above.

## Acceptance criteria

**We have a high focus on attention to detail in code**
* The formatting of the codebase should be consistent and written in a modular approach
* Internally, we use BEM - but we are open to other CSS naming conventions as long as it's built with scale and maintenance in mind
* We expect the codebase to be written using ES6 and libraries kept to a minimum
* We expect code to be written with performance in mind
* We expect the code to be included in the relevant files
* Mobile-first development approach using min-width media queries
  
**We have a high focus on attention to detail in design**
* We expect the designs to match as closely as they can
* Correct fonts and sizes, correct colours, correct line-heights and letter-spacing
* Images to be cropped and sized correctly to designs
* Interactions and animations to be considered but not distracting users away from the experience
* Minimal visual bugs when going resizing to mobile and large screen sizes

## Getting started
1. **Create a self-signed SSL certificate**

Before getting started, you will need to have created a self-signed SSL certificate to serve your assets locally. Please follow this guide before proceeding. [Create a self signed SSL certificate](https://github.com/Shopify/slate/wiki/4.-Create-a-self-signed-SSL-certificate)

2. **Install project dependencies**

You will need to make a clone of this repo and run the following command in the project folder. This will install the Shopify theme dependencies as well as third party packages required for the local theme development.

`$ yarn install`

3. **Set up your .env file**

You will need to create a .env file using the contents below in the project directory. These details will not be supplied to you, you will to set up a private Shopify app to get these details for your environment.

```
# The myshopify.com URL to your Shopify store 
SLATE_STORE=your-test-store.myshopify.com

# The API password generated from a Private App 
SLATE_PASSWORD=

# The ID of the theme you wish to upload files too
SLATE_THEME_ID=

# A list of file patterns to ignore, with each list item separated by ':' 
SLATE_IGNORE_FILES=settings_data.json:
```

1. **Start Node.js Express server and begin watching assets**

The command will compile the assets within /src into a /dist directory - which are all the necessary files for your theme to run.

`$ yarn start`

5. **Start developing!**

The terminal should provide you with a preview link to your theme, and will automatically inject and refresh the browser when changes are made. The preview link should like either of the following:

`https://localhost:3000/?preview_theme_id=THEME_ID`

`https://123.45.678.90:3000/?preview_theme_id=THEME_ID` 

> If you are getting localhost or certificate issues, then please follow this guide to troubleshoot the issue. [Create a self signed SSL certificate](https://github.com/Shopify/slate/wiki/4.-Create-a-self-signed-SSL-certificate)


## Reviewing and submitting your results
1. **Deploy**
   
Once you have finished and are ready for a final review, please deploy your code to your theme and send through a preview link of the Shopify theme for us to see the results.

2. **GitHub link**
   
Ensure that you have committed and pushed your most up to date changes to a public GitHub repo. Once confirmed, please send through a link to the repo for a code review.

3. **Shopify store access**

We would also require a collaborator or staff access to the Shopify store that you have complete the test on for further inspection of the theme and store set up.

4. **Let someone know**

If all is good - then contact daniel@wemakewebsites.com that the test is ready for review with a link to a GitHub repo and shopify store access - and we will get back to you as soon as we can regarding your results!


## System requirements
You’ll want to ensure you have the following already installed on your local machine before getting started with the test:

* **Node 9+:** The current LTS (long-term support) release. We like to use a Node Version Manager like NVM.

* **NPM 5+ or Yarn:** Both of these package managers have ups and downs, choose whichever you prefer. Follow the installation instructions for Yarn or NPM to make sure you're using the latest version.