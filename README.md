# Sheff Races Blog

This website hosts the development blog for our project in 2026 IBM AI Racing Competition.


The website is powered by [Ryze](https://ryze.pages.dev/) (a blog starter that is build with Astro and Tailwind CSS) and hosted via GitHub Pages.




## Deployment

To **deploy** the website (https://sheffrace.qzz.io/),
you need to have your changes **push/merged** into the **main** branch which github action will automatically sort out the deployment.


## Testing without deploying
```bash
# Install dependencies
npm install

# Start development server
npm run dev
```
The site will be available at `http://localhost:4321`
### Commands

| Command             | Description                        |
| ------------------- | ---------------------------------- |
| `npm run dev`       | Start local development server     |
| `npm run build`     | Build production-ready static site |
| `npm run preview`   | Preview production build locally   |
| `npm run astro ...` | Run Astro CLI commands             |
## Adding Blog Post
To add a blog post, you need to add in a markdown file (.md) in ``sheff-races-blog\src\blog``

Make sure to include this code snippet at the very beginning of the file in order to have the post render correctly.
```markdown
---
slug: file-name 
title:  
description: A summary of the post 
date: 2025-01-1 
author: Adam Smith 
tags: ["Tag","tag2"] 
featured: true 
editable: true 
---
```
| Field              | Value                   |Description        |
| ------------------- | ---------------------------------- | ----------------- |
| `slug`       |   `file-name`  |The name of the file. Do not include the `.md` file extension. |
| `title`     | `Title Name` |  The title of the blog post.  |
| `description`     | `A summary of the post` | A short description or summary of the blog post.   |
| `date`   | `2025-01-1` | The publication date (It should be formatted as `YYYY-MM-DD`).  |
| `author` |  `Adam Smith`   |  Your name or the author's name of the post. |
| `tags` |      `["Tag","tag2"] `      | A list of tags to assign to the post to categorizated. |
| `featured` |     `true`       |If `true`, a preview of the post will display on the homepage under the featured section. |
| `editable` |     `true`      | If `true`, an edit icon will display on the post.|

A example of a blog post can be found in ``templates\ryze-typography.md`` that showcase all the available typography feautes (like displaying headers, table, list,  video etc etc). 
## Project Structure
```
sheff-races-blog
├── public/
│   └── favicon.svg
│
├── src/
│   ├── assets/
│   │   └── ... (static assets like fonts, icons)
│   ├── blog/
│   │   ├── intro.md
│   │   └── ... (add your posts here)
│   │
│   ├── components/
|   |   ├── CopyButton.astro
│   │   ├── FeatureCard.astro
│   │   ├── Featured.astro
│   │   ├── Footer.astro
│   │   ├── Header.astro
│   │   ├── Introduction.astro
│   │   ├── Navigation.astro
│   │   ├── Newsletterastro
│   │   ├── Pagination.astro
│   │   ├── PostCard.astro
│   │   ├── ProgressBar.tsx
│   │   ├── Seo.astro
│   │   ├── Socials.astro
│   │   ├── ThemeToggle.tsx
│   │   ├── Title.astro
│   │   └── Year.astro
│   │
│   ├── layouts/
│   │   ├── BaseLayout.astro
│   │   └── BlogLayout.astro
│   │
│   ├── pages/
│   │   ├── index.astro
│   │   ├── [...slug].astro
│   │   ├── 404.astro
│   │   ├── rss.xml.ts
│   │   ├── robots.txt.ts
│   │   ├── archive/
│   │   │   ├── [page].astro
│   │   │   └── [year]/[page].astro
│   │   └── tags/
│   │       ├── index.astro
│   │       └── [tag]/[page].astro
│   │
│   ├── styles/
│   │   ├── global.css
│   │   └── typography.css
│   │
│   └── content.config.ts
├── templates/
│   └── ryze-typography.md
├── .gitignore
├── .prettierrc
├── astro.config.mjs
├── tsconfig.json
├── eslint.config.js
├── package.json
├── LICENSE
└── README.md
```