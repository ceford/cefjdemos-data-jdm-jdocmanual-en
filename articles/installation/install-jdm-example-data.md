<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/installation/install-jdm-example-data",
  "title": "Install JDM Example Data",
  "description": "Instructions for obtaining and installing the JDM documentation to use as an example.", 
  "author": "Clifford E Ford"
}
-->

Jdocmanual uses source data in Markdown format. To try it out you can download data from GitHub and build a manual yourself. Start with the data set that documents Jdocmanual. There are more datasets in multiple languages for Joomla! documentation.

You will find it best to have a local Joomla installation to work on data preparation and testing and to **Push** finished data to a production site or to GitHub.

## Clone the JDM Repository

After creation of a working Joomla installation and installation of Git you need to decide where to locate your Jdocmanual data repositories. This is normally outside your web site folder tree but within the your own file space. For example: `/home/username/manuals/` or `/Users/username/manuals`. Each manual should have a suitable name within the manuals folder, for example:

- /home/username/manuals/developer
- /home/username/manuals/jdm
- /home/username/manuals/user

This stage of the installation is best accomplished in a terminal window:

- cd ~
- mkdir manuals
- cd manuals
- mkdir jdm
- cd jdm
- git clone https://github.com/ceford/cefjdemos-data-jdm-jdocmanual-en.git
- mv cefjdemos-data-jdm-jdocmanual-en en

You should end up with a file structure that looks like this:

```
/home/username/manuals/jdm
    |---en
        |---.git
        |---articles
            |---introduction.md
            |--- more folders and articles
        |---images
            |---introduction
                |---00-screenshot-of-site-view.png
                |---01-next-image
            |--- more folders and images
        |---folders.json
        |---menu.json
```
Any translation will have an almost identical structure under its own language code (de, fr and so on).

You do not have to use Git! You can download the data as a zip file and unzip it in the correct location.

