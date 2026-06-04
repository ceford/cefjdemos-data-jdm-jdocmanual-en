<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-management/user-groups-in-jdocmanual",
  "title": "User Groups in Jdocmanual",
  "description": "How to set up users and user groups to contribute to Jdocmanual.", 
  "author": "Clifford E Ford"
}
-->

If you wish to allow others to help maintain content you may need to create two User Groups:

- **JDM Author** Allowed to edit content in the default language and other languages.
- **JDM Publisher** Allowed to commit and publish updated content.

## Setting Permissions

The **JDM Author** group should have Public as its parent. The **JDM Publisher** group should have **JDM Author** as its parent.

### Users: Viewing Access Levels

**JDM Author** should be set to the Special Viewing Access level.
From the Users / Access Levels page select `Special` and add `JDM
Author` to the User Groups with Viewing Access.

### Global Options

In the Global Options form select the Permissions tab and then the
**JDM Author** item. Set Administrator login to *Allowed*.

### Jdocmanual Options

From the Jdocmanual, Manual page select the Options button. In the
Permissions list select **JDM Author** and set the following to
Allowed: - Access Administration Interface - Create - Delete - Edit

Select **JDM Publisher** and set the following to Allowed: - Publish

Save and Close

If you now login as a user in the **JDM Author** group you will see
the Home Dashboard with some modules not relevant for Jdocmanual.

### Turn off the Help menu item

Go to the list of Administrator modules and find the Administrator Menu
module. In the Module tab set the Help Menu item to Hide.

### Unpublish or restrict Access to modules

In the Administrator modules list find the Logged-in Users item used in
the cpanel position (not the cpanel-users position). Either Unpublish it
or set Access to Super Users.

Find and unpublish the Popular Articles and Recently Added Articles
items for the cpanel position (not the cpanel-content position).

There may be other modules needing similar treatment.

The Home Dashboard should now be empty for a **JDM Author**.

## Who can do what?

**JDM Author** and **JDM Publisher** can login but should only
have access to the the Home Dashboard and the Jdocmanual component.

**JDM Author** does not have access to the Commit button in the
Article Edit page toolbar so cannot update the git repository or
displayed page. Otherwise each can use all other features.

**Manager** and **Administrator** can login but will not see the
Jdocmanual component.

**Author**, **Editor** and **Publisher** do not have access
to the Administrator interface.

**Super Users** have complete access.
