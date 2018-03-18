---
title: Build application forms with Plone
---
#  Build application forms with Plone


<small class="github">[Corporate-Vacancies](https://github.com/EU-OSHA/Corporate-Vacancies)</small>

osha.applicationform is a minimalistic Plone add-on that builds on top of the
PloneFormGen product to enable you to build forms on the EU-OSHA site, under
the 'vacancies' section, so that the applicant can send the CV and the
motivation letter via Web.

  * [Source code @ GitHub](http://github.com/syslabcom/osha.applicationform)
  * [Releases @ PyPI](http://pypi.python.org/pypi/osha.applicationform)
  * [Continuous Integration @ Travis-CI](http://travis-ci.org/syslabcom/osha.applicationform)

##  Installation

To install `osha.applicationform` you simply add `osha.applicationform` to the
list of eggs in your buildout, run buildout and restart Plone. Then, install
osha.applicationform using the Add-ons control panel.

###  Importing HR Application Form

Theoretically it should be possible to import the form and its fields
automatically with the 'content' GS profile using the structure folder. But
there are some errors when running the profile, so currently the form must be
imported manually.

File hr-application-form.tar.gz in profiles/content contains the exported form
with all the fields.

Steps for importing the form:

  * Create a new Form Folder named 'HR Application form' (it is important that the form id is 'hr-application-form' or 'hr_application_form' to make the rdb integration work)
  * Change the form view by clicking on "Display -> HR Application Form"
  * Click on "Actions -> Import"
  * Select file "hr-application-form.tar.gz"
  * Check "Remove Existing Form Items?"
  * Click "import"

XXX: At the moment, there are some additional manual steps needed to make the
form work properly:

  * Click on 'Add new -> RDBPloneFormGenAdapter' and enter `osha.applicationformdb` in the 'Database utility name' field, then click 'Save'
  * Click on 'Actions -> Rename' and rename the adapter to `rdb-adapter`
  * Go back to the form, click on 'QuickEdit' tab and make sure that RDB Action Adapter is enabled.
  * On the 'Contents' tab, click on the 'Languages' field.
  * Click 'Edit', then check options 'Allow Row Deletion', 'Allow Row Insertion' and 'Allow Row Reordering'
  * Click 'Save'.

###  Setting up RDB

HR Application Form uses relational database to store the data. There are two
sql scripts in resources/, which should be used to create initial db
structure. Currently sqlite and postgresql are supported.

Instructions for creating tables in postgresql (you need to create a database
beforehand):

    
    
    $ psql -d database_name -a -f hr_form_postgres.sql
    

Then you need to set the connection string in your buildout:

    
    
    [instance]
    ...
    zope-conf-additional =
    <product-config osha.applicationform>
        hr.database postgresql://username:password@ip/database_name'
    </product-config>
    

##  Requirements

>   * [Plone](http://plone.org/) 4.1 or newer

>   * [PloneFormGen](http://plone.org/products/ploneformgen) 1.7 or newer

>

##  Usage

TODO

[Edit this page](https://github.com/EU-OSHA/Corporate-Vacancies/edit/master/README.rst)
