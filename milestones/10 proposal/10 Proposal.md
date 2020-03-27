# Project Proposal

You'll kick off your project by handing in a proposal document. This document should connect the functional design of your project (what does it do?) to a problem in the real world. Below, we list all required aspects of your proposal document.

## Getting started

1. To start your project, you should accept a new assignment on GitHub classroom:

	[Accept the Final Project assignment](https://classroom.github.com/a/rsHLtKs2).

	This will create a GitHub repository for your project. Recall that a git repository is just a location where your code will be stored and which can be used to keep track of changes you make to your code over time.

{:start="2"}
2. Click on the link that follows "Your assignment has been created here", which will direct you to the GitHub repository page for your project. It may take a few seconds for GitHub to finish creating your repository.

3. In the upper-right corner of the repository page, click the "Fork" button, and then (if prompted) click on your username. This will create a fork of your project repository, a version of the repository that belongs to your GitHub account.

Now, you should be looking at a GitHub repository titled username/project-username, where username is your GitHub username. This will be the repository to which you will push all of your code while working on your project. When working on the project, do not directly push to the uva-webapps/project-username repository: always push your code to your username/project-username repository.

Inside your new repository you will find a mostly empty file called `README.md`. Your should write your proposal in that file using the **Markdown** language ([read a brief intro](https://guides.github.com/features/mastering-markdown/)).

## Adding pictures

You will need to include some sketches into your proposal. Put these images inside the folder called **doc** inside your repository. Use exactly that name, for consistency with other projects! To use pictures from the `doc` folder in a Markdown document, use the following example.

    ![Alternative Text](doc/image.png)

Make sure that you provide an alternative (descriptive!) text inside the square brackets as well, as this will greatly help visually impaired people in understanding the contents of your proposal, as well as guarantee that the content of the image is clear, even if it fails to load. 

## Goal of the document

You and others can use this document to estimate the effort required to implement the project. Your project has a high risk of failure if:

- the envisioned product tries to do too much
- the envisioned product doesn't do enough
- the purpose of the product is not well-defined (too vague)

By writing a clear proposal document and getting feedback on it from multiple students and teachers, you can better avoid these risks!

## Problem statement

Write a brief statement, four lines of text, about the **problem** (not the solution) that your finished product will solve or the idea that it is based on. The problem has to be clearly described and very specific. We see a few possibilities:

- There is a clearly defined problem that a reasonable group of people have, which a web application is particularly suited to solve.
- There is a widespread lack of knowledge or understanding that an interactive visualization or story is particularly suited to remedy.
- There is an interesting game concept that is particularly suited to implementing in a server-side or client-side web application.

In all cases, you should be able to define a specific target audience or a specific categorization of your proposed web application. Include that, too.

## Solution

Describe your solution in full detail.

- **Summarize** your idea in a single sentence, connecting it to the problem that you have defined.

- Include a **visual sketch** of what the final product will look like for the user; if you envision the application to have multiple screens, sketch these all out separately. Clearly specify the possible user interactions, and include concrete examples of data. Your sketches have to be complete and neat!

<div class="row">
<div class="col-xs-6 col-md-3">
<a href="/course/10%20Milestones/10%20Project%20Proposal/screens-proposal.png" class="thumbnail">
![](screens-proposal.png)
Example sketch for a mobile app
</a>
</div>
<div class="col-xs-6 col-md-3">
<a href="/course/10%20Milestones/10%20Project%20Proposal/sketch.jpg" class="thumbnail">
![](sketch.jpg)
Example sketch for a data visualization
</a>
</div>
</div>

- Include a brief list of **main features** that will be available to users. All features should also be visible in the sketch. If you have complicated features, it might be good to create a separate sketch for each feature. Yes, you will do a lot of sketching! This is required.

- Mark which features define the *minimum viable product* (MVP) and which parts may be optional to implement.

## Tips for sketching

- [Prototyping in Keynote](https://designcode.io/sketch-keynote). You can use Keynote on Mac, but you can also create a free account on [iCloud](https://www.icloud.com) and use it online. This allows you to make very interactive prototype without much effort.

- [Marvel](https://marvelapp.com) is a fairly advanced prototyping website. It may take more time to get used to.

- [Wireframe.cc](https://wireframe.cc) is a very simple prototyping tool. Easy to get started! You can save each page as a separate wireframe and share with anyone. However, it's not possible (for free) to create an account to save your designs for later editing etc. That should not really be a problem for one week.

Do make sure that you use realistic content in your sketches! Google a few images, write real texts and make sure it gives a good impression of what you want to make.


## Prerequisites

Describe the things that you'll have to get in order before really starting your project.

- List any **data sources** that you will use and whether you will need to transform the data before it is usable for your application. The list should include links to where the data sources can be found (downloaded or accessed via API). If you need to have an account to access the data, make the account now. Often it proves to be harder than expected to access good data.

- List the **external components** (libraries like `sqlalchemy` or `bootstrap`) that you need to implement certain features. Include the names, and if the component is not very standard, include a link to its website. Specify what part you need and what for.

- Include a review of **similar** web apps, in terms of features and technical aspects: what do they do? how have they implemented it? can you do it in the same way? (Spend a few lines per "competitor".)

- Identify the **hardest parts** of implementing your application: think of technical problems or limitations that could arise during development and what possibilities you have to overcome these.

## Sanity check

Before continuing, compare your solution to the [project requirements](/reference/requirements) one last time. Also, is it still clear that your proposed project is indeed a solution to the stated problem?

The proposal document should be well-written and clearly formatted. Do not forget to include a
title, your name, and a paragraph summary of the application goals at the top. Use Markdown to format your headers etc.

Finally, make sure that your document is spell-checked, and that images are **not too large** or too small (your document will be read in a normal browser via GitHub).

## Submitting

After you have pushed all changes to Github, copy the URL of the GitHub page for your project and submit it below. It will be in this format: `https://github.com/username/project`. You should NOT submit the github/uva-webapps URL this time, because we will be tracking your project during the next few weeks!

Don't commit any code yet. Your repository should be clean for us to read, containing the `README.md`, a `doc` folder, pictures in the `doc` folder, an empty `app` folder and nothing else.

## What's next

The next step in your project is creating a design document. There, you'll describe how your project will be created according to the rules of the application framework that you're using.

Meanwhile, keep an eye on the **GitHub Issues** for your project. This is where you will get feedback on whether your project is accepted as it is described, or you need to make some changes.
