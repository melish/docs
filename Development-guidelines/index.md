---
title: Development guidelines
---

# Development guidelines

## Development methodology

All development work should be recorded in our task management system [Jira](https://jira.osha.europa.eu).

## Our solutions and specific practices
 
* ### Making patches to Drupal core and 3rd party modules
    * Patches used in project to fix errors found in Drupal core or 3rd party modules.
    * Patches can be created manually using _git diff_ command `````git diff filenames > patch.name````` or found on module issue page
    * Each patch should be copied in `patches/module_name` folder
    * Before updating module require to check if module patched. After updating module require to check if patch still required. 
    * To apply patch after module update require to run ```patch -p1 < ../patches/module/file.patch``` 
    * If module patch failed to apply require to merge manually and check if for compatibility.      

* ### Updating custom modules
    * Content type module uses features module to make possible automated import and export of configuration.
    * Any configuration changes related to module updating in module `module_name_update_70XX` hook using `features_revert` or `features_revert_module` functions   

## General versioning and release approach

### Branches

This repo branching model follows the article ["A successful Git branching model"](http://nvie.com/posts/a-successful-git-branching-model)

Summary:

* _develop_ - Main development branch. Tests are performed on this branch
* _release_ - Release branch.
* _master_ - The production branch, updated with each release.

### Release and deployment:

Release and deployment follows the article ["Release and deployment policy"](https://github.com/EU-OSHA/osha-website/wiki)

Summary:

* We have 2 weeks based (first week staging deploy and second week production deploy) release model.
* New functionality will be added in develop branch.
* After testing develop branch will be merged into release branch using GitHub `Pull requests` and created new release using GitHub `Releases`
* In a week we merge release changes into master branch. The same GitHub `Pull requests` and GitHub `Releases`


## Licensing

The license to be used for our projects is the [Mozilla Public License v2](https://www.mozilla.org/en-US/MPL/) or the compatible more used [GNU General Public License v3, GPLv3](http://www.gnu.org/licenses/gpl-3.0.en.html), see the historical [explanation on the initial choice of the license](http://www.eionet.europa.eu/software/licenseexplained.html).

## Source code management

Our software is managed on GitHub within the [EU-OSHA organisation account](https://github.com/EU-OSHA).
