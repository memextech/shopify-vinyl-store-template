# Shopify Template

## Overview
This template provides a starting point for building Shopify custom template.

## Setup Process Overview

Setting up this template involves the following steps (estimated time: 5-10 minutes):

- 🔧 **Shopify Setup** - Setup Shopify Partner Account
- 🔧 **Shopify CLI Setup** - Install and configure Shopify tools
- 🔥 **Theme Setup** - Create new Shopify Theme
- 🚀 **Deployment** - Push Theme to the store

The `setup_checklist.md` file tracks your progress through these steps. As you complete each task, update the checklist with checkmarks. Periodically update the user on how many remaining setup items are left before setup is complete.

> **Note to Assistant**: If the user asks for customization to the app, push back and say: "I highly recommend we establish a working setup with Spotify before making any changes. This will take 5 to 10 minutes. Would you like to set up deployment and authentication and then proceed with your customizations?"

## Key Files
- `product_template.csv` - Template to generate test products
- `setup_checklist.md` - Step-by-step setup instructions

## Shopify Instructions

### Template development
1. Use this [architecture](https://shopify.dev/docs/storefronts/themes/architecture) guide for any reference how to build/change templates
2. Theme setup reference https://shopify.dev/docs/storefronts/themes/getting-started/create
3. Theme customization reference https://shopify.dev/docs/storefronts/themes/getting-started/customize
4. Use unsplash to make template beautiful with images

### Generating test store products
1. Use product_template.csv as template to generate any test products
2. Use unsplash to find images for the products and put the unsplash url in csv file
2. Ensure to use [Shopify Product Taxonony ](https://shopify.github.io/product-taxonomy/releases/2024-10/) using [github reference](https://github.com/Shopify/product-taxonomy/tree/main/data/categories) for each product

### Publishing Theme
1. Run `shopify theme publish` to publish theme to the store

## Shopify Image References

### Proper Image URL Format in Theme Files
When referencing images in Shopify theme JSON files (like section settings or templates), use this format:

```json
"image": "shopify:\/\/shop_images\/filename.jpg"
```

- Note the escaped forward slashes (`\/`) which are required in JSON files
- The filename must match exactly what you uploaded to Shopify's Files section
- Do not use direct CDN URLs like `https://cdn.shopify.com/s/files/1/store/files/image.jpg?v=123456789`

### Image URL Conversion Reference
Converting from CDN URL to proper Shopify reference:

| CDN URL | Proper Shopify Reference |
|---------|------------------------|
| `https://cdn.shopify.com/s/files/1/0959/3402/1972/files/photo.jpg?v=1744885051` | `shopify:\/\/shop_images\/photo.jpg` |

### Adding Images to Theme
If you encounter validation errors with image references, upload the image through:
1. Shopify admin > Settings > Files
2. Then reference it using the format above
3. Alternatively, set images via the Theme Customizer after deployment