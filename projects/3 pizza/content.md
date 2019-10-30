# Project 3: Pizza

## Objectives

* Become more comfortable with Django.
* Gain experience with relational database design.

## Overview

In this project, you'll build an web application for handling a pizza
restaurant's online orders. Users will be able to browse the restaurant's menu,
add items to their cart, and submit their orders. Meanwhile, the restaurant
owners will be able to add and update menu items, and view orders that have
been placed.

## Preparations

Before your do anything else, watch and understand these video lectures:

- Lecture 7, [Django](/lectures/django)

## Milestones

We recommend that you try to meet the following milestones in order:

* Complete the Menu, Adding Items, and Registration/Login/Logout steps.
* Complete the Shopping Cart and Placing an Order steps.
* Complete the Viewing Orders and Personal Touch steps.

## Getting Started

### GitHub Classroom

1. [Click here](https://classroom.github.com/a/F7JwXzsp) to go to the GitHub Classroom page for starting the assignment.
2. Click the green “Accept this assignment” button. This will create a GitHub repository for your project. Recall that a git repository is just a location where your code will be stored and which can be used to keep track of changes you make to your code over time.
3. Click on the link that follows “Your assignment has been created here”, which will direct you to the GitHub repository page for your project. It may take a few seconds for GitHub to finish creating your repository.
4. In the upper-right corner of the repository page, click the “Fork” button, and then (if prompted) click on your username. This will create a fork of your project repository, a version of the repository that belongs to your GitHub account.
5. Now, you should be looking at a GitHub repository titled username/project3-username, where username is your GitHub username. This will be the repository to which you will push all of your code while working on your project. When working on the project, do not directly push to the uva-webapps/project3-username repository: always push your code to your username/project3-username repository.

### Python and Django

Make sure you installed Python (Instruction for [Windows](/installation/Windows) and [macOS](/installation/macOS)).

To try running your first Flask
application:

Open "Git Bash" on Windows or the "Terminal" on macOS or Linux.

`cd` to a directory where you want to put your project. 

Clone your username/project3-username repository from GitHub and navigate into this directory.

Run

    $ pip3 install -r requirements.txt

to make sure all of the necessary Python packages (Django) are installed.

Run `python3 manage.py runserver` to start up your Flask application.
If you navigate to the URL provided by `django`, you should see the text
   `"Project 3: TODO"`!


## Requirements

Alright, it's time to actually build your web application! Here are the
requirements:

* **Menu**: Your web application should support all of the available menu items
  for [Pinocchio's Pizza & Subs](http://www.pinocchiospizza.net/menu.html) (a
  popular pizza place in Cambridge). It's up to you, based on analyzing the menu
  and the various types of possible ordered items (small vs. large, toppings,
  additions, etc.) to decide how to construct your models to best represent the
  information. Add your models to `orders/models.py`, make the necessary
  migration files, and apply those migrations.
* **Adding Items**: Using Django Admin, site administrators (restaurant owners)
  should be able to add, update, and remove items on the menu. Add all of the
  items from the Pinocchio's menu into your database using either the Admin UI
  or by running Python commands in Django's shell.
* **Registration, Login, Logout**: Site users (customers) should be able to
  register for your web application with a username, password, first name, last
  name, and email address. Customers should then be able to log in and log out
  of your website.
* **Shopping Cart**: Once logged in, users should see a representation of the
  restaurant's menu, where they can add items (along with toppings or extras, if
  appropriate) to their virtual "shopping cart." The contents of the shopping
  should be saved even if a user closes the window, or logs out and logs back in
  again.
* **Placing an Order**: Once there is at least one item in a user's shopping
  cart, they should be able to place an order, whereby the user is asked to
  confirm the items in the shopping cart, and the total (no need to worry about
  tax!) before placing an order.
* **Viewing Orders**: Site administrators should have access to a page where
  they can view any orders that have already been placed.
* **Personal Touch**: Add at least one additional feature of your choosing to
  the web application. Possibilities include: allowing site administrators to
  mark orders as complete and allowing users to see the status of their pending
  or completed orders, integrating with the [Mollie](https://github.com/mollie/mollie-api-python)
  API to allow users to actually use a credit card to make a purchase during
  checkout, or supporting sending users a confirmation email once their purchase
  is complete. If you need to use any credentials (like passwords or API
  credentials) for your personal touch, be sure not to store any credentials in
  your source code, better to use environment variables!
* In `README.md`, include a short writeup describing your project, what's
  contained in each file you created or modified, and (optionally) any other
  additional information the staff should know about your project. Also, include
  a description of your personal touch and what you chose to add to the project.
* If you've added any Python packages that need to be installed in order to run
  your web application, be sure to add them to `requirements.txt`!

Beyond these requirements, the design, look, and feel of the website are up to
you! You're also welcome to add additional features to your website, so long as
you meet the requirements laid out in the above specification!

## Hints

* Unlike in Project 1, you shouldn't need to build your application's entire
  login and authentication system yourself. Feel free to use Django's built-in
  users and authentication system to simplify the process of logging users in
  and out.
* Before diving into writing your models, you'll likely want to think carefully
  about the different types of menu items and how best to organize them. Some
  questions to consider include: how should you represent the different prices
  for large and small versions of the same dish? Where do toppings fit into your
  model for pizzas, and how do you calculate the ultimate price of a pizza? How
  will you make the custom add-ons for the subs work?

## FAQs

### What is a "Special" pizza?

It's up to you to decide what a "special" pizza means, and to implement it
accordingly. It could be one particular set of toppings, allowing up to 5
different types of toppings, or something else entirely!

## How to Submit

1. Using Git, push your work to GitHub. Ask for help if needed!
2. Go to the GitHub page for your username/project3-username repository (note: this is different from the uva-webapps/project3-username repository).
3. On the right side of the screen, click the Pull request button.
4. Make sure that the “base fork” is uva-webapps/project3-username, and the “head fork” is username/project3-username.
5. Click “Create pull request”.
6. On the next page, click the “Create pull request” button again.
7. Submit the link to your project's GitHub repository below (the one with uva-webapps/project3-username).
8. On (or before) the date of the deadline, show your working website to one of the staff.
