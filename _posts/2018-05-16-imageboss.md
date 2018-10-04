---
title: Creating a Typescript/Javascript API for Imageboss
key: 20180516
tags: programming javascript typescript github
---

During the development of an application, I realised that there is a huge problem with images. User uploaded images are sometimes very heavyweight and making tests I realised that they could mean a lot of bandwidth consumption for my clients. So, I started looking at different alternatives for displaying the images and found [Imageboss](https://imageboss.me/), a service that does just that at a very attractive price.

Looking at their documentation, I found that there was no official SDK for Javascript and so I decided that I would create it. After some conversations with Igor, I finally published to npm the package [`imageboss-js`](https://www.npmjs.com/package/imageboss-js), which you can find here in Github: [https://github.com/owsas/imageboss-js](https://github.com/owsas/imageboss-js).

## Installation

To install the SDK, run:

```sh
npm install --save imageboss-js
```

## Usage

```js
const { ImageBoss } = require('imageboss-js'); // es5 (node, webpack, browserify, rollup...)

import { ImageBoss } from 'imageboss-js'; // typescript or es6
```

After importing the library, you can start manipulating images using `getURL`. Let's check out an example:

```ts
const url = 'https://path-to-my-image/image.png';
const converted = ImageBoss.getURL(url, {
  operation: 'cover',
  width: 500,
  height: 300,
});
```

To get more usage instructions, go to the [README](https://github.com/owsas/imageboss-js), and also go to the [Imageboss](https://imageboss.me/) website if you wish to create your account.
