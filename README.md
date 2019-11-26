# cookie-consent-box

[![Latest Version on NPM](https://img.shields.io/npm/v/cookie-consent-box.svg?style=flat-square)](https://npmjs.com/package/cookie-consent-box)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/adriandmitroca/cookie-consent-box/master.svg?style=flat-square)](https://travis-ci.org/adriandmitroca/cookie-consent-box)

This is a simple package that lets you add good-looking cookie box to your website
within few seconds without any setup required. If you would like to see
how it works and looks, make sure to check out the [demo](https://adriandmitroca.github.io/cookie-consent-box).

## Usage

### Webpack

You can install the package via package manager of your choice:

```bash
$ yarn add cookie-consent-box
$ npm install cookie-consent-box
```

Import it as normal ES6 module:

```js
import CookieBox from 'cookie-consent-box';

new CookieBox({ options }).init();
```

and include in your SCSS file:

```scss
@import "~cookie-consent-box/dist/cookie-consent-box";
```

### CDN

Or include it via jsDelivr CDN:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/cookie-consent-box@2.4.0/dist/cookie-consent-box.min.css" />
<script defer src="https://cdn.jsdelivr.net/npm/cookie-consent-box@2.4.0/dist/cookie-consent-box.min.js"></script>
```

Additionaly, you can configure the plugin using `CookieBoxConfig` object declared in your DOM. 
Just make sure that you declared it before you load js file.

Example:
```js
<script>CookieBoxConfig = { backgroundColor: '#ec008c', url: '/privacy-policy' }</script>
```

## Available Options

| Option | Type | Default | Description |
|---|---|---|----|
| backgroundColor | string | #007bff | Color used for background |
| textColor | string | #fff | Color used for text |
| language | string | en | ISO 639 code. Supported languages: `en`, `de`, `pl`, `ro`, `it`, `fr`, `pt` |
| url  | string/null | null | Custom URL that points to your Privacy Policy page. If empty, link is automatically hidden.
| linkTarget | string | _blank | The `target` parameter for the url above.
| containerWidth | int | 1140 | Width of your page container
| cookieKey | string | cookie-box | Cookie name that is used to save users acceptance
| cookieDomain | string | defaults to the host portion of the current document location | The domain that the cookie belongs to
| cookieExpireInDays | int | 365 | The number of days after which the cookie expires
| content | object/null | defaults to language | Content object accepts following properties: `title`, `content`, `accept`, `learnMore`.

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

## Credits

- [Adrian Dmitroca](https://github.com/adriandmitroca)
- [Alexander Pepper](https://github.com/apepper)
- [Daniel Stancu](https://github.com/birkof)
- [All Contributors](../../contributors)
