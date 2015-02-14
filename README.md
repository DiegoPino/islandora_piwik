# Islandora Piwik Integration

## Overview

This utility module provides integration with the [Piwik Open Analytics Platform](http://piwik.org/).

This module tracks object usage and collection usage. Object usage is straight foward: each time a user views an object at /islandora/object/pid, the request for that URL is recorded by Piwik. Collection usage works differently. Each time an object is viewed, a "usage" of its collection is recorded. If an object is a member of more than one collection, each collection gets a usage.

Collection PIDs are recorded as custom Piwik variables are are available under the "Visitors" tab in the Piwiki Dashboard. Collections are also objects, so when the default collection object page is viewed, Piwik records that as well, but as an object. Keep in mind that object usage and collection usage as describe in the previous paragraph are not the same - the object usage (including collections as objects) records how many times the object (or collection) default display at /islandora/object/pid was viewed, whereas the collection usage records how many times objects in each collection were viewed.

## Dependencies

A Piwik server.

## Configuration

Visit admin/islandora/tools/piwik to configure this module. There is no set up on the Piwik side other than creating a site corresponding to your Islandora instance.

## Maintainer

* [Mark Jordan](https://github.com/mjordan)

## Feature requests

This module was written as part of a large migration to Islandora from another repository platform. It wasn't intended to be extensible or terribly flexible. So feel free to fork the Github repo and modify it to suit your needs. That said, if enough people +1 a featue identified in the issue queue or on the Islandora email lists, we can look at how we can develop the module further.

* Ability to use one Piwik site for multiple Islandora front ends, so that objects accessible in multiple front ends would have their usage aggregated in one place.



