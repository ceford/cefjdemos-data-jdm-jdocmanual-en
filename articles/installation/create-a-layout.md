<!--
{
  "source": "https://jdocmanual.org/jdocmnual?article=jdm/installation/create-a-layout",
  "title": "Create a Layout",
  "description": "Instructions on creation of a suitable layout for Jdocmanual.", 
  "author": "Clifford E Ford"
}
-->

Jdocmanual works best in full page mode, although mobile phone views work well too. The following instructions ... are a suggestion.

## Create a Child Template

This is intended to simplify module management, which can become a chore on complex sites.

### Part 1: Start with the Cassiopeia Template

- Go to **System / Site Templates / Cassiopeia Details and Files**
- Use the **Create Child Template** button in the Toolbar.
- In the **Child Template** dialog:
  - Enter a child template name, for example **Cassiopeia_jdocmanual**
  - Select Additional Template Styles: **Cassiopeia Default**
  - Select **Create Child Template**
- At this stage you are still in the original Cassiopeia template.
- Open the **index.php** file, select its contents and copy to the clipboard or to a temporary text file.
- Close the **Templates: Customise (Cassiopeia)** form.

### Part 2: Update the Child Template

- Select the newly created child template: **Cassiopeia_jdocmanual Details and Files**.
- Select the **New File** button.
  - At the top left, select (twice) the name of the new template: **/templates/cassiopeia_jdocmanual**
  - In the **File Name** field enter **index**
  - From the **File Type** list select **.php**
  - Select **Create**
- In the newly created **index.php** file paste the contents of the original index.php file copied to the clipboard.
- Look for lines 106 to 114, 142, 205 to 209 and 221 to 225 - this is where the left and right sidebars are specified.
- Also look for line 212 (breadcrumbs).
- Delete these lines in reverse order or the line numbers will be out of sync.
- There may be others to delete later.
- **Save & Close**

## Create a Menu Item

A default Joomla installation has a Main Menu located in the right side bar. Its **Home** page is a **Featured Articles** blog layout but as there are no articles, featured or otherwise, the Home page is empty apart from the Main Menu and Login modules in the right sidebar.

Create a menu item as follows:

- Go to **Menus / Main Menu** and select the **New** button from the Toolbar.
- Enter the title **Jdocmanual** (the alias must be jdocmanual).
- For the **Menu Item Type** select **Jdocmanual**.

## Create a Custom Module

The top of the page often has a banner but Jdocmanual works best with a Search form In the same row as the site title. A custom module works nicely for that:

- Create a Custom Module
- Set the **Title** field to **Site Name** (it is not used)
- Set the **Title** button to **Hide**
- Set the **Position** to **below-top**
- Toggle the content area so that you can enter plain text and add this HTML:
  ```html
  <div class="navbar-brand">
    <div class="site-logo h2 mb-0"><a href="jdocmanual">Jdocmanual Local</a></div>
    <div class="site-description">A site for Joomla! documentation</div>
  </div>
  ```
- In the **Advanced** tab set the **Module Class** to **flex-grow-1** and the **Module Style** to **noCard**.

## Add a Search Form

- Set the **Title** field to **Search Form**
- Set the **Title** button to **Hide**
- Set the **Position** to **below-top**
- In the **Advanced** tab set the **Module Style** to **noCard**

## Remove Brand from Default template Style

The original Cassiopeia template will have the new custom banner and its original Brand banner. To turn off the latter:

- Go to **System / Site Template Styles**
- Select the **Cassiopeia - Default** style
- In the **Advanced** tab set **Brand** to **No**

## Site View

Check that the site view suits your purpose and behaves as you expect.


