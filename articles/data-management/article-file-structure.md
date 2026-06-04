<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-management/article-file-structure",
  "title": "Article File Structure",
  "description": "Description of the structure required in an article markdown file.", 
  "author": "Clifford E Ford"
}
-->

The markdown format file used for each article has metadata at the top enclosed in HTML comments. This is not displayed in the article but is used in its management.

## Metadata Format

The metadata at the top of each article is in JSON format. This is the metadata for this article:

```html
<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-management/article-file-structure",
  "title": "Article File Structure",
  "description": "Description of the structure required in an article markdown file.", 
  "author": "Clifford E Ford"
}
-->
```

In the future there may be additional items. The order does not matter. The current items are as follows:

- **source** The original source of this article - not currently used but available for consultation.
- **title** The title of the article, used for the menu and for translation. This may be duplication but it is important to have a short menu title where the article title is long.
- **description** This is intended for use in the description element at the head of the page. ToDo!
- **author** This field allows credit for one or more authors. It may be empty - original Wiki articles had no formal record of authorship and often had many contributors.

Take very great care to preserve the JSON formatting! Any error is likely to cause omission of the file or changes to it from the manual.

## The Preamble

On output, each article begins with a H1 Title taken from the Menu. The first part of an article should be an introductory paragraph summarising what the article is about. It is what might come before a *Read More* separator in a Joomla article or what might be in the *Abstract* of a scientific paper. 

## Headings

The preamble should be followed by the first H2 heading, trying not to duplicate what is in the title. Headings give an article structure and appear in the *In this Article* column at the right. Headings should not be duplicated as this leads to accessibility violations. Make sure that headings do not skip a level. Following H2 with H4 is wrong, although following H4 with H2 is fine. 

Avoid special symbols in headings ToDo: check.

## Images

In markdown, image links start with an exclamation mark followed by two segments enclosed in square and round brackets:

!&#8203;[site example screenshot]&#8203;(../../en/images/introduction/01-site-example.png)

The part within square brackets `[...]` becomes the **alt** text so make sure it makes sense for a screen reader. The part within round brackets `(../../en/images/folder/file.png)` is a link that in VSCode will show the image on hover and in preview. It is converted to a real link during the article build process. 

There is one more level of `../` for each additional folder in the structure.
