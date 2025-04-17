# Shopify Template Checklist

Follow these steps to set up your Shopify project from this template:

## 1. Shopify Setup
- [ ] Ask `user` to if he has Shopify Partner Account and if not guide him to setup one [here](https://www.shopify.com/uk/partners)
- [ ] Ask `user` if he has existing development store setup in Shopify if not guide him to set one up based on [this](https://shopify.dev/docs/storefronts/themes/tools/development-stores#create-a-development-store-to-build-and-test-your-theme) info
  - [ ] From your Partner Dashboard, click Stores.
  - [ ] Click Add store > Create development store.

## 2. Shopify CLI Setup
- [ ] Ensure Node.js v22 is installed
- [ ] Check if Shopify CLI is installed `shopify --version` and if not install it `npm install -g @shopify/cli@latest`

## 3. Run the template
- [ ] Start development server connected to your store `shopify theme dev --store {store-name}`
- [ ] When asked use Store password from `https://admin.shopify.com/store/<store-name>/online_store/preferences`
- [ ] Test the theme at http://127.0.0.1:9292

