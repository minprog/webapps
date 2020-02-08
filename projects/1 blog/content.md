# Project 1: Blog

## Objectives

* Learn to use Jekyll to create a more complex website.
* Better understand how to separate responsibilities in your code.

## Preparations

For this project, you'll be using Jekyll, which is a **static site generator**. It allows you to define some logic using a programming language called Liquid, write templates in HTML, add layout using CSS, and write "blog posts" using Markdown. Mike Dane provides a short introduction:

![embed](https://www.youtube.com/embed/T1itpPvFWHI)

All of these languages serve their own purposes, allowing you to write each part more easily. Jekyll is able to take your files and from those generate a HTML/CSS-based website that may be put online. Even better, you can put your Jekyll website on GitHub, make changes, and GitHub Pages will put it online for you.

## Getting Started

You are going to need to install Jekyll to be able to generate your website skeleton, and to test your site locally (i.e., on your own computer). Later on, you will put the site on GitHub Pages.

1. Follow Mike's instructions to perform the installation on either Mac or Windows:

    ![embed](https://www.youtube.com/embed/WhrU9m82Wm8)
    ![embed](https://www.youtube.com/embed/LfP7Y9Ja6Qc)

2. Then, generate a new website according to the example:

    ![embed](https://www.youtube.com/embed/pxua_1vyFck)

## The Parts and the Whole

- First, let's have a look at **front matter**. Using front matter, you can attach variables to your written content for the website. For example, if you have a Markdown file for a blog post, you can attach a *category* to it, if your site supports showing different categories of posts.

    ![embed](https://www.youtube.com/embed/ZtEbGztktvc)

- Then, learn to create a new blog post file in Markdown, using the example from the following video:

    ![embed](https://www.youtube.com/embed/gsYqPL9EFwQ)

- But besides blog posts, you will generally need to add a few pages to the website containing more static content. For example, on how to contact you or your business. Have a look:

    ![embed](https://www.youtube.com/embed/1na-IWfv08M)

These are the basics parts of any Jekyll website.

## How it all Works

Now let's dive into the details of Jekyll. You aren't quite tied to creating a website just like in the examples. Almost anything in Jekyll is customizable.

- You can specify defaults for front matter variables:

    ![embed](https://www.youtube.com/embed/CLCaJJ1zUHU)

- You can choose a different theme for your website (with some important caveats!):

    ![embed](https://www.youtube.com/embed/NoRS2D-cyko)

- You can create your own layout files using HTML:

    ![embed](https://www.youtube.com/embed/bDQsGdCWv4I)

- You can use the values of variables inside your layouts to make the code more "modular":

    ![embed](https://www.youtube.com/embed/nLJBF2KiOZw)

    (See the [Variables](https://jekyllrb.com/docs/variables/) references on the Jekyll website.)

- You can create "lists" from any collection of posts:

    ![embed](https://www.youtube.com/embed/6N1X5XffuUA)

Note that Jekyll has [built-in support for SCSS](https://jekyllrb.com/docs/assets/). Any `.scss` files in the `css/` folder will automatically be compiled into CSS that the browser can display.


## Creating your own Jekyll website

To begin Project 1:

1. [Click here](NOT LIVE YET) to go to the GitHub Classroom page for starting the assignment.
2. Click the green “Accept this assignment” button. This will create a GitHub repository for your project. Recall that a git repository is just a location where your code will be stored and which can be used to keep track of changes you make to your code over time.
3. Click on the link that follows “Your assignment has been created here”, which will direct you to the GitHub repository page for your project. It may take a few seconds for GitHub to finish creating your repository.
4. In the upper-right corner of the repository page, click the “Fork” button, and then (if prompted) click on your username. This will create a fork of your project repository, a version of the repository that belongs to your GitHub account.
5. Now, you should be looking at a GitHub repository titled username/homepage-username, where username is your GitHub username. This will be the repository to which you will push all of your code while working on your project. When working on the project, do not directly push to the uva-webprog/homepage-username repository: always push your code to your username/homepage-username repository.
6. Next, let’s set up GitHub Pages for this repository. Click on the “Settings” tab on the repository page. Scroll down until you see “GitHub Pages”, set the “Source” to “master branch”, and click “Save.”
7. If you scroll down on the page again to “GitHub Pages”, you should see the URL at which your GitHub pages website will (soon) live! But first, we’ll need to add some HTML to your repository.


## Requirements

Based on your earlier "Homepage" project, create a Jekyll-based website for yourself or some other
topic of choice. Again, the subject matter, look and feel, and design of the site are entirely up
to you, subject to the following requirements:

* Your website must contain at least four different pages, and it
  should be possible to get from any page on your website to any other page by
  following one or more hyperlinks.
* Your website's content (pages and posts) must be written in Markdown.
* Your website must contain at least two different layouts, which must be written in HTML.
* Your website's homepage's layout must include a list of the blog posts from the `_posts` directory.
* Your website's layouts must be based on at least one "include" file.
* Your website must have at least one stylesheet file.
* Your stylesheet(s) must use at least five different CSS properties, and at
  least five different types of CSS selectors. You must use the `#id` selector
  at least once, and the `.class` selector at least once.
* Your stylesheet(s) must include at least one mobile-responsive `@media` query,
  such that something about the styling changes for smaller screens.
* You must use Bootstrap 4 on your website, taking advantage of at least one
  Bootstrap [component](https://getbootstrap.com/docs/4.3/components/),
  and using at least two Bootstrap columns for layout purposes using
  Bootstrap's [grid model](https://getbootstrap.com/docs/4.3/layout/grid/).
* Your stylesheets must use at least one SCSS variable, at least one example of
  SCSS nesting, and at least one use of SCSS inheritance.
* In `README.md`, include a short writeup describing your project, what's
  contained in each file, and (optionally) any other additional information the
  staff should know about your project.


## How to Submit

1. Using Git, push your work to GitHub. Ask for help if needed!
2. Go to the GitHub page for your username/homepage-username repository (note: this is different from the uva-webapps/homepage-username repository).
3. On the right side of the screen, click the Pull request button.
4. Make sure that the “base fork” is uva-webapps/homepage-username, and the “head fork” is username/homepage-username.
5. Click “Create pull request”.
6. On the next page, click the “Create pull request” button again.
7. Click "Merge pull request".
8. Click "Confirm merge".
9. Submit the link to your project's GitHub repository below (the one with uva-webapps/homepage-username).
10. On (or before) the date of the deadline, show your working website to one of the staff.
