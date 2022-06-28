# Half Helix Headless vendors package

## Purpose

This repository is a wrapper for several 3rd party vendor API's.

### WHY DO THIS?

- B/c endpoints for various vendor's such as Yotpo, Algolia etc are consolidated in here
- Working on headless project's means loading scripts and calling global object's functions which can lead to race conditions
- Hence, build your own frontend and use the repository to call the API's.

> We will try our best to keep the guides on `How to use the API's` up to date.

## Install

```shell
# via npm
npm i hh-headless-vendors

# via yarn
yarn add hh-headless-vendors
```


## Calling API's

```javascript
import { getProductReviews } from 'hh-headless-vendors/yotpo';

try {
  const reviews = await getProductReviews({
    appKey: YOTPO_APP_KEY,
    productId: productId
  });
} catch(err) {
  console.error("reviews()", err.message, err);
}
```
