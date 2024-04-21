# Overview
This repo contains my configs to python linters. Specifically python linters used in the [python-lint-annotate](https://github.com/juissi-t/python-lint-annotate/tree/ff09bc6bdd47de544b00cf57a9921c636a829909/) github action.

Additionally it contains the github action to run [python-lint-annotate](https://github.com/juissi-t/python-lint-annotate/tree/ff09bc6bdd47de544b00cf57a9921c636a829909/) on pull request actions.


# To copy github action and configs to another repo
- Create a copy of `.github/workflows/workflow-templates/copy-to-repo-TEMPLATE.yml` and rename the "TEMPLATE" portion to the destination repo
- In the copied file edit the 'CHANGEME's in the env section at the top.
- Commit and push changes.

> Don't modify the github action for the python linters directly. It'll be annoying when there's
> changes from this repo.