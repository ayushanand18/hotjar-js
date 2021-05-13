# @hotjar/browser

> Bring [Hotjar](https://www.hotjar.com/) directly to your application

## Installation

Add this package as a dependency in your project, then import the library in your code.

```bash
yarn add @hotjar/browser
```

```javascript
import Hotjar from '@hotjar/browser';
```

## Initialize Hotjar

In order for Hotjar to run, it needs to be initialized with your site ID.
You can find your site ID on [this page](https://insights.hotjar.com/site/list) just before your site name.

```javascript
const siteId = 123;
const hotjarVersion = 6;

Hotjar.init(siteId, hotjarVersion);
```

## Identify API

One of the main interest of this library is to be able to use [Hotjar Identify API](https://help.hotjar.com/hc/en-us/articles/360033640653-Identify-API-Reference).

```javascript
const userId = 'abc_123';
const firstName = 'John';
const favoriteColor = 'blue';

Hotjar.identify(userId, {
  first_name: firstName,
  color: favoriteColor,
});
```

## Manual URL changes

Depending on how your website routing works, you might need to manually instruct Hotjar when a route change has happened. [More details about URL changes](https://help.hotjar.com/hc/en-us/articles/360034378534).

```
const newPage = '/new';

Hotjar.stateChange(newPage);
```

## Example

You can find a working example on [Githup Pages](https://hotjar.github.io/hotjar-js/).
