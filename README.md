heroku-selectable-procfile
==========================

## Usage

For this buildpack to work, the env variable `TASKS` needs to be set. The buildpack picks all the Procfiles corresponding to the tasks specified by `$TASKS` and combine them in a single Procfile.

For example, if we want the app to run all the processes specified in `debug/Procfile.metrics` and `debug/Procfile.queries`, 
we add the variable to the environment,

```
$ heroku config:add TASKS=metrics,queries
```
and the buildpack will do the rest.
