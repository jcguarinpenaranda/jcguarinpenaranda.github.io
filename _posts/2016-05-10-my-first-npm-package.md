---
title: Publishing my first npm package
key: 20160510
tags: javascript programming
---

I had always wanted to start contributing to the open source community and I had been working a lot with Javascript, so I decided to publish my first npm package, which is available as `is-platform-node`. I have also been learning about [git](https://en.wikipedia.org/wiki/Git_(software)) and [Github](https://www.github.com) and I was very very attracted to writing it.

I have also been working with [`angular`](https://github.com/angular/angular) and [`ionic`](https://github.com/ionic-team/ionic), and I needed a way to easily detect if some logic was going to run only on node, so I came up with this package that runs a very basic detection and is very easy to use.

You can see my first package here: [https://github.com/jcguarinpenaranda/is-node](https://github.com/jcguarinpenaranda/is-node)

## Installation
```sh
npm install --save is-platform-node
```

## Usage

```js
var isNode = require('is-platform-node');
 
if(isNode()){
  //do something
}

// then it's the browser, or other platform
```

Publishing packages to npm easily becomes addictive :D 
