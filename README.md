# WhoColor-updates
This userscript updates the [WhoColor](https://github.com/wikiwho/WhoColor) userscript.
# Installation
Install the userscript using ``Tampermonkey`` or ``Greasemonkey`` for Chrome and Firefox:

* First install one of:
    * [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo/) for Chrome
    * [Tampermonkey](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/) for Firefox
    * [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) for Firefox
* Open [userscript](https://github.com/kiku2333/WhoColor-updates/blob/master/WhoColor-updates.user.js) and click on ``Raw`` button on the top right (as shown in the images)
![Screenshot](/screenshot/new-raw-button.JPG)
* ``Tampermonkey`` or ``Greasemonkey`` will automatically detect the user script and ask to install it
* Open an article in Wikipedia and now you should see the ``WhoColor`` to the left of the default "Read" tab in the head navigation of the articles

# WhoColor Tabs
The updated WhoColor contains 5 tabs. ``Provenance``, ``Conflict`` and ``Age`` are from the original WhoColor. ``Camps`` and  ``Warring Camps`` are added in this update version.\
**<br />Note: There is a selection part above the tabs. This part is used for testing, and will be removed later. The selection part allows you to select the mode. TCM shows the results obtained with TCM articles. All Data shows the results obtained with all data. Finally we will remove the TCM part, since it only used for testing.<br /><br />Currently, you need to manually select the mode and click on the change mode button to load the data. If the chagne mode is not clicked, the results for Camps and Warring Camps will not shown.**
* [TCM result](/clusterResult) is stored in this repository under clusterResult folder.
    * The csv files with -after-join are the results used in the plug in.
    * The csv files without -after-join are the original cluster result without joining similar groups
    * TCM-user-cluster-result-after-join.csv stores user group info. This result is used in Camps tab.
    * TCM-mutual-and-min-revert-after-join.csv stores mutual revert and minimum revert info between each pair of groups. This result is used in Warring Camps tab.
* [All Data result](https://github.com/kiku2333/wikipedia-project) is still not updated. Currently it is stored in another repository, and will be updated later. 

## Added Tabs
* ``Camps``: Shows the user group result. 
    * The right bar lists all groups found for current page with its percentage of contribution.
    * Click on the plus sign before group name to expand/collapse the group. The editors in this group who contributed to this article will be shown after expand the group. Some editors' name are not shown completely, move the mouse to the editor to show full name. 
    * Click on the group name on the right bar to color/uncolor the group and its corresponding tokens. The max number of color allowed are 20. Top 3 groups are colored automatically once the tab is open.
    * The tokens added by anonymous editors are shown in light gray. 
    * All colored tokens will be removed if the tab is closed.
* ``Warring Camps``: Shows the group conflict result. 
    * The right bar lists all groups found for current page with its percentage of contributions.
    * Click on the plus sign before group name to expand/collapse the group. The fighting groups will be shown after expand the group. The fighting groups are sorted by mutual revert. The fighting groups with a mutual revert less than 3 is ignored. 
    * Mutual revert is the number of times two groups revert each other. (sum of groupA revert groupB and groupB revert groupA)
    * Click on the group name on the right bar to color/uncolor the group and its corresponding tokens. Only 1 colored group is allowed.
    * The tokens are colored with different brightness. The brightness is determined by the number of times the token is edited by current group's fighting groups. Darker color indicates more edits, lighter color indicates less edits.
    * Click on the fighting groups to color/uncolor the fighting groups and its corresponding tokens. The color is a contrast color with the parent group. The fighting groups with larger mutual revert has a darker color. 
    * The tokens added by anonymous editors are shown in light gray. 
    * All colored tokens will be removed if the tab is closed.

