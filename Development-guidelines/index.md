---
title: Development guidelines
---

# Development guidelines

First see [Software standards of EEA and Eionet](http://www.eionet.europa.eu/software/swstandards) (OBS: obsolete link see [issue #1](https://github.com/eea/docs/issues/1)) for general guidelines on developing software for the EEA and Eionet.

## Design

EEA products must follow the [EEA corporate design manual](http://www.eea.europa.eu/publications/eea-corporate-design-manual), and also use the [web design elements](http://www.eea.europa.eu/code/design-elements) for web based products.

Eionet web based products must follow the Eionet [Website Design Guidelines](http://www.eionet.europa.eu/software/design).

## Development methodology

All development work should be recorded in our task management system [Taskman](https://taskman.eionet.europa.eu).

The methodology to follow is a blend of Scrum and Kanban, see [Working with tickets in Taskman](https://taskman.eionet.europa.eu/projects/netpub/wiki/Working_with_tickets_in_Taskman_(Flow)) for a guide on the workflow.

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

## Licensing

The license to be used for our projects is the [Mozilla Public License v2](https://www.mozilla.org/en-US/MPL/) or the compatible more used [GNU General Public License v3, GPLv3](http://www.gnu.org/licenses/gpl-3.0.en.html), see the historical [explanation on the initial choice of the license](http://www.eionet.europa.eu/software/licenseexplained.html).

## Source code management

Our software is managed on GitHub within the [EEA organisation account](https://github.com/eea). For legacy reason, some software is still also managed in Subversion on the [Eionet SVN server](http://svn.eionet.europa.eu/).

The software is built and tested with our continous integragation (CI) tool [Jenkins](http://ci.eionet.europa.eu/).

