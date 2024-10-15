# ghas
GitHub Advanced Security

## To Run
1. `brew upgrade`
1. `python3 -m venv .venv`
1. `source .venv/bin/activate`
1. `pip install flask`
1. `pip install Flask flask_httpauth`
1. `python3 main.py`

## Demo Steps
### Secret Scanning
#### Push Protection
1. View the `Enable/Disable` button for Push protection under repo Settings→Code Security
1. Add a new GitHub PAT to `main.py`. Attempt to push. View error message.
  - `git reset --soft HEAD^` to undo a commit
