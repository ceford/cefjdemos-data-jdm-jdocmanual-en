<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/data-installation/file-system-layout",
  "title": "File System Layout",
  "description": "The repository layout for a Jdocmanual source manual.", 
  "author": "Clifford E Ford"
}
-->

Manual source files in Markdown format are located outside a web site file system tree so that they cannot be accessed directly from the internet. Each source may be a git repository, either a source itself or a clone of a remote source.

## Common Source Location 

If there are several manuals or several translations of a manual they should be kept in a `manuals` folder. The location of the manuals folder is kept as a Jdocmanual configuration parameter that must be entered before any source data can be used. The following list shows an installation with several manuals and one with several translations:

```
/home/username/manuals/docus/en/...
/home/username/manuals/jdm/de/...
/home/username/manuals/jdm/en/...
/home/username/manuals/jdm/fr/...
/home/username/manuals/users/en/...
/home/username/manuals/wiki/en/...
```

## Single Manual and Language Structure

The following schematic diagram shows the essentials of a manual source using this source as an example:

```
jdm
    |---en
        |---articles
            |---data-installation
                |---file-system-layout.md
                |---image-naming-conventions.md
                |---markdown-files.md
                |---menu-control.md
            |---another-folder
                |---another-file.md
            introduction.md
        |---images
            |---data-installation
                |---file-system-layout
                    |---00-first-image-in-article.png
                    |---01-second-image-in-article.png
            |---introduction
                |---00-site-example.png
        folders.json
        menu.json
```
## The *articles* Files

In an IDE the folders and files will be listed in alphabet order as in this page in VSCode:

![structure seen in vscode](../../../en/images/data-installation/file-system-layout/00-structure-seen-in-vscode.png)

The content structure of each article file is covered later in the article on Markdown.

The final menu order is controlled by the menu.json file with folder names coming from the folders.json file. It is best not to go more than three folders deep or users will find it difficult to remember where articles are located. 

## The *images* Files

Images are located in a separate tree from article markdown files. A translated article may then select the original image or a translated image, if it exists, just by changing the language code. Image links have the following syntax in the article markdown source:

&#33;&#91;structure seen in vscode&#93;(../../../en/images/data-installation/file-system-layout/00-structure-seen-in-vscode.png)

Hover over the link and VSCode will show a thumbnail of the image. Select Preview mode and VSCode will show the image full size within the rendered preview text.

Images are converted to a set of responsive images in a picture tag in the final HTML output.

