<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-nanagement/data-flow-options",
  "title": "Data Flow Options",
  "description": "Jdocmanual is a Joomla component designed for the display of multi-lingual technical information.", 
  "author": "Clifford E Ford"
}
-->

The data used in Jdocmanual articles are located in Markdown format files. There are many possible ways to manage those files. How to create and update them, how to approve contributions from co-workers, and so on. 

This article uses three manuals in use in Jdocmanual to illustrate three approaches to data management by an individual, me. So this is about what I do. Others may choose a different approach.

## Case 1: The Joomla User Manual

The data for the Joomla User Manual as presented in Jdocmanual originated in the [Joomla Documentation Wiki](https://docs.joomla.org). The data there are published under the Joomla Electronic Documentation Licence (JEDL), which allows re-use elsewhere to promote the Joomla CMS. 

I extracted user-related articles relevant for Joomla 4 onwards and converted them to GitHub Flavoured Markdown (GFM). My working copy of the markdown files is located on the laptop computer I use for testing and development purposes. I use Git to keep track of changes. There is a master copy of of the markdown files located in an upstream git repository on GitHub. That is considered the **origin** as it can be forked, cloned or downloaded by anyone who would like to use the data.

There is a clone of the Github repository in my [Jdocmanual](https://jdocmanual.org) site. The date there is pulled from the GitHub repository.

When I need to add or change an article this is the procedure I use:

  1. Make changes to the markdown file on my laptop.
  2. Build my local copy of Jdocmanual in my test installation of Joomla.
  3. Check there are no problems in the new or revised article.
  4. **Commit** the changes to my local repository and **Push** them to the GitHub repository.
  5. Go to the Administrator menu of my Jdocmanual site and select the Jdocmanual / Manuals item.
  6. **Pull** the changes from GitHub to the Git repository in the Jdocmanual site.
  7. Build the production copy of the manual.
  8. Check the changes are as expected in the production site.

Summary of data flow:

- Push the local Git repository on my development laptop to GitHub.
- Pull the GitHub repository to the clone on my production site.

## Case 2: The Joomla Programmers Documentation

The official documentation for programmers was created at about the same time that Jdocmanual appeared and also used content from the Wiki. However, it uses Docusaurus, a document management system that uses markdown files to generate static HTML files. It is fine, but there is no obvious mechanism for translation and it is not possible to search for *User* information and *Programmer* information at the same time. For that reason, I decided to import the Joomla Programmers Documentation into Jdocmanual as an additional manual. The content uses the JEDL license.

The Joomla! Programmers Documentation source files are located in a GitHub repository. I have a local clone of that repository and a short PHP script used to transform the data into the structure used by Jdocmanual. When ready, there is an upstream repository on the Jdocmanual site to which data is pushed from my local repository.

This is my procedure to update my version of the Joomla Programmers Documentation (JPD):

1. In my local clone of the JPD, Pull changes from GitHub.
2. Process my local JPD clone to update my own JPD repository.
3. Build my local version of the JPD in Jdocmanual.
4. Check for any problems in the changed or new articles.
5. Push changes from my local JPD repository to an upstream JPD repository in my Jdocmanual production site.
7. Build the production copy of the manual.
8. Check the changes are as expected in the production site.

Summary of data flow:

- Pull the GitHub repository to the local clone on my development laptop.
- Import my local docusaurus clone into my local jdocmanual master repository.
- Push my local master repository to the production site repository.

## Case 3: The Joomla Magazine

Each month the [Magazine](https://magazine.joomla.org/) has several articles containing information of a tutorial nature. For several years I have kept a list of such articles in the [Wiki](https://docs.joomla.org/J4.x:Magazine_Articles). However, I found it increasingly difficult to remember where I had seen an article on any particular topic. Magazine articles are not published under the JEDL license so I cannot republish them in Jdocmanual without the permission of each author. However, I can include them as a manual to make them searchable and provide a link to the original article. And I can see the content on my local installation. I do that frequently to help answer questions in the Joomla Forums.

To import selected articles from the Magazine I have a short PHP script that imports HTML and converts that to Markdown. I need to do quite a lot of editorial work on each article to ensure compliance with accessibility standards. I also provide a brief summary of the article content as the titles are sometimes obscure.

This is my procedure for adding Magazine articles to Jdocmanual after publication each month.

1. Extract the HTML content of a selected article.
2. Convert HTML to Markdown in my local repository.
3. Download images individually.
4. Build my local version of the Magazine articles in Jdocmanual.
5. Check for any problems in the new articles.
6. Push the changes from my local magazine Git repository to my Jdocmanul production site.
7. Build the production copy of the magazine.
8. Check the changes are as expected in the production site.

Summary of data flow:

- Transfer article content from the Magazine site to my local Git repository.
- Push my local repository to the upstream repository on my Jdocmanual production site.

## A note on Repositories

Each manual and language uses a separate repository. So the Joomla! Programmers Documentation in English requires one repository. The Joomla Users Manual in 8 different languages requires 8 repositories. You can find them all on GitHub. 