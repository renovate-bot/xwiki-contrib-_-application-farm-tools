# Farm Tools

This is a bundle of tools for XWiki farm administrator.
The bundle is actually composed of:
 * Farm importer
 * Farm property updater

* Project Lead: [Denis Gervalle](https://www.xwiki.org/xwiki/bin/view/XWiki/dgervalle)
* [Documentation & Downloads](https://extensions.xwiki.org/xwiki/bin/view/Extension/Farm%20Tools)
* [Issue Tracker](https://jira.xwiki.org/browse/FARMTOOLS)
* Communication: [Mailing List](http://dev.xwiki.org/xwiki/bin/view/Community/MailingLists), [IRC](http://dev.xwiki.org/xwiki/bin/view/Community/IRC)
* [Development Practices](http://dev.xwiki.org)
* Minimal XWiki version supported: XWiki 7.4
* License: LGPL 2.1
* Translations: N/A
* Sonar Dashboard: N/A
* Continuous Integration Status: N/A

Farm Importer
-------------

Ease importing a XAR package on multiple wikis.

Instructions:

* Attach the desired .xar to the FarmTools.FarmImporter page
* Autocomplete will help you while you type in the xar input of the form
* You can start the xar import on the selected batch of wikis by pressing the 'Start' button. You can also cancel
  the operation on the upcoming wikis by pressing the 'Cancel' button

Farm Property Updater
---------------------

Batch property updater for objects in multiple wikis.
It is currently splitted in two separate tools:
 * Farm Field Value Updater (FarmTools.FarmFieldValueUpdater)
 * Farm Preferences Updater (FarmTools.FarmPreferencesUpdater)

Both tools allows to change the value of a given object property from one value to another. You select the name of
the document containing the object to change (without wiki prefix), and the same document in all wikis will get its
object property updated. The object selected is always the first object matching the object class to be updated.

In the Farm Field Value Updater, you can freely choose the object class you want to update, and you can set a constant
value to one of its properties.

In the Farm Preferences Updater, the object is always of class 'XWiki.XWikiPreferences', so only properties of this
class could be updated. The update is done using a regex and a replacement value, so you have the ability to manipulate
the existing value to produce the new one.
Additionnaly, in this second tool, there is a special property named "doc.parent", which allows you to update the parent
of any choosen document using the same regex mechanism.
