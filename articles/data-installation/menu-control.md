<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/data-installation/menu-control",
  "title": "Menu Control",
  "description": "The files used for menu building in Jdocmanual.", 
  "author": "Clifford E Ford"
}
-->

The menu used by Joomla is created from entries in a human readable `menu.json` file in the root of the default language data set for the manual. Translations use this *default* menu but obtain article titles from translated articles if they exist.  

## Structure of a *menu.json* file

The articles included in a manual appear in the order in which they appear in the menu.json file. The structure of the menu is set by nesting folders as required, for example:

```
{
    "introduction.md" : "Introduction",
    "notes.md" : "Notes",
    "data-installation" : {
        "file-system-layout.md" : "File System Layout",
        "menu-control.md" : "Menu Control",
        "markdown-files.md" : "Markdown Files",
        "image-naming-conventions.md" : "Image Naming Convention"
    },
    "jdocmanual" : 
    {
        "introduction-to-jdocmanual.md" : "Introduction to Jdocmanual",
        "jugl-2025-05-20.md" : "JUGL Presentation",
        "installation-notes.md" : "Installation Notes",
        "source-data.md" : "Source Data",
        "how-to-contribute.md" : "How to Contribute",
        "markdown.md" : "Markdown",
        "edit-in-vscode.md" : "Edit with VSCode",
        "edit-article-in-jdocmanual.md" : "Edit Article in Jdocmanual",
        "new-article-in-jdocmanual.md" : "New Article in Jdocmanual",
        "menu-items.md" : "Menu Items",
        "proxy-server.md" : "Proxy Server",
        "changelog.md" : "Changelog",
        "translation-analysis.md" : "Translation Analysis"
    }
}
```
The folder names come from a `folders.json` file, for example:

```
{
    "jdocmanual" : "Jdocmanual",
    "data-installation" : "Data Installation"
}
```
