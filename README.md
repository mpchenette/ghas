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
### Code Scanning
1. Enable Code Scanning under Settings→Code Security
  - start with CodeQL default setup
1. Under Security→Code Scanning, we can add new 3rd party tools
  - Be sure that under Settings→Actions→General we have given the GITHUB_TOKEN read and write permissions
### Dependabot
1. Enable Dependabot under Settings→Code Security <!-- Only "Dependabot alerts" is needed to display the flask vulnerability -->
1. Under Security→Dependabot, view all Dependabot alerts
1. To remediate an alert, click on it and click the green "Create Dependabot security update" button
  - Enabling "Dependabot security updates" under Settings→Code Security will auto-create PRs with remediations
  - Enabling "Dependabot version updates" under Settings→Code Security is similar but more proactive: will auto-create PRs when new versions of your dependencies are available.
### Secret Scanning
#### Push Protection
1. View the `Enable/Disable` button for Push protection under repo Settings→Code Security
1. Add a new GitHub PAT to `main.py`. Attempt to push. View error message.
  - `git reset --soft HEAD^` to undo a commit
