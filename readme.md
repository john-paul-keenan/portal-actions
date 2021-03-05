# Kong Developer Portal Templates


## Requirements

- [kong-portal-cli](https://github.com/kong/kong-portal-cli)
- [Kong Portal Templates](https://github.com/Kong/kong-portal-templates)
- [Kong Enterprise](https://konghq.com/)

## Steps to Demo:
1. Clone this repo and CD into it.
Take note of the files in the workspaces/default/ directory. Those are the same files as the default Kong portal. With Kong running, issue the following command to sync your portal with the files in this repo
`portal deploy default`

2. In this repo, take a look at the jpmcDemo/.github/workflows/ actions_push.yaml
That will be used to push the changes to the default portal to Kong. In this demo, we will be hosting the runner locally, but in a production enviroment, this would be run in a shared cloud enviroment.

3. Create and run a self hosted Github Action Runner inside your $PROJECT_ROOT.

4, Make a PR on one of the portal files and merge the PR.

5. Give your local runner a few moments to pickup the change, but that will do the rest.
