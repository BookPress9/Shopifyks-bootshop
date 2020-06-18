# BootShop - Shopify Theme
Shopify Started Theme powered by Bootstrap framework (v4), developed respecting [Shopify themes requirments](https://shopify.dev/tutorials/review-theme-store-requirements), accessbility best practices, and of course our own experince in developing themes for more than 15 years now.

## Note: 
Currently work in progress. We are constantly working with this project, and it should be completed within August 2020.

## Demo 
https://ks-bootshop.myshopify.com/

## Premium Shopify Themes 
In case you are interested in our Premium Shoipfy Themes, please visit our website
https://kondasoft.com

## Getting started
There are 2 ways to install our theme (or any other Shopify theme) on your Shopify store. 

1- The simpliest option, is by going to you Shopify Admin and installing the latest package (.zip file) from our [releases](https://github.com/kondasoft/ks-bootshop/releases/). In case you need help with this please check the [official tutorial](https://help.shopify.com/en/manual/online-store/legacy/using-themes/adding-themes#add-a-free-theme-from-the-admin) from Shopify. 

2- The second option is by using [Theme kit](https://shopify.github.io/themekit/), the the official command line tool from Shopify. This is the option which we will be covering below, as it gives you far more freedom to customize and modify our theme.

## Installation
**Note:** Please, make sure you are familiar with [Theme kit](https://shopify.github.io/themekit/), official documentation before proceding. We are assuming that at this point you have already installed Theme Kit.

### 1- Clone this repository (download theme files)
Create a new folder on your computer, `cd` to it and run the following command to copy all theme files from our GitHub repository master branch. Note: Include the dot at the end of the command to clone into your current directory.

`git clone https://github.com/kondasoft/ks-bootshop .`

### 2- Create and configure theme with Theme Kit
Run the folowing command to create a new theme in your Shopify store along with our theme files that you have just downloaded:

`theme new --password=[your-api-password] --store=[your-store.myshopify.com] --name="KS BootShop"`

Optional: Run this command to open your shopify store with our theme in preview mode.

`theme open`

## Customization
It is advised to not directly modify theme files as you will loose changes when you upgrade our theme. The recommended way to handle this is by creating a copy of our theme and then modify it. Please follow this [offical tutorial](https://help.shopify.com/en/manual/online-store/legacy/using-themes/managing-themes/duplicating-themes) to learn more.

In case you want to customize styles and scripts please continue reading below. 

### Modifing styles (SCSS)
To customize theme styles in the proper way as recommended by Bootstrap as well, is by working with [Sass](https://sass-lang.com/). 

First, create a new file called `_custom.scss` inside the `scr/scss` folder and start adding your Sass variables and styles. To learn more about what you do in your _custom.scss file, please refer to the official Bootstrap [documentation for Theming](https://getbootstrap.com/docs/4.5/getting-started/theming/)

E.g:
```scss
// src/scss/_custom.scss

// My variables
$primary: green;

// My styles
body { 
  background-color: red; // Dont' try this :)
}
```

Make sure you have Sass, Postcss and Autoprefixer installed globally by running the following command

`npm i -g sass postcss-cli autoprefixer`

Now, you can run this comand to compile your Sass files into the the theme assets folder

`npm run styles`

To deploy your changes on your Shopify store run the following Theme Kit command:

`theme deploy` or: `theme watch`

### Modifying scripts (JS)
This part will be documented soon.

## Upgrading
This part will be documented soon.

## Support
Please submit a [new issue](https://github.com/kondasoft/ks-bootshop/issues/new) in case you want to submit a bug or feature request. Additonaly, you may visit our [Support Forum](https://forum.kondasoft.com/) to discuss with other users and to get support from our Support team.
