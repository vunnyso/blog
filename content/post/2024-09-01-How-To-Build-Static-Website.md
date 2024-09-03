+++
author = "Vunny Sodhi"
title = "How to build static website"
date = "2024-09-01"
description = "Guide to build static website"
tags = [
    "hugo",
    "markdown",
]
+++

Detailed steps in building static website using Hugo
<!--more-->
----
#### What is Website
Website is the collection of web pages, different multimedia content such as text, images, and videos which can be accessed by the URL.
For example: https://vunnyso.github.io

---
#### Types of Website:

- Static Website
- Dynamic Website

---
**Below are the key differences between them**
| Static Website | Dynamic Website |
| :--------: | :-------: |
| Content of Web pages cannot be changed at runtime | Content of Web pages can be changed |
| No database interaction | Interaction with database is possible |
| Faster to load  compared to dynamic website. | Slower than  static website |

---
#### Tools to generate static websites

Before we discuss specific static site generator, lets's mention other tools which are available
* **Hugo** - A blog-friendly static site generator that you can use with Github Pages.
* **Jekyll** -  A module-based static site generator with blazing fast performance.
* **Gridsome** - A data-driven static site generator that generates HTML files from local files, CMSs, and external APIs

---
#### What is Hugo
[Hugo](https://gohugo.io/) is a fast and modern static site generator written in `GO` progrmaming language. Originally created as an open source project in 2013.
Hugo Stands for High-performance Universal Generator.


#### Follow the below steps to create website

1. First install `hugo` on your system

   * On macOS (using Homebrew)
      ```
      brew install hugo
      ```
   *  On Linux (using APT for Ubuntu/Debian)
      ```
      sudo apt-get install hugo
      ```

2.  Create website using
    ```
    hugo new site <you-site-name>
    ```

3. Find theme of your choice from https://themes.gohugo.io/


4. Example for this blog I am using
    ```
    https://github.com/wlh320/hugo-theme-hulga.git themes/hulga
    ```

5. Follow the theme installtion instruction from github page of choosen theme as mentioned in step 4


6. Finally run and in view in your browser http://localhost:1313/
    ```
    hugo server --theme <your-theme-name>
    ```