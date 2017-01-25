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
