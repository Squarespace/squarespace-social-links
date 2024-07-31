# This repository is scheduled to be deprecated. After October 31, 2024, the contents of this repo will no longer be available on GitHub. See [developers.squarespace.com/tools](https://developers.squarespace.com/tools) for more details

Squarespace Social Links
------------------------------

Plug-and-play social icons template partial for Squarespace websites that link out to your connected accounts.

*NOTICE: This code is licensed to you pursuant to Squarespace’s Developer Terms of Use. See license section below.*

## Usage

### Installing Toolbelt

This is a Squarespace web module. To handle the markup, styles, and configuration files in this module, you'll need to install [Squarespace Toolbelt](https://github.com/Squarespace/squarespace-toolbelt) as a development dependency and use its `assemble` functionality.

```sh
npm install --save-dev @squarespace/toolbelt
```

### Using Social Links

Basic usage is as simple as applying the template partial.

```jsont
{@|apply sqs-social-links.block}
```

Tweaks are automatically added for:
* Size
* Style (Regular, Border, Knockout, Solid)
* Shape (Square, Rounded, Circle)
* Color

If you want to set a different color for a certain occurrence of the partial, you can use the mixins provided by the LESS file to override the default color:

```LESS
// Using mixin to override color
@custom-social-icons-color: cornflowerblue;
.my-special-container {
  .mixin-template-social-icons-color(@custom-social-icons-color);
}

// Same, but with classname on body
body.is-special-page {
  .mixin-template-social-icons-color-body(@custom-social-icons-color);
}
```


## License
Portions Copyright © 2016 Squarespace, Inc. This code is licensed to you pursuant to Squarespace’s Developer Terms of Use, available at http://developers.squarespace.com/developer-terms-of-use (the “Developer Terms”). You may only use this code on websites hosted by Squarespace, and in compliance with the Developer Terms. TO THE FULLEST EXTENT PERMITTED BY LAW, SQUARESPACE PROVIDES ITS CODE TO YOU ON AN “AS IS” BASIS WITHOUT WARRANTIES OF ANY KIND, EITHER EXPRESS OR IMPLIED.
