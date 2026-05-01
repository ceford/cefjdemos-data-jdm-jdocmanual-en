<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/installation/build-a-manual",
  "title": "Smart Search",
  "description": "Instructions setting up Smart Search in Jdocmanual.", 
  "author": "Clifford E Ford"
}
-->

Smart Search is an important feature of Jdocmanual. It was one of the reasons for bringing together various Joomla document sources in one place. After installation, the **Smart Search - Jdocmanual** plugin needs to be enabled.

## Run the Indexer after Updates

The Manual build process writes HTML directly to a database table without triggering an onAfterSave event. So at the moment it is necessary to run the Smart Search Indexer manually after updating. 

- Go to **Components / Smart Search / Index** in the Administrator menu.
- Select **Index / Index** from the Toolbar. 
- Wait! First time indexing of a large Manual may take a long time. Later re-indexing is much quicker.

When you type two characters in the search form you should see words beginning with those two characters with progressive filtering with each additional character entered.
