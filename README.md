# The Software Tooling Cheat Sheet

Welcome to the curated software tooling cheat sheet. 

Have you ever asked yourself: **"What is the best tool for this job?"**

We searched the far depths of the internet to bring you all the information you need to get started with some of the major tools used in software engineering today. It is of course a non exhaustive list, so feel free to contribute! 

### Disclaimer
This document is **very opinionated**. Our goal is not to give you a detailed, unbiased report of exisiting tools, but rather to give a brief overview of what **in our experience** works best.

Often times we will say one tool is better than another, with little to no explanation added. Sometimes there are valid reasons, in which case we do try to briefly elaborate, but sometimes that is not the case. We might simply say one tool is better than another because it has proven so through experience. 

### Topics

* [General Info](#general-info)
* IDEs & Editors
* Bash
* Git
* Markdown
* [Build Tools](#build-tools)
* Continous Integration
* Continous Delivery
* Hosting Platforms
* Domains & SSL
* Licenses


## <a name="general-info">General Info</a>

The best place to go for general advice about anything is probably the repository below. Quote:

> "Some useful websites for programmers.
>
> When learning CS there are some useful sites you must know to get always informed in order to do your technologies eve and learn new things. Here is a non exhaustive list of some sites you should visit."

https://github.com/sdmg15/Best-websites-a-programmer-should-visit

## <a name="build-tools">Build Tools</a>

### Java
* #### [Gradle](https://gradle.org/docs) (2012): 
  Similar to Maven, but it has a [DSL](https://docs.gradle.org/current/userguide/writing_build_scripts.html) which makes the config files short, concise and easy to work with. You get the convention and structure from Maven, but with the flexibility of a real programming language instead of bulky XML. 
* #### [Maven](https://maven.apache.org/) (2004):
  Don't use maven unless you have to, it results in very big and cumbersome XML config files. Use Gradle instead.
### Javascript
* #### [NPM](https://docs.npmjs.com/getting-started/what-is-npm): 
  THE package manager used when dealing with Javascript/[ES6](https://github.com/lukehoban/es6features)/[Node.JS](https://nodejs.org/en/). This is not a build tool on its own, but it does provide "scripts" that can be executed to build the project.
* #### [Webpack](https://webpack.js.org/):
  THE "build tool" used when dealing with ES6/next-gen Javascript. Combined with [Babel](https://babeljs.io/) it transpiles the next-gen JS to common JS. Great for web development. For libraries use Rollup. Also supports hot reloading of changes.
* #### [Rollup](https://rollupjs.org/):
  Just like Webpack, but optimized for libraries. It creates smaller bundles with something called tree shaking.  
* #### [Gulp](http://gulpjs.com/):
  Gulp is a "task runner", which means it automates tasks like minification, compilation, unit testing, linting, etc. You write a "task" that does something, and Gulp runs it. This is not just bound to next-gen JS, but also works with common JS.
* #### [Grunt](https://gruntjs.com/):
  Just like Gulp, but with more configuration to do. Stick with Gulp if you have to, but really you should be using webpack/rollup if you're using [ES6](https://github.com/lukehoban/es6features). (And if you have a choice, always go with ES6).
### Python
### Ruby
### C/C++
### C#
### Haskell
