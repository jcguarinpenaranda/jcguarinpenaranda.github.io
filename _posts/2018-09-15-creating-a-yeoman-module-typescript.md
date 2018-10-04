---
title: Creating a Yeoman module for typescript
key: 20180915
tags: programming javascript typescript github
---

A year ago, I posted a new entry [announcing the creation](/2017/10/22/typescript-module-template.html) of a [Typescript module template](https://github.com/owsas/typescript-module-template), very easy to clone to start developing new Typescript modules ready to be published to [npm](https://www.npmjs.com/) with typings, linting and testing integrated.

So here is the code to the [typescript module generator with Yeoman](https://github.com/owsas/generator-typescript-module) that I created and want to share with all the open source community.

## About Yeoman

[Yeoman](http://yeoman.io/) is a Javascript CLI tool that helps you generate new Javascript projects, used for example by Microsoft to create new [Visual Studio Code](https://code.visualstudio.com/) extensions, or creating new `node` modules. These recipes are called Generators and there are [lots of them](http://yeoman.io/generators/).

## The Typescript Module Generator

The code I created, available [here](https://github.com/owsas/generator-typescript-module), defines a new Typescript module, that clones the [Typescript Module Template](https://github.com/owsas/typescript-module-template) repository and sets the right name and author in the `package.json` file. It also breaks the git connection between the new code and the template repository and gets you all set to start coding.

### Installation

To install it, first install Yeoman and generator-typescript-module using [npm](https://www.npmjs.com/) (we assume you have pre-installed [node.js](https://nodejs.org/)).

```bash
npm install -g yo
npm install -g generator-typescript-module
```

Then generate your new project:

```bash
yo typescript-module
```

The generator will get you ready in seconds.
