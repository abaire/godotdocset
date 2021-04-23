# godotdocset
Dash docset generator for Godot engine xml docs

```
usage: godotdocset.py [-h] -f FROM

optional arguments:
  -h, --help            show this help message and exit
  -f FROM, --from FROM  path to the godot-engine repository to be parsed.
```

Generating docset:

1. Clone the appropriate branch from https://github.com/godotengine/godot
1. `pipenv install`
1. `pipenv run ./godotdocset.py -f <path_to_cloned_repo> --install`
1. Restart Dash/Zeal if it was already running.

# Nightly autocreates

Docsets for Godot branches:

* [master](https://nightly.link/abaire/godotdocset/workflows/build_docset-master/master/godot-docset-master.zip)
* [3.x](https://nightly.link/abaire/godotdocset/workflows/build_docset-3.x/master/godot-docset-3.x.zip)


*Note*: Github scheduled actions are not guaranteed to run so it is possible that the docsets will fail to be generated nightly.
See https://github.community/t/no-assurance-on-scheduled-jobs/133753.

## Adding a new nightly:

Duplicate one of the yml files under `.github/workflows` and:

1. Modify the cron entry.
1. Update the `refs` under `Checkout Godot`
1. Update the `name` under the `upload-artifact` action.
