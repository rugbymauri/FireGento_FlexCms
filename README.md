FireGento_FlexCMS
=====================
This extension makes adding content much easier and enhances the category navigation.

Facts
-----
- version: 0.1.0
- [extension on GitHub](https://github.com/magento-hackathon/FireGento_FlexCms)


Description
-----------
Improve Magento's default CMS capabilities by using FlexCMS elements.

FlexCMS elements can be used on:

- CMS pages
- Category pages
- Product pages

Features

- Insertion/Creation of FlexCMS elements from backend (i.e. category management)
- Customizable and extendable FlexCMS element renderers

Adds new ready-to-go content type:

- Simple Text-Element (WYSIWIG)

Miscellaneous

- Adds an option to link categories to external URLs

## Installation
Install the files using one of the following methods:

### Via modman
- Install [modman](https://github.com/colinmollenhour/modman)
- Use the command from your Magento installation folder: `modman clone https://github.com/magento-hackathon/FireGento_FlexCms`


### Manually
You can copy the files from the 'src' folder of this repository to the same folders of your installation

Once the files are installed:

- Clear the cache, logout from the admin panel and then login again.

## Uninstallation
- Remove all module files
- Run the following SQL queries:

```sql
DELETE FROM eav_attribute WHERE attribute_code LIKE 'flexcms%';
UPDATE eav_attribute SET source_model = 'catalog/category_attribute_source_mode' WHERE attribute_code = 'display_mode';
DROP TABLE flexcms_content;
DROP TABLE flexcms_content_link;
DELETE FROM core_resource WHERE code = 'firegento_flexcms_setup';
```

Requirements
------------
- PHP >= 5.3.0

Compatibility
-------------
- Magento >= 1.6

Support
-------
If you have any issues with this extension, open an issue on [GitHub](https://github.com/magento-hackathon/FireGento_FlexCms/issues).

Contribution
------------
Any contribution is highly appreciated. The best way to contribute code is to open a [pull request on GitHub](https://help.github.com/articles/using-pull-requests).

Developer
---------
- Website: https://github.com/orgs/magento-hackathon/teams/flexcms

Licence
-------
[GNU General Public License, version 3 (GPLv3)](http://opensource.org/licenses/gpl-3.0)

Copyright
---------
(c) 2014 FireGento
