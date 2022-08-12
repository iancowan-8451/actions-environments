# GitHub Environments Testing

### Demo Deploying Rules
* When pushing to `main`, deployment to `stag` environment is triggered automatically
* After deployment to `stag` environment, deployment to `prod` is triggered but requires user interaction before deploying
* Any branch can be triggered to be deployed to `qa-1` or `qa-2`
* Whenever a deployment to `qa-1` or `qa-2` is triggered, deployment to `stag` and `prod` is always ignored

### Process for Demo Deploying
* If you want to deploy to `stag` and `prod`, merge something into `main`
  * If you're trying to deploy into `prod`, after the deployment to `stag` is complete, approve the deployment to `prod` by "reviewing deployments"
* If you want to deploy to `qa-1` or `qa-2`,
  * Navigate to the actions page
  * Click on the action, "Build and Deploy"
  * Click on "Run workflow"
  * Select the QA environment to deploy to
  * Click "Run workflow"
