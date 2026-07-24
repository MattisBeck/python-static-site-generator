# Python Static Site Generator

I built this static site generator from scratch in Python as part of Boot.dev's guided project. Boot.dev provided the project requirements and milestones, while I wrote the implementation and tests myself.

## Why I wanted to build this
Before starting the project, I did not know about static site generators by name or tools like [Hugo](https://github.com/gohugoio/hugo) and [Jekyll](https://github.com/jekyll/jekyll). I only knew that writing HTML pages by hand could become tedious. While working through the project, I learned how static site generators turn content into finished websites without repeating the same HTML structure.

Building this was a lot of fun, and I learned a ton about Python, Markdown parsing, building HTML node structures, recursion, file processing, project structure, and testing the conversion pipeline.

## Why I didn't use my own static site generator for my website
So... Why didn't I use this generator for my own website?
First of all, my website is still fairly small and custom-built with only a few pages and infrequent updates. Writing it by hand gives me much more control over the structure and design.
For example, I could not directly use it on my [homelab pages](https://mattisbeck.com/homelab), because each page has its own layout and navigation. My generator currently only supports one shared template for all the pages.

## The final Demo website
You can find a small demo website, which I built from just a few Markdown files [here](https://mattisbeck.com/python-static-site-generator/)

## The Basic Structure
Here is a quick peek at how things are set up:

- **`src/`**: The brains of the operation. This is where all the Python code lies that is responsible for the conversion.
- **`content/`**: Drop Markdown files here, and they'll get converted into HTML. You can also put nested folders in here to create a nice structure for your site.
- **`static/`**: All the sweet extras. This folder holds the static assets like images and the CSS design to make everything look good.

## Getting Started
Want to try it yourself? Just run the program with the following commands:
- `./test.sh` to run the test suite.
- `./main.sh` to build the site normally (runs `python3 src/main.py`).
- `./build.sh` to build the site with the base path `"/python-static-site-generator/"` for deployment on GitHub Pages.
