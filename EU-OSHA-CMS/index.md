---
title: EU-OSHA CMS platform
---

## Introduction

## Getting started for users

## Getting started for developers

## Features and architecture overview

### Main features

### EU-OSHA tools

#### 1 Issue tracker
EU-OSHA has its own issue tracker tool (Jira). This tool is used for the tracking of issues with all the
contractors for all the projects (development, maintenance, service desk…).

#### 2 Versioning
GitHub is the tool used by EU-OSHA for versioning: https://github.com/EU-OSHA. All the code
developed for EU-OSHA projects should be stored in EU-OSHA repository.

#### 3 Statistics
Matomo (Piwik)is the tool used for statistics. EU-OSHA has its own instance of Matomo.

#### 4 Monitoring
The monitoring is done with an online tool.

#### 5 User Management
LDAP is the tool used by EU-OSHA for centralizing the user management for the various hosted
websites:
* Corporate website
* Healthy workplaces campaign
* Napo
* OiRA
* Vesafe
* OSH Wiki
* Dangerous substances

### Architecture overview

#### EU-OSHA existing websites and applications

Application<br>Website | URLs | Technology <br>/ Hosting | Description
-----------------------|------|--------------------------|------------
Corporate<br>website | https://osha.europa.eu/ | Drupal / External Hosting | Corporative website with all<br>EU-OSHA content and<br>services.<br>
Archive<br>Corporate | https://archives.osha.europa.eu/ <br> Internal only | Plone /<br>EU-OSHA<br>Hosting | Archive of some of the<br>previous EU-OSHA websites
Campaign<br>16-17 | https://healthyworkplaces.eu/previous/allages-2016/ | Drupal /<br>External<br>Hosting | Website dedicated to HWC<br>16-17:<br>Healthy workplaces for All<br>ages.
Campaign<br>18-19  | https://healthy-workplaces.eu | Drupal /<br>External<br>Hosting | Website dedicated to HWC<br>18-19:<br>Dangerous Substances.
OIRA<br>Website | http://www.oiraproject.eu/ | Drupal /<br>External<br>Hosting | Website which gives<br>information about the OiRA<br>project and risk assessment<br>in general
OIRA<br>Tool | https://client.oiraproject.eu/ | Plone /<br>External<br>Hosting | OIRA Web application<br>enabling micro and small<br>organisations to perform risk<br>assessments.<br>An ‘Admin’ site for the<br>creation of sectorial and<br>multilingual OiRA tools
OSHWiki | https://oshwiki.eu/ | MediaWiki /<br>External<br>Hosting | Wiki with a repository of OSH<br>terms, which aims to provide<br>authoritative, in-depth,<br>multilingual and easily update<br>information on OSH.<br>
NAPO | https://www.napofilm.net/ | Drupal /<br>External<br>Hosting | Website devoted to the<br>animated character Napo,<br>who helps to highlight the<br>hazards in the workplaces.
DVT<br>ESENER | https://osha.europa.eu/en/surveys-and-statisticsosh/esener/2009<br>https://osha.europa.eu/en/surveys-and-statisticsosh/esener/2014 | R code /<br>External<br>Hosting | Interactive survey dashboard<br>which allows to visualise and<br>share ESENER data<br>exploring the responses to a<br>selection of questions of<br>ESENER in detail, by<br>country, sector type and<br>establishment size<br>(ESENER1 for 2009,<br>ESENER 2 for 2014).
DVT<br>Ageing and<br>OSH | https://visualisation.osha.europa.eu/ageing-and-osh#!/ | Pentaho /<br>External<br>Hosting | Interactive data visualisation<br>tool which allows the users to<br>explore how European<br>countries deal with the<br>challenge of ageing at work<br>
DVT<br>OSH Costs | https://visualisation.osha.europa.eu/osh-costs#!/ | Pentaho /<br>External<br>Hosting | Interactive data visualisation<br>tool about the costs<br>estimates of OSH.<br>
DVT<br>EU-OSH<br>infosystems | Not live | Pentaho /<br>External<br>Hosting | Interactive data visualisation<br>tool about OSH figures in the<br>EU at country level<br>
eGuide<br>Stress | http://eguides.osha.europa.eu/stress/ | Articulate<br>Storyline /<br>External<br>Hosting | This e-guide provides<br>employers with a source of<br>information about Managing<br>Stress and Psychological<br>Risks at Work.
eGuide<br>All Ages | http://eguides.osha.europa.eu/all-ages/ | Drupal /<br>External<br>Hosting | This e-guide provides<br>practical information, tips and<br>examples related to the<br>ageing of the workforce and<br>the opportunities it brings<br>along. It also shows how agerelated<br>challenges can be<br>addressed at work.
eGuide<br>Dangerous<br>Substances | http://eguides.osha.europa.eu/dangerous-substances/ | Drupal /<br>External<br>Hosting | Online questionaire to<br>manage dangerous<br>substances at the workplace
Vesafe | https://eguides.osha.europa.eu/vehicle-safety/ | Drupal /<br>External<br>Hosting | An e-guide to good practice<br>to reduce work related<br>vehicle risks in the EU.
CRM | https://euoshacontacts.osha.europa.eu/ | MS Dynamics<br>/ Hosted by<br>EU-OSHA | CRM contact database is a<br>collection of all the contacts<br>of the Agency.
Extranet | http://extranet.osha.europa.eu/ | Plone /<br>Hosted by<br>EU-OSHA | Repository used to exchange<br>documentation with<br>stakeholders.
Virtua<br>RMS | Internal only | Power Builder<br>/ Hosted by<br>EU-OSHA | EU-OSHA Record<br>Management System.
Virtua<br>Intranet | Internal only | MS<br>SharePoint /<br>Hosted by<br>EU-OSHA | EU-OSHA Intranet.
Virtua<br>Workspaces | Internal only | MS<br>SharePoint /<br>Hosted by<br>EU-OSHA | EU-OSHA platform for<br>sharing internal documents.

## API reference
