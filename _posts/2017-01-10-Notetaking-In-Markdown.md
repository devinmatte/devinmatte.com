---
layout: post
title:  Notetaking in Markdown
subtitle: Markdown, Pandoc and Black Magic
description: Taking notes in markdown, with latex, can be really useful
date:   2017-01-10 12:15:00
categories: tutorial
featured-image: /images/posts/2017-01-10-Notetaking-in-Markdown.png
thumbnail-image: /images/posts/2017-01-10-Notetaking-in-Markdown2.png
comments: true
author: Devin Matte
author-image: /images/devinmatte.jpg
author-bio: Third Year Software Engineering Student at Rochester Institute of Technology
---

This explains my notetaking method using Markdown, LaTeX and Pandoc and how I set it up. All Instructions listed here are written for *my* personal method. Once you understand how I set it up, there are plenty of ways you can adapt this knowledge to a setup that works for you.

Installation
============

In order to set up the installation you need a few things. First we need to determine which operating system you'll be using, and then follow the installation instructions after that.

Windows
-------

### 1. Install Atom
First we're going to need to grab Atom from [atom.io](https://atom.io/)

### 2. Install Pandoc
1. There is a package installer at pandoc’s [download page.](https://github.com/jgm/pandoc/releases/tag/1.19.1)
2. For PDF output, you’ll also need to install LaTeX.
    - If you're using *windows cmd prompt* then install [MiKTeX](https://miktex.org/)
    - If you plan to use *bash on ubuntu on windows* then run `sudo apt-get install texlive` in your bash client

### 3. Atom Plugins
Launch Atom and configure it to your liking then:

1. Install `markdown-preview-plus`
    - Search for Markdown Preview Plus in Atom's Settings view **File** › **Settings** › **Install** and click **Install**. Please allow 3-5 mins for installation. Alternatively if you would prefer to use the command line utility apm: `apm install markdown-preview-plus`

2. Disable Markdown Preview
    - Disable the built in Markdown Preview package. You can do this by searching for Markdown Preview in Atom's Settings view **File** › **Settings** › **Packages** and clicking **Disable**.

Linux
-----

### 1. Install Atom
First we're going to need to grab Atom from [atom.io](https://atom.io/)

### 2. Install Pandoc
1. First you need to install pandoc via Terminal `sudo apt-get install pandoc`
2. For PDF output, you’ll also need to install LaTeX `sudo apt-get install texlive`

### 3. Atom Plugins
Launch Atom and configure it to your liking then:

1. Install `markdown-preview-plus`
    - Search for Markdown Preview Plus in Atom's Settings view **Edit** › **Preferences** › **Install** and click **Install**. Please allow 3-5 mins for installation. Alternatively if you would prefer to use the command line utility apm: `apm install markdown-preview-plus`

2. Disable Markdown Preview
    - Disable the built in Markdown Preview package. You can do this by searching for Markdown Preview in Atom's Settings view **File** › **Settings** › **Packages** and clicking **Disable**.

3. *(Optional)* Enable Pandoc
    - Optionally you may use Pandoc to render the Markdown preview. To enable Pandoc within MPP:
        1. Install pandoc
        2. Run `which pandoc` and note the full path to the Pandoc executable.
        3. On the MPP settings page enable **Enable Pandoc Parser**
        4. Enter the path from step 2 into **Pandoc Options: Path**


MacOS
------
I have not personally installed this on a MacOS system, so I cannot provide installation instructions, although I imagine they would be similar to the Linux instructions because MacOS has Bash installed by default.


How to Use
==========

Once everything has been installed you're ready to take notes in Markdown. Open up Atom to get started.

### 1. Create a new Markdown file
Once Atom is open use `ctrl + n` to open a new file tab. (Alternatively use **File** > **New File**)

From there use `ctrl + s` to save the file as `filename.md` the **.md** is important because it defines the file as a Markdown file.

### 2. Begin typing
Now you're ready to type in the document. There's just one last thing you need, to be able to see your working product. Use `ctrl + shift + M` to open the markdown preview. You must be clicked inside your markdown file tab to ensure the preview appears. If you're using LaTeX math make sure to press `ctrl + shift + X` to preview it in the preview window. There is a setting you can enable to enable math by default.

### 3. Using Math
Now you may want to use Math Equations in your notes, because let's face it, if you didn't need a little bit more than your average text editor, you'd just use an average text editor.
All Math uses LaTeX math equations, there are plenty of online resources to look them up. I used [this](http://csrgxtu.github.io/2015/03/20/Writing-Mathematic-Fomulars-in-Markdown/) a lot when learning.

#### Writing Block Equations
When writing block math, put two dollar signs `$$` at a line above and below the equation

```
$$
x^2 - \sqrt{7} \times \pi
$$
```

#### Writing Inline Equations
When writing inline, simply put a single `$` on each end of the equation.

```
$x^2 - \sqrt{7} \times \pi$
```

In order to preview your math live, use `ctrl + shift + X` to toggle math rendering

### 4. Export your work
Now that you've typed up some notes, maybe you want to print them, or share them with others. Well now comes the part where you use Pandoc.

1. Open up your Terminal (*cmd* in Windows and *Terminal* in Linux)
2. Run the command `pandoc path/to/file.md -o path/to/export.pdf`
    - Example: `pandoc ~/Documents/Notes/MathNotes.md -o ~/Documents/Notes/MathNotes.pdf`
    - If you're using *bash on ubuntu on windows* you need to run `export GHCRTS=-V0` once per session before it will work properly.
3. Now if you go to the path where you set the **.pdf** file, you'll find your document waiting for you.
