# The Software Tooling Cheat Sheet

Welcome to the curated software tooling cheat sheet. 

Have you ever asked yourself: **"What is the best tool for this job?"**

We searched the far depths of the internet to bring you all the information you need to get started with some of the major tools used in software engineering today. It is of course a non exhaustive list, so feel free to contribute! 

### Disclaimer
This document is **very opinionated**. Our goal is not to give you a detailed, unbiased report of exisiting tools, but rather to give a brief overview of what **in our experience** works best.

Often times we will say one tool is better than another, with little to no explanation added. Sometimes there are valid reasons, in which case we do try to briefly elaborate, but sometimes that is not the case. We might simply say one tool is better than another because it has proven so through experience. 

### Sample Configs
We have included all kinds of sample config files for different tools in the ```sample-configs``` folder. They should get you up and running in no time. 

### Topics

* [General Info](#general-info)
* [IDEs & Editors](#ides-editors)
* Bash
* Git
* [Markdown](#markdown)
* [Package Managers & Build Tools](#build-tools)
* Continous Integration
* Continous Delivery
* [Hosting Platforms](#hosting-platforms)
* [Domains & SSL](#domains)
* Licenses


## <a name="general-info">General Info</a>

The best place to go for general advice about anything is probably the repository below. Quote:

> "Some useful websites for programmers.
>
> When learning CS there are some useful sites you must know to get always informed in order to do your technologies eve and learn new things. Here is a non exhaustive list of some sites you should visit."

https://github.com/sdmg15/Best-websites-a-programmer-should-visit

## <a name="ides-editors">IDEs & Editors</a>
* #### [VIM for Humans](https://vimebook.com/en)
  Very good introduction and explanation why and how to use Vim.  
  **Recommendation**: Print any VIM-CheatSheet and place it near your desk, try out vim-keybindings in other editors.

## <a name="markdown">Markdown</a>

* The official [GitHub Cheat Sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) for GitHub flavoured Markdown.
* The most popular Markdown [cheat scheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on GitHub.

## <a name="build-tools">Package Managers & Build Tools</a>

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
* #### [pip](https://pip.pypa.io/en/stable/quickstart/)
  Simply put, the package manager for python. It uses a file called *requirements.txt* to store dependencies, which you often have to create by hand. 
* #### [PyBuilder](http://pybuilder.github.io/)
  A build tool in python for python that has build lifecylces similar to ones found in maven/gradle. 
  
### Ruby
* #### [RubyGems](http://guides.rubygems.org/rubygems-basics/)
  A dependency in Ruby is called a Gem. RubyGems is the repository for ruby dependencies, but the actual dependency management is done with Bundler. 
* #### [Bundler](http://bundler.io/)
  The actual package manager for ruby. It uses a file called *Gemfile* to store dependencies. 
* #### [Rake](https://ruby.github.io/rake/)
  Rake is a Make-like program implemented in Ruby. Tasks and dependencies are specified in standard Ruby syntax.
  
### C/C++
* #### [Meson](http://mesonbuild.com/Tutorial.html)
* #### [CMake]()

### C#
* #### [MSBuild](https://github.com/Microsoft/msbuild)
  The build tool from Microsoft for C#/.NET/Mono. It has a XML config file and doesn't just run on Windows, but also Mac and Linux, wow! 

### Haskell
* #### [Cabal]()
* #### [Stack]()

## <a name="hosting-platforms">Hosting Platforms</a>

### Free
* #### [GitHub-Pages](https://pages.github.com/)
  A great place to store **static** sites. It's easy, and even supports custom domains, however no SSL with them. 
* #### [Google Firebase (Spark)](https://firebase.google.com/pricing/)
  Google Firebase is actually a mobile and web-application development platform, but it does also support **free static sites hosting**, even with a custom domain and SSL.

### Fast & Cheap
* #### [Digital Ocean](https://www.digitalocean.com/)
  A great, easy-and-fast-to-setup solution. It is rather cheap, with their cheapest option being $5 a month. Their big bonus: they offer a ton pre-configured VMs (with things like, ubuntu, docker, etc. pre-installed). They work right of the box, and offer more advanced features like load balancing as well. As a student, you even get $50 off with an initial $5 purchase, through the [GitHub Student Pack](https://education.github.com/pack). 
  
* #### [Host1Plus](https://www.host1plus.com/)
  Probably the cheapest VPS hosting I have seen to-date, with a VM costing only $2.25 a month! Probably the best option if you have a small server that you want to run that doesn't get a lot of traffic. 

### "The Big Guns"
* #### [Azure](https://azure.microsoft.com/en-us/)
  I don't even know where to start. This has everything you can possibly dream of, and more. But it comes at a price: it is a huge pain to setup and maintain! It is one of the best services out there for serious projects, but I would not recommend it for a hobby project.. unless you sign up for [BizzSpark](https://bizspark.microsoft.com/), where you can get free credits. Azure is also not cheap, so beware.
* #### [AWS](https://aws.amazon.com/)
  Super powerful, I have never used it - we will add more later.
* #### [Google Cloud Platform](https://cloud.google.com/products/)
  Super powerful, I have never used it - we will add more later.

## <a name="domains">Domains & SSL </a>
* #### [GoDaddy](https://www.godaddy.com/)
  The default. But not always cheap, eventhough it can be as well.
* #### [Namecheap](https://www.namecheap.com/)
  ...it's really cheap!
* #### [Let's Encrypt](https://letsencrypt.org/getting-started/)
  get free SSL certificates.
