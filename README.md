# Cypress GH Actions Dispatch Workflow

This is a demo on how to use the [repository dispatch event](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#repository_dispatch) to listen to dispatch events and trigger specific [Cypress](https://www.cypress.io/) e2e tests from another repository. 
This repo contains the tests that should run when a workflow is triggered from the [dispatcher](https://github.com/tiotto/cypress-gh-actions-dispatcher) repo.

### Usage

- Fork both [cypress-gh-actions-dispatcher](https://github.com/tiotto/cypress-gh-actions-dispatcher) and [cypress-gh-actions-dispatch-workflow](https://github.com/tiotto/cypress-gh-actions-dispatch-workflow);
- This repo uses the [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch) action to dispatch events easily. Make sure to generate a ([Personal Access Token (PAT)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) and add it as a Github Actions secret for the dispatch to work;
- Lastly, run the ["trigger end-to-end"](https://github.com/tiotto/cypress-gh-actions-dispatcher/actions/workflows/trigger.yml) workflow on the [dispatcher](https://github.com/tiotto/cypress-gh-actions-dispatcher) repo by picking which test suite you would like to dispatch an event for.
