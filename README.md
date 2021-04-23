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
