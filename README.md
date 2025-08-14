# Portfolio website template

This is a Jekyll website template that is based on the [Basically Basic Jekyll Theme](https://github.com/mmistakes/jekyll-theme-basically-basic).

Jekyll is a simple website generator that allows you to create websites using plain text files, without needing to write HTML or manage a database. It takes your content, applies layouts and themes to them, and produces a complete, static website that can be hosted anywhere (including on GitHub Pages, which is free). 

You can focus on writing your content while Jekyll handles the structure, navigation, and styling automatically.

Whenever you add or change a file, your website will be updated automatically - it may take a minute for your changes to take effect.

## Installation

1. Fork this repository: 

* to the right of the repository's name, you find a number of buttons: Pin, Watch, Fork and Star; click the Fork button
* then select your GitHub user account to be the "Owner" of the repository, and change the "Repository name" to "portfolio". Under description, write "My portfolio for the ISMC DH course". Finally, click the green "Create Fork" button.
* This will create a copy of the repository on your own GitHub page, and transport you to that page (you should see your GitHub username in the URL and at the top of the page)

2. Adapt the configuration of the site in the _config.yml file:

* In your fork of the repository, find the [_config.yml](./_config.yml) file in the list of folders and filenames, and click it
* This will open the file, which contains the settings for your site. Click the pencil icon 
 ("Edit this file") at the top right of this file to start editing the file
* Scroll down and fill in the relevant values for the following fields: 
  - title: fill in a title for your blog
  - email: fill in your email
  - name: fill in your name
  - github_username: fill in your GitHub username
* Click the green "Commit changes..." button at the top to save your changes; 
* In the popup that appears, write "Fill in personal information" as the "Commit message" and click the green "Commit changes" button. 

3. Publish your website with GitHub Pages

* Go to "Settings" tab at the top of the repo page
* Click "Pages" in the left-hand column
* Under "Source", choose "Deploy from a branch"
* Under "Branch", choose "master" and " / (root)", then click "Save"

That's it, your page will now be deployed to the web and in about 30 seconds it will be live at the URL https://\<yourGitHubUsername\>.github.io/portfolio. You can follow the progress of your deployment by clicking the "Actions" tab at the top of the repository page. 

## Adding a new blog post

Our website uses a technology called Jekyll to build html pages from simple text files,
formatted in the very simple markdown language (see the introduction to markdown [here](https://www.markdownguide.org/basic-syntax/)).

In order to publish a new blog post, simply place a new text file in the `_posts` folder; make sure the file has the extension ".md" (short for"markdown"). 

Go to the `_posts` folder in your portfolio repository on GitHub, click the "Add file" button, and choose "Create new file". 

A file editor will open; it will ask you to give your file a name. It's a good idea to add the date in the filename, and to avoid spaces in the filename: e.g., "2025-01-31-my-new-post.md". 

The file should start with a header, like this (paste the header into your new file, including the sequences of three hyphens, and adapt the title, categories, tagsm and image keys to your need):

```yaml
---
title: "My first blog"
excerpt_separator: "<!--more-->"
categories:
  - project1
tags:
  - experiments
  - tests
image: images/my-image.jpg
---
```

Explanation of the header keys:
* title : the title of your blog post
* excerpt_separator : If you add the excerpt_separator `<!--more-->` in your blog post, 
  everything above that  separator will be shown on your home page, below the title of your blog.
* categories : you can add your blog post to one or more categories, to organise them. In the "categories" page of your website, your posts will be grouped by category. 
* tags : you can assign one or more tags (keywords) to your blog post, to make it easier for readers to find posts that interest them. In the "tags" page of your website, your posts will be grouped by tag. 
* image : the path to the image that should be displayed at the top of your post. The image should be uploaded to the `images` folder beforehand.

Your blog post's text should start below the header's last line (`---`). 

For inspiration on how you can format your posts (e.g., include images and videos), take a look at the sample posts on the [Basically Basic Jekyll Theme website](https://mmistakes.github.io/jekyll-theme-basically-basic/) (and find the markdown file for the post you like on [its GitHub page](https://github.com/mmistakes/jekyll-theme-basically-basic/tree/master/docs/_posts)).

When you're ready, you can click the green "Commit changes" button at the top of the editor; in the new popup that opens, click the "Commit changes" button again. 

NB: you can also create your file in a text editor on your own computer and upload it: go to the `_posts` folder in your portfolio repository on GitHub, click the "Add file" button, and choose "Upload files".

Whenever you add or change a file, your website will be updated automatically - it may take a minute for your changes to take effect.

## Adding an image

If you want to include an image in your post, you have to upload it to GitHub first. 

Go to the `images` folder in your portfolio repository on GitHub, click the "Add file" button, and choose "Upload files". Drag and drop your image (or click the "Choose your files" button to open up a dialog that allows you to browse your computer and select an image). Once you have uploaded your file, click the green "Commit changes" button at the bottom of your screen. 

The image should now be visible in the `images` folder in your portfolio repository.

If you want to use this image in a blog post, you simply include a link to the image in your post, like this:

```
![write a caption here]({{site.baseurl}}images/my_photo.png)
```

You can change the text "write a caption here" (this will be displayed instead of your image if it can't be loaded), and you have to plug in the real filename of your image (), but it is very important that you keep all the other elements of the link intact: 

```
![          ]({{site.baseurl}}images/          )
```

Examples:

```
![My favourite picture of myself]({{site.url}}images/my_photo.png)
![A cool, techy-looking picture]({{site.url}}images/home-banner.jpg)
```

After you have added this image link to you post and have saved your file, the image will be displayed once the site has reloaded (it may take a minute to load).

## Adding a new sub-page

You can add a new sub-page (which will be shown in the left-hand menu) by adding a new page in the root of this repository (that is, the folder that contains all the other files and folders in this repository).

The header should look something like this:

```yaml
---
title: Projects
permalink: /projects/
layout: page
image: images/projects-banner.png
---
```

* The title is what will be displayed in the menu (and on top of the page when you open it);
* the permalink is what will be appended to your page's URL
* the layout defines the type of layout your page will have; options: see [here](https://github.com/mmistakes/jekyll-theme-basically-basic#layouts) 
* the image contains the path to the image that will be displayed at the top of the page. You  need to upload the image to the `images` folder first.

## Folder structure

The repository contains a lot of files and folders. Most of these you will never need to touch; they contain the templates, styles and code that build your website from the text files and images you provide. 

Here is a short list of the most important files and folders for you (you can ignore the folders and files that are not mentioned here for now):

```terminal
jekyll-theme-basically-basic
├── _posts/                          # all your blog post markdown files
|      └── 2025-08-13-first-blog.md  # a sample blog post
├── images/                          # save all the images you use on your website here
|      └── my_photo.png              # a placeholder for your photo
|      └── banner_home.png           # a sample image
├── _config.yml                      # configuration file
├── index.md                         # home page - will display your latest posts by default
├── posts.md                         # the page that displays all your posts
├── categories.md                    # the page that groups your posts by category
├── tags.md                          # the page that groups your posts by tag
├── projects.md                      # the page that describes your projects
└── README.md                        # this file - it contains the repository's documentation
```

Basically, the repository contains two important folders: one will contain your posts (`_posts`), 
the other contains all the images you use on your websit (`images`).

The index.md, posts.md, categories.md and tags.md files are templates for the pages of your website; they contain nothing more than a header, which will tell Jekyll to 


## building the site on your local machine, using [VSCode](https://code.visualstudio.com/)

If you don't want to wait for GitHub pages to load your site every time you make a small change, you can build the website on your own computer, and when you're happy with it, push it to GitHub. 

Prerequisite: you have a local clone of your repository on your computer. 

1. (only do this once) install ruby and jekyll

* follow the installation steps for [Windows](https://jekyllrb.com/docs/installation/windows/)
*  Check if Jekyll has been installed properly by running this command in your terminal: `jekyll -v`

2. (only do this once) install the necessary ruby gems: in your terminal, navigate to your portfolio folder, and then run the command `bundle install`

3. build your site: in VSCode, open the command palette (ctrl+shift+P), type "Tasks: Run Task", then choose "Run Jekyll" (This will run the "Run Jekyll" task, defined in tasks.json in this repository; based on [this website](https://tosbourn.com/running-jekyll-from-vscode/))

4. Go to your browser; the site should now be displayed at the URL http://127.0.0.1:4000/

## Customisation

For more info on how to customise your website, go to the theme's [GitHub page](https://github.com/mmistakes/jekyll-theme-basically-basic?tab=readme-ov-file#configuration).

## Credits

### Creator

**Michael Rose**

- <https://mademistakes.com>
- <https://twitter.com/mmistakes>
- <https://github.com/mmistakes>

### Icons + Demo Images:

- [Simple Icons](https://simpleicons.org/)
- [Noun Project](https://thenounproject.com)
- [Unsplash](https://unsplash.com/)

### Other:

- [Jekyll](http://jekyllrb.com/)
- [Susy](http://susy.oddbird.net/)
- [Breakpoint](http://breakpoint-sass.com/)

---

## License

The MIT License (MIT)

Copyright (c) 2017-2021 Michael Rose and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Basically Basic incorporates icons from [The Noun Project](https://thenounproject.com/).
Icons are distributed under Creative Commons Attribution 3.0 United States (CC BY 3.0 US).

Basically Basic incorporates photographs from [Unsplash](https://unsplash.com).

Basically Basic incorporates [Susy](http://susy.oddbird.net/),
Copyright (c) 2017, Miriam Eric Suzanne.
Susy is distributed under the terms of the [BSD 3-clause "New" or "Revised" License](https://opensource.org/licenses/BSD-3-Clause).

Basically Basic incorporates [Breakpoint](http://breakpoint-sass.com/).
Breakpoint is distributed under the terms of the [MIT/GPL Licenses](http://opensource.org/licenses/MIT).
