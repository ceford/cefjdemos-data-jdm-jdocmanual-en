<!--
{
  "source": "",
  "title": "Temporary Notes",
  "description": "Temporary Notes", 
  "author": ""
}
-->

## Search / Replace Metadata

The metadata at the top of each markdown file changed from Jdocmanual Version 4 to Versions 5. The following regular expressions can be used in VSCode to batch convert all articles in a manual:

Search:
```
<!-- Filename:\s*(.*?)\s*\/.*Display title:\s*(.*)\s*-->
```
Replacement:
```
<!--
{
  "source": "https://docs.joomla.org/$1",
  "title": "$2",
  "description": "", 
  "author": ""
}
-->
```
