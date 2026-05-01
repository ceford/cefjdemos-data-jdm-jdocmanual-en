<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/installation/clone-jdm-repo",
  "title": "Clone the JDM Repo",
  "description": "Instructions for obtaining a copy of the JDM documentation.", 
  "author": "Clifford E Ford"
}
-->

After creation of a working Joomla installation and installation of Git you need to decide where to locate your Jdocmanual data repositories. This is normally outside your web site folder tree but within the your own file space. For example: `/home/username/manuals/` or `/Users/username/manuals`. Each manual should have a suitable name within the manuals folder, for example:

- /home/username/manuals/jdm
- /home/username/manuals/user

This stage of the installation is best accomplished in a terminal window:

- cd ~
- mkdir manuals
- cd manuals
- git clone https://github.com/ceford/cefjdemos-data-jdm-jdm-en.git (check this)
- mv repoLongName repoShortName

The repoShortName will appear in article links and throughout the Jdocmanual management of the repo data. In this case the repoShortName is jdm. You should end up with a file structure that looks like this:

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
