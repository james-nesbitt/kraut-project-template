# SETTINGS

A folder that holds settings used to build and configure the
project.

This folder can hold runtime configuration for Drupal
(the site folder) and can also hold operation settings for
Drupal-Console and Drush, and other such tools.

## Usage

Put any project configuration folders into this folder
as a subfolder.  When building source images, include each
settings folder as needed.  In local run-time, bind/map
each folder into place, as needed.

@NOTE some of these binds/maps may be nested.  Take care
to have them bound/mapped in an appropriate order during
building and orchestration.
