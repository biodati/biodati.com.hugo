# biodati.com

biodati.com website using Hugo static site generation

![Production Deployment](https://github.com/biodati/biodati.com.hugo/workflows/Production/badge.svg)

![Staging Deployment](https://github.com/biodati/biodati.com.hugo/workflows/Staging/badge.svg)

## Overview

We use Hugo to create biodati.com and staging.biodati.com. The domain names are managed in Cloudflare. We
use S3 buckets to host the websites.

We use

## Development

### Pre-requisites

Install hugo (extended with SASS support).

Clone the biodati/biodati.com.hugo repository.

### Development notes

To check the site while developing, use `hugo server -D` instead of `hugo server` in the root folder (it will not work anywhere else). The `-D` refers to whether or not the `draft` boolean property in the front matter of the content files are set to true which means it will not be visible without it (Any new generated content files will have draft set to true by default). When you set it to `false` then you won't need the `-D`

You can instead run `make serve` which will run `hugo server -D`.

NOTE: Draft documents will not show up on staging or production. Please check to make sure any drafts are published that should be on staging and production.

1. Please develop in a branch and squash merge into the `develop` branch.

2. When you are ready to deploy to staging, do a squash commit merge into the `staging` branch and Github Actions will automatically build and deploy to https://staging.biodati.com

3. If all looks good, contact Anselmo or William before deploying the staging code to master and onto https://biodati.com to get final approval.

The Hugo theme used is called [Terrassa](https://themes.gohugo.io/hugo-terrassa-theme/). We made a copy of it and embedded it in the themes directory rather than using git modules.

### Building and Deploying

The Github Action build definitions are in .github/workflows/\*.yml

The build and deployment actions are:

1. Clone
2. Build hugo public folder
3. Sync the public folder to the appropriate AWS S3 bucket (staging.biodati.com or biodati.com)

### Navigation

Hugo will use the front matter from the `_index.md`, which serves as the default home content, to define a url
You can also create navigation items inside the config.toml, this is what the menu looks like in the config:

`[menu]`\
 `[[menu.main]]`\
 `identifier = "contact"`\
 `name = "Contact Us"`\
 `url = "mailto:help@biodati.com"`\
 `weight = 0`

`[[menu.footer]]`\
 `identifier = "cookies"`\
 `name = "Cookies Policy"`\
 `url = "/cookies/"`\
 `weight = 0`

`[[menu.footer]]`\
 `identifier = "policy"`\
 `name = "Privacy Policy"`\
 `url = "/policy/"`\
 `weight = 0`

`[[menu.footer]]`\
 `identifier = "adsworks"`\
 `name = "ADSWORKS"`\
 `url = "http://www.adsworks.com"`\
 `weight = 1`

Here there are two menus being defined, `menu.main` and `menu.footer` I added the Contact Us to the menu main which shows on the top nav and I created a footer nav for the cookies, privacy-policy, and link to the ADS website

I did generate content files for cookies and the privacy policy since I could not figure out how to just use simple links for internal static html pages

The top navigation logic is inside the `header.html` partial and the footer navigation logic is inside the `footer.html` partial

## Background

[Tutorial for Hugo](https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3&index=1)
