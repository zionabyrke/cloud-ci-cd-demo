# Cloud CI/CD Demo

![CI Status](https://github.com/zionabyrke/cloud-ci-cd-demo/actions/workflows/main.yml/badge.svg)

## Final Pipeline
On every push to `master` branch, GitHub Actions:
1. Installs dependencies
2. Runs the test suite
3. Only if tests pass, deploys `index.html` to GitHub Pages through the `gh-pages` branch

## Deployment Trigger
A push to `master`branch that passes the `build-and-test` job

## Security Setup
The `API_KEY` secret is stored in GitHub Secrets and never hardcoded or printed in logs.<br>
The Pages deploy uses the auto-provisioned `GITHUB_TOKEN` only for this repo.