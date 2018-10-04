---
title: Creating a typescript module template
key: 20171022
tags: javascript typescript programming
---

[Follow this link to the repo](https://github.com/owsas/typescript-module-template)

I must admit that I love [Typescript](https://www.typescriptlang.org/). As it becomes more and more useful for me, making me able to define types for the variables I write in Javascript, making me able to define classes, interfaces, decorators and more, I realised that I needed to create a template which I could easily clone in the future to keep developing more Typescript modules for my applications.

So, I got my hands dirty and started configuring Typescript for my project. I created the `tsconfig.json` file, installed Typescript as a `dev dependency` and created the `index.ts` file

`tsconfig.json`
```json
{
  "compileOnSave": true,
  "compilerOptions": {
    "lib": [
      "es2015",
      "dom"
    ],
    "outDir": "out",
    "declaration": true,
    "declarationDir": "out",
    "rootDir": "src"
  },
  "exclude": [
    "node_modules",
    "test",
    "out"
  ]
}
```

`index.ts`
```ts
export class MyModule {
  // Your code here
}
```

## EDIT
Now the typescript module template is also available as a `yeoman` generator, here: [https://github.com/owsas/generator-typescript-module](https://github.com/owsas/generator-typescript-module)

## How to use

To start developing with the typescript module template, clone [this repo](https://github.com/owsas/typescript-module-template), and start adding your code in the `index.ts` file.  

When you are done, write the tests in the `index.test.ts` file. For testing, this repo works with [Jest](https://facebook.github.io/jest/).

Once you finished, you can publish your module to npm with `npm publish`. This will compile your Typescript code
and send it to npm.

Make sure to change the name of the package in `package.json`

## Dev Features
* Testing with Jest
* Linting out of the box (checks the style of your code), with TSLint
* Build, prepublish and other scripts to help you to develop
* Works with Typescript: Static typing for your JS Applications, reducing amount of runtime errors
* Coverage out of the box, thanks to Jest
* Uses deterministic module resolving, with `package-lock.json`

## Conclusion

Being able to develop faster, having a Typescript module template makes me much more productive in my day by day. In this way I just need to clone the repository I created and start adding my custom code, then publish it to [npm](https://www.npmjs.com).
