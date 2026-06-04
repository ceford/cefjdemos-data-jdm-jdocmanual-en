<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-management/menu-file-structure",
  "title": "Menu File Structure",
  "description": "Description of the structure required in a menu JSON file.", 
  "author": "Clifford E Ford"
}
-->

The menu for each manual is stored in a JSON format file in the root of the default language manual. There is also a folder names file stored in JSON format. Both are shown below. The menus for secondary languages use the default language for structure but take the article titles from the articles themselves and the folder names from a language-specific folder names file in JSON format.

## The menu.json File

This is the menu.json file for this manual:

```
{
    "introduction.md" : "Introduction",
    "notes.md" : "Temporary Notes",
    "installation" : {
        "install-jdm-example-data.md" : "Install JDM Example Data",
        "install-jdocmanual.md" : "Install Jdocmanual",
        "configure-languages.md" : "Configure Languages",
        "build-a-manual.md" : "Build a Manual",
        "smart-search.md" : "Smart Search",
        "create-a-layout.md" : "Create a Layout",
        "help-proxy-server.md" : "Help Proxy Server"
    },
    "data-management" : {
        "file-system-layout.md" : "File System Layout",
        "data-flow-options.md" : "Data Flow Options",
        "data-entry-in-vscode.md" : "Data Entry in VSCode",
        "data-entry-in-jdocmanual.md" : "Data Entry in Jdocmanual",
        "user-groups-in-jdocmanual.md" : "User Groups in Jdocmanual",
        "article-file-structure.md" : "Article File Structure",
        "menu-file-structure.md" : "Menu File Structure",
        "image-naming-conventions.md" : "Image Naming Conventions"
    },
    "reference" : {
        "changelog.md" : "Changelog",
        "markdown.md" : "Markdown",
        "magazine-author-license.md" : "Magazine Author License"
    },
    "blog-posts" : 
    {
        "jugl-2025-05-20.md" : "JUGL Presentation"
    }
}
```

## The folders.json File

This is the folders.json file for this manual:

```
{
    "blog-posts" : "Blog Posts",
    "installation" : "Installation",
    "data-management" : "Data Management",
    "data-installation" : "Data Installation",
    "reference" : "Reference"
}
```
