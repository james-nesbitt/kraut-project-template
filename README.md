# radi-project-template

A template for the definition of a project

This source code is a demo project, which can be used as a project template
when starting new projects.  It is a model used to strategize the configuration
and definition of projects, regardless of what backend tool and hosting 
implementation is used to deliver and develop the project.

The role that Radi plays is to provide a first implementation that uses the
configuration to produce development and production environments.

# How to use this template

Use this template as the starting point for your project by either:

1. use git to clone this repository
2. use `radi local.project.create --project.create.source <github raw link for the .radi/init.yml>`

> #2 is currently broken, and needs to be fixed.

Then make changes, primarily in the following files:

- .radi/settings.yml : change the name of the project
- .radi/user.yml : this should have updated data and be moved to ~/.config/radi/user.yml
- docker-compose.yml : make any changes that you need for your project architecture
- commands.yml : make any changes to existing commands based on your project arch, and add any additional commands

# The future of this template

1. This template will get further refinements related to configuration of projects
2. this template will get a tool for automatic use, with questions and answers used to configure it automatically

# Components of the template:

## .radi

Configuration for the tools that consume the template.  This has it's own README

## source

Conceptually where project specific source would go.  This allows true project 
source to be kept separately from project configuration and local configuration

The point with this path is that it contains only files that make sense to the 
project, that are not a part of this tool.  In the template case, you can see
that the current source code folder contains the result of running:

```
$/> composer create-project drupal-composer/drupal-project:8.x-dev
```

## settings

A convention used to keep settings used by the project separate from source
code, for environment based use.

Examples are to put drush and drupal console settinge here for local use.

This concept came mainly from having to interpret existing project source that
had already integrated source code configuration files that made no sense for 
the tools that consume this template.
If settings for projects are better maintained, then this path will not be 
necessary.

## assets

A temporary path that can be used for local effort to keep assets used in the 
project locally.
This is an early idea, that is not really necesary, so it will probably be 
dropped in the future, and docker volumes will be used to implement it.

