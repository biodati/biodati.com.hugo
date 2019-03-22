# biodati.com.hugo
Hugo-based biodati.com website

The Hugo theme used here is called [Terrassa](https://themes.gohugo.io/hugo-terrassa-theme/)

This is the [tutorial](https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3&index=1) that I followed for Hugo

IMPORTANT NOTE: For some reason I cannot push the theme up to github, so you may have to do a git clone from the [terrassa theme github](https://github.com/danielkvist/hugo-terrassa-theme) into the theme folder. It may easier to just pull the `_default/` files out and put them into the root site instead of the theme.

### Usage
To run the site, use `hugo server -D` instead of `hugo server` in the root folder (it will not work anywhere else)
The `-D` refers to whether or not the `draft` boolean property in the front matter of the content files are set to true which means it will not be visible without it (Any new generated content files will have draft set to true by default). When you set it to `false` then you won't need the `-D`

The navigation can be affected by this as well since the `_index.md` (which serves as the home for each content folder e.g. `/posts`).

### Summary
* I created partials from the original biodati site separated by each section
* placed all those partials inside the `index.html` which is in the top level of the `layout/` folder which hugo recognizes as the home page of the site
* these files override the theme partials and the theme home page
* the only files that are still used from the theme are the files in the `_default/` folder which hugo uses for the default templates (the name is very important so I created a `_default/` folder as well in the layout folder, but I did not copy the template files over)
* hugo creates navigation from generated content files (e.g. `hugo new posts/post1.md` which hugo creates a url for `/posts/post1`)
* you can also defined navigation items inside the config file which I did for the Contact Us (under `[menu]` in the config.toml)
* Also Hugo has an [asset pipeline](https://gohugo.io/hugo-pipes/) which I used for sass files

Hugo does not pull from the config.toml in the theme

### Created Files
The home page of the biodati site is in the `index.html` template file which is in the root layout folder and is made up of partials which looks like this:

`{{ define "main" }}`\
`{{ partial "hero.html" . }}`\
`{{ partial "videos.html" . }}`\
`{{ partial "uses.html" .}}`\
`{{ partial "features.html" . }}`\
`{{ partial "focuses.html" . }}`\
`{{ end }}`

the `{{ define "main"}}` `{{ end }}` is used for the `baseof.html` (once again located in the theme `_default/` folder).
The partials and the home page override the index and partials of the Terrassa Theme files.
The site is still using the templates in the `_default/` folder (baseof, list, and single are internally recognized hugo files and those names are important, including the `_default/`).
* `baseof.html` which is the base that all templates inherit from
* `list.html` which contains logic for any list content such as blog posts
* `single.html` which is to view a single item
* `card.html` and `tags.html` are specific to the template, but not Hugo overall (tags will be useful for adding tags for posts)
* You can still add custom files to the `_default/`

the `baseof.html` file looks like this:

`<!DOCTYPE html>`\
`<html lang="en">`\
`{{- partial "head.html" . -}}`\
`<body>`\
    `{{- partial "header.html" . -}}`\
    `{{- block "main" . }}{{- end }}`\
    `{{- partial "footer.html" . -}}`\
`</body>`\
`</html>`

Any file inside the layout folder wrapped in the `{{ define "main" }}` will go into the `{{ block "main" . }}` tag above which has the header and footer around it as well

Hugo also looks in the layout folder for any names that match the content files and will use that layout for that content so if you wanted to use a different `list.html` template page for say a specfic blog, you would just put the `list.html` file in that folder you created

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

The top navigation logic is inside the `header.html` partial and the footer navigation logic is inside the `footer.html` partial

### Hugo Pipes
[Hugo Pipes](https://gohugo.io/hugo-pipes/) is an asset pipeline (if downloading hugo, download the extended zip version 0.43 and above otherwise it will not exist)

I'm not completely sure how it works, but the logic is inside the `head.html` partial

