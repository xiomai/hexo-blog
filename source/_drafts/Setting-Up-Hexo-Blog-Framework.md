---
title: "Setting Up Hexo: A Blog Framework and Live Deployment with Zeit Now"
date: 2020-04-09 12:14:36
tags:
  - zeit-now
  - hexo
categories:
  - [Code, Javascript, Node]
  - Hexo
---

[>>> Skip to Setup <<<](#Setting-up-Hexo)

**Note**: Unlike other blog frameworks which has a backend (CMS) for your contents, you will need to have a programming knowledge to implement this.

I have always been planning to create my own blog site and for me it was not always ideal to create it from scratch as what is important is what content I could put into it.

I have tested some frameworks like [Wink - PHP Laravel](https://wink.themsaid.com/) and [Nuxt - VueJS Framework](https://nuxtjs.org/). Both of them are easy to implement but my concern always is how is it easy to deploy live.

Ultimately I decided with a javascript static site generator, it was between Nuxt and Hexo, then use [Zeit - Now](https://zeit.co/) as for me it a great tool for fast deployments without having to setup or configure a server.

Both Nuxt and Hexo can statically generate but I preferred Hexo as it has a good variety of themes that is easy to apply and configure.

## What is Hexo

[Hexo](https://hexo.io) is `A fast, simple & powerful blog framework` according to their site.
It is a very simple JavaScript (NodeJS) static site generator application basically.

## Prerequisite

First you need to install [NodeJS](https://nodejs.org/) to be able to start. You can check this by typing in your terminal:

```shell
node --version
```

and you should see a result something like:

```
v12.16.1
```

## Setting up Hexo

### Install `hexo` globally

```shell
npm install hexo-cli -g
```

### Initializing Project

Now initialize your project _(go your code of projects folder first)_

```shell
hexo init blog
```

This will create a folder **blog**, clone the hexo-starter repository and install the dependencies of that project.
By default it will have the theme **landscape**.

### To run locally

```shell
cd blog
npm server
```

By default it will on `localhost:4000`, go and check it out, or specify a port by this command:

### Specifying a port

```shell
hexo server -p 4001
```

That's it, now you have a locally served blog!

## Theme

Personally I did like the default theme, so if you want to checkout available themes go to [https://hexo.io/themes/](https://hexo.io/themes/).

I have chosen [cactus - dark](https://github.com/probberechts/hexo-theme-cactus) as my theme.
![Hexo Theme Cactus Dark](/images/posts/cactus-dark.jpg)

The way to apply a theme is by cloning the theme's repository under you projects `theme` folder and be sure to checkout the `README.md` of the theme for insttructions.

For this particular theme this how it is set up.

```shell
git clone https://github.com/probberechts/hexo-theme-cactus.git themes/cactus
```

Change the `theme` property in the `_config.yml` file.

```
# theme: landscape
theme: cactus
```

Start and stop the server whenever you update `_confil.yml` to apply the changes.

## Hexo Config

Now that the theme is applied, you can now change your blog configs like the title, subtitle, social links, etc.

Refer to [Hexo Configuration](https://hexo.io/docs/configuration) for more details.
