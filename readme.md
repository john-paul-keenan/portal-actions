# Kong Developer Portal Templates


## Requirements

- [kong-portal-cli](https://github.com/kong/kong-portal-cli)
- [Kong Portal Templates](https://github.com/Kong/kong-portal-templates)
- [Kong Enterprise](https://konghq.com/)

## Steps to Demo:
1. Clone this repo and CD into it.
Take note of the files in the workspaces/default/ directory. Those are the same files as the default Kong portal. With Kong running, issue the following command to sync your Kong Dev Portal  default workspace with the files in this repo
`portal deploy default`

2. In this repo, take a look at the jpmcDemo/.github/workflows/ actions_push.yaml
That will be used to push the changes to the default portal to Kong. In this demo, we will be hosting the runner locally, but in a production enviroment, this would be run in a shared cloud enviroment.

3. Create and run a self hosted Github Action Runner inside your `$PROJECT_ROOt`.
On a Mac
```
# Create a folder
mkdir actions-runner && cd actions-runner
# Download the latest runner package
curl -O -L https://github.com/actions/runner/releases/download/v2.277.1/actions-runner-osx-x64-2.277.1.tar.gz
# Extract the installer
tar xzf ./actions-runner-osx-x64-2.277.1.tar.gz
```
Configure the runner
```
# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/john-paul-keenan/jpmcDemo --token ABJG54XJWJNWNUMYY5P37LDAILKCS# Last step, run it!
$ ./run.sh
```

4. Edit one or more of the portal files and save the changes directly in that branch or in a new branch and merge. 

5. Keep an eye on yoyur local runner. It will notice the update and push the changes to the portal.

