heroku-selectable-procfile
==========================

## Usage

This buildpack picks the Procfile corresponding to the process specified by the 
environment variable `$PROC_NAME` and sets it as the main Procfile of the app.

For example, if we want the file `debug/Procfile.metrics` as the main Procfile 
of the app, we run
```
$ heroku config:add PROC_NAME=metrics
```
and the buildpack will take care of the rest.
