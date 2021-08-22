# site

[![Netlify Status](https://api.netlify.com/api/v1/badges/8dd06d08-6e69-48c3-a367-7c310c94aebd/deploy-status)](https://app.netlify.com/sites/jeromerodrigo/deploys)
![GitHub](https://img.shields.io/github/license/jeromerodrigo/site)

Personal site & blog. Built using the [Hugo](https://gohugo.io/) static site generator.

## Prerequisites

- Ensure that [Hugo](https://gohugo.io/getting-started/quick-start/#step-1-install-hugo) is installed

## Local development

To get started with the site locally, just run

```
hugo server
```
After the server has started, you can view the website on `http://localhost:1313`.

## Production build

Build the site
```
hugo --minify
```

Use a http server to host the `public/` folder. Here's an example using [http-server](https://www.npmjs.com/package/http-server).
```sh
npm i -g http-server
cd public
http-server
```
Output
```
Starting up http-server, serving ./
Available on:
  http://127.0.0.1:8080
  http://192.168.0.1:8080
Hit CTRL-C to stop the server
```