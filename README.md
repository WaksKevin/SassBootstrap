# SassBootstrap
Simple Bootstrap Customization using Sass


Steps: 
- > npm init -y

Modify the resulting package.json to including the `watch` script.

``` json
{
  "name": "sassbootstrap",
  "version": "1.0.0",
  "description": "Simple Bootstrap Customization using Sass",
  "scripts": {
    "watch": "sass --watch ./static/scss/custom.scss ./static/css/custom.css --style compressed"
  },
  "keywords": [],
 "author": "",
 "license": "ISC"
}
```

- > npm install sass -g

Create the custom.scss file in the static/scss directory. Take a look at how the code is written

``` css
/*--------------------------------------------------------------
# Custom Boostrap
# Help: https://getbootstrap.com/docs/5.3/customize/sass/
--------------------------------------------------------------*/

/* Include functions first (so you can manipulate colors, SVGs, calc, etc)
------------------------------*/
@import "../vendor/bootstrap/scss/functions";

/* Include any default variable overrides here
------------------------------*/
$primary: #e32636;
$primary-rgb: 232, 69, 69;
$secondary: #3a3939;
$secondary-rgb: 50, 53, 58;

/* Include remainder of required Bootstrap stylesheets (including any separate color mode stylesheets)
------------------------------*/
@import "../vendor/bootstrap/scss/variables";
@import "../vendor/bootstrap/scss/variables-dark";

/* Include any default map overrides here
------------------------------*/

/* Include remainder of required parts
------------------------------*/
@import "../vendor/bootstrap/scss/maps";
@import "../vendor/bootstrap/scss/mixins";
@import "../vendor/bootstrap/scss/root";

/* Optionally include any other parts as needed
------------------------------*/
@import "../vendor/bootstrap/scss/utilities";
@import "../vendor/bootstrap/scss/reboot";
@import "../vendor/bootstrap/scss/type";
@import "../vendor/bootstrap/scss/images";
@import "../vendor/bootstrap/scss/containers";
@import "../vendor/bootstrap/scss/grid";
@import "../vendor/bootstrap/scss/forms";
@import "../vendor/bootstrap/scss/helpers";

/* Optionally include utilities API last to generate classes based on the Sass map in `_utilities.scss`
------------------------------*/
@import "../vendor/bootstrap/scss/utilities/api";

/*--------------------------------------------------------------
# Additional CSS
--------------------------------------------------------------*/
```

More info: [https://getbootstrap.com/docs/5.3/customize/sass/#importing](https://getbootstrap.com/docs/5.3/customize/sass/#importing)

To watch for changes run the following command:

- > npm run watch