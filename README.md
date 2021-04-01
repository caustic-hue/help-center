# FalixNodes Help Center - Design Refresh
![image](https://i.imgur.com/YKRFCSL.png)

A new design of the help center is being worked on along with adding a few other things like filters, search, author, and options(Copy Link, Report, and Edit)

# Creating a New Article
Want to help contribute to the Help Center? Write or update an article!

## 🛡️ Requirements 
 - The communication must be clear and well explained for the user to understand
 - Fact check and make sure the information you're providing is accurate
 - Good grammar, we check our grammar using [Grammarly](https://grammarly.com/)
 - Valid syntax, make sure there are no syntax errors
 - Proper metadata

## ✍️ Creating an Article
By following the file structure, create a `.md` file under the correct category. As an example, if you were to create an article that explains on how to install and use a plugin on Minecraft Java, the file would be created like `docs/minecraft/plugins/plugin-name.md`. Then start writing the article in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do, if you need help understanding how to do certain task like creating a link, inserting an image, creating a list look [here](https://guides.github.com/features/mastering-markdown/).

## 📃️ Metadata
Make sure the metadata is setup probably, this is usually at the top of every article.
It should look like this:
```
---
layout: default
title:  "Article Title"
parent: Sub-Category
grand_parent: Category
permalink: /category/sub-category/article-title/
tags: falixnodes
---
```

## 📢️ Publishing
Create a pull request on this repo and title it like this "New Post: Name of Article" or if you're editing an article, title it like "Edit: Name of Existing Article".

We use [Cloudflare Pages](https://pages.cloudflare.com/) to host the Help Center, so when the pull requested is merged, Cloudflare will rebuild the Help Center and then update if the rebuild was success.

Your edit will be reviewed by [Korbs](https://github.com/KorbsStudio/) along with your code to check for any syntax error.

*We use the [Just the Docs](https://pmarsceill.github.io/just-the-docs/docs/ui-components) theme with slight modifications to styling.*
