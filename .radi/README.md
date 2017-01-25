# .radi folder

The central location for all radi oriented configuration.  While the path name
is clearly tied to the radi tool, beyond that convention there is not strict 
requirement that the template matches the tool.  The tools used are meant to 
adapt to the configurations in this path.

# YML Files

The first thing to note is that configuration is separated into various yml
files which are used to provided configuration to the tool.  Each tool
encapsulates a configuration concept, with some common sense, and others 
platform dependent (such as upcloud.yml)

# Environments

Configurations are inherently overrideable, either in part or as a whole,
depending on the particular configuration.  This means that configurations 
are loaded in a scope, and collected across scopes.

The typical scope order (from lower priority to higher priority):

- default
- user
- project
- environment

In the case of some configuration such as settings, individual values from
a higher scope override values in a lower scope.
In other configurations, values from a single scope are used, in the highest
priority scope where settings are found.

# Secrets

Secret management, and centralization is a key consideration in the settings.

The intitial implementation will likely be key value yml file in the secrets
folder, which will be used as string replacement keys for all other yml read.

# Local versus remote platforms

It is likely that remote platforms which provide environments for staging, 
production and feature branching will not use the configuration directly, but
will provide different internal services to provide the settings.  In such
cases, the project yml may be used to populate those services.
