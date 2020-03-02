# Pizza (Flask)

**NOTE: THIS PROJECT IS NOT QUITE READY. IF YOU'D LIKE TO GET STARTED, FIRST CONTACT YOUR TEACHERS VIA E-MAIL**

## Objectives

* Become more comfortable with Flask.
* Gain experience with relational database design.
* Practice with Flask migrations and admin pages.


## Overview

In this project, you'll build an web application for handling a pizza
restaurant's online orders. Users will be able to browse the restaurant's menu,
add items to their cart, and submit their orders. Meanwhile, the restaurant
owners will be able to add and update menu items, and view orders that have
been placed.


## Milestones

We recommend that you try to meet the following milestones in order:

* Complete the Menu, Adding Items, and Registration/Login/Logout steps.
* Complete the Shopping Cart and Placing an Order steps.
* Complete the Viewing Orders and Personal Touch steps.


## Getting Started

### GitHub Classroom

1. [Click here](https://classroom.github.com/a/DWaZUt_z) to go to the GitHub Classroom page for starting the assignment.
2. Click the green "Accept this assignment" button. This will create a GitHub repository for your project. Recall that a git repository is just a location where your code will be stored and which can be used to keep track of changes you make to your code over time.
3. Click on the link that follows "Your assignment has been created here", which will direct you to the GitHub repository page for your project. It may take a few seconds for GitHub to finish creating your repository.
4. Now, you should be looking at a GitHub repository titled uva-webapps/pizzaf-username, where username is your GitHub username. This will be the repository to which you will push all of your code while working on your project.
5. Submit the link to your project's GitHub repository below.


### PostgreSQL

For this project, you'll need to set up a PostgreSQL database to use with our
application. It's possible to set up PostgreSQL locally on your own computer,
but for this project, we'll use a database hosted by
[Heroku](https://www.heroku.com/), an online web hosting service.

1. Navigate to [https://www.heroku.com/](https://www.heroku.com/), and create
   an account if you don't already have one.
2. On Heroku's Dashboard, click "New" and choose "Create new app."
3. Give your app a name, and click "Create app."
4. On your app's "Overview" page, click the "Configure Add-ons" button.
5. In the "Add-ons" section of the page, type in and select "Heroku Postgres."
6. Choose the "Hobby Dev - Free" plan, which will give you access to a free
   PostgreSQL database that will support up to 10,000 rows of data. Click
   "Provision."
7. Now, click the "Heroku Postgres :: Database" link.
8. You should now be on your database's overview page. Click on "Settings", and
   then "View Credentials." This is the information you'll need to log into your
   database. You can access the database via
   [Adminer](https://adminer.cs50.net/), filling in the server (the "Host" in
   the credentials list), your username (the "User"), your password, and the
   name of the database, all of which you can find on the Heroku credentials
   page.
   At Adminer you can use "SQL opdracht"/"SQL command" to try out a query.

Alternatively, if you install
[PostgreSQL](https://www.postgresql.org/download/) on your own computer, you
should be able to run `psql URI` on the command line, where the `URI` is
the link provided in the Heroku credentials list.


### Kickstarting the project

- Open "Git Bash" on Windows or the "Terminal" on macOS or Linux.

- `cd` to a directory where you want to put your project.

- Clone your `uva-webapps/books-username` repository from GitHub and navigate into this directory.

- Run

        $ pip3 install -r requirements.txt

    to make sure all of the necessary Python packages (Flask and SQLAlchemy, for instance) are installed.

- Run

        $ export FLASK_APP=application.py

    to the environment variable `FLASK_APP` to be `application.py`.

- You may optionally want to set the environment variable `FLASK_DEBUG` to `1`, which will activate Flask's debugger and will automatically reload your web application whenever you save a change to a file.

- Set the environment variable `DATABASE_URL` to be the URI of your database, which you should be able to see from the credentials page on Heroku.

- Run `flask run` to start up your Flask application.

- If you navigate to the URL provided by `flask`, you should see the text `"Pinocchio's: TODO"`!


### Your first migration

- Your `application.py` already `import`s the Flask "migrations" plugin. This plugin will use the **Alembic** system to generate your database structure for you, as derived from the models that you create. To get started, `models.py` already contains one model for storing `User` names. Take a look at `models.py` before you go on!

- Now generate a `migrations` directory in your project by running

        $ flask db init

    and take a look at the migration files. You will not need to change any of these.

- Then, generate your first migration by running

        $ flask db migrate -m "Initial migration."

    and take a look at the `migrations/versions` directory. It will now contain a single migration file with a unique name. This contains rules to "upgrade" or "downgrade" your database. In the method `upgrade`, you will find that a method `create_table` is called to create the `users` table in the database.

- To upgrade your database to the current version using that first migration, run

        $ flask db upgrade

- However, you have no good way to inspect or change the data in the database yet. The next section will help you out there.

- One thing to pay attention to, is that generating migrations often works very well, but some changes can't be derived automatically. For example, if you decide to rename your `users` table to `userinfo`, then run `flask db migrate`, you will find that the migration first deletes (all data in the) users table and then create a new table called `userinfo`. But it isn't necessary to delete the table in that case! SQL (and SQLAlchemy) have methods to rename tables. You can change the migration to replace the remove/add combo by a rename command. See the [Alembic operations reference](https://alembic.sqlalchemy.org/en/latest/ops.html) for more information.


### Integrating the admin section

Flask comes with many optional plugins. One of those is `flask-admin`, which generates pages to edit data in the database. Such a generic admin interface can be very useful when starting up a project. Going on, you might decide to create more specialized pages that allow users to add or delete data, but it's great that you don't have to until later! Let's add an admin page for the `User` model.

- To add this plugin, first edit `requirements.txt` to add `flask-admin`. Then follow up with

        $ pip3 install -r requirements.txt

    which should install the plugin to your local system.

- Then, in your `application.py`, add `import`s:

        from flask_admin import Admin
        from flask_admin.contrib.sqla import ModelView

- Use one of the methods on [Stack Overflow](https://stackoverflow.com/questions/34902378/where-do-i-get-a-secret-key-for-flask) to generate secret key, and add it to an enviroment variable called `SECRET_KEY`. Then add this line to your apps `application.py` to configure it.

        app.secret_key = ENV['SECRET_KEY']

- Below the initialization section, but before your first route, add another section to configure the admin interface and generate your first admin page as well, which will be linked to your `User` model:

        admin = Admin(app, name='Pinocchio Admin', template_mode='bootstrap3')
        admin.add_view(ModelView(User, db.session))

    You can later add additional calls to `add_view` to link more models to your admin interface.


## Requirements

Alright, it's time to actually build your web application! Here are the
requirements:

* **Menu**: Your web application should support all of the available menu items
  for [Pinocchio's Pizza & Subs](http://www.pinocchiospizza.net/menu.html) (a
  popular pizza place in Cambridge). It's up to you, based on analyzing the menu
  and the various types of possible ordered items (small vs. large, toppings,
  additions, etc.) to decide how to construct your models to best represent the
  information. Add your models to `models.py`, generate the necessary
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
  they can view basic details of any orders that have already been placed.

* **JavaScript**: TODO AUTOCOMPLETE?

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

> A special note: your neighbor might choose to implement additional features, and you might think that those parts are mandatory to implement. This may not be true! So, before you implement the same features, always take a good look at the requirements above and decide if you really want to implement it the same way!

## Implementation details

The following remarks place important constraints on your project's implementation:

* TODO Unlike in Project 1, you shouldn't need to build your application's entire
  login and authentication system yourself. Feel free to use Django's built-in
  users and authentication system to simplify the process of logging users in
  and out.

* Before diving into writing your models, you'll likely want to think carefully
  about the different types of menu items and how best to organize them. Some
  questions to consider include: how should you represent the different prices
  for large and small versions of the same dish? Where do toppings fit into your
  model for pizzas, and how do you calculate the ultimate price of a pizza? How
  will you make the custom add-ons for the subs work?

* You should not use jQuery. Using JavaScript is not required for this project, but if you use it, you should show off your newly learning ES6 skills from lecture!

* You should not use raw SQL queries, but instead always use SQLAlchemy to interact with the database. In very special circumstances it might be OK to write a custom query, but in general this should not be necessary and is not allowed for this assignment.


## FAQs

### I called my model `Pizza_Hut` and now I get errors!

Note that model names should be written in `CamelCase` and not in `snake_case`. When writing camel cased names, the words are separated by using capital letters. You should not add underscores, because the Django framework depends on camel casing.

### I can't get the database design "right"!

Well, this is indeed a big challenge and a fundamental part of this project. For historical reasons, Pinocchio's menu has become pretty arcane, and a such, hard to "fit" into a nice database design. It's up to you to decide on trade-offs between different solutions.

### What is a "Special" pizza?

It's up to you to decide what a "special" pizza means, and to implement it
accordingly. It could be one particular set of toppings, allowing up to 5
different types of toppings, or something else entirely!


## How to Submit

1. Using Git, push your work to GitHub. Ask for help if needed!
9. Submit the link to your project's GitHub repository below (the one with uva-webapps/pizzaf-username).
10. On (or right after) the date of the deadline, show your working website to one of the staff.