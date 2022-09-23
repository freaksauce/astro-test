# Markdown frontmatter undefined on build

The setup is very simple, there is a link on the index page that loads the only markdown page in this repo, `/pages/v10.1.3/index.md`.
This markdown file has some frontmatter that looks like this:

```
---
date: 2022-09-19
title: 10.1.3
excerpt: Update visual styling of disabled check boxes/radio buttons
layout: ../release.astro
---
```

Finally there is a simple page called `release.astro` that attempts to use the `frontmatter.title` value.

When I run `npm run dev` everything is fine, however when I run `npm run build` I get the error:

```
TypeError: Cannot read properties of undefined (reading 'title')
```

I have recreated my application with this very stripped down and simple version and still have the same build error.

https://discord.com/channels/830184174198718474/1022024886757101588
