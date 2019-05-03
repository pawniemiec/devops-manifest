# CI/CD Pipeline


## High level overview
- Upon code Change Request new feature branch is created 
- Code is changed, signed with GPG key and pushed to VCS
- Artifact is built and unit tested automatically
- Upon successful tests outcome Developer creates Pull Request/Merge Request to `master` branch
- Code change is reviewed (built and tested locally according to PR/MR description)
- Code change is approved by at least 1 member of the team
- When this change is merged to `master` branch, automatic deployment to SIT Environment is performed
- Artifact built is pushed to Artifact repository with tag `<BUILD-NUMBER>`
- E2E tests are performed
- Staging Deployment is performed automatically given E2E tests success
- Load/Performance tests are performed
- User Acceptance Testing proceeds
- Upon successful UAT, changes are scheduled to be deployed in Production (details to be agreed)
- Production deployment is performed (automatically or 


## Local development
- Developer creates their environment initially from `local-dev-repo` which contains:

  - git client
  - local drone client
  - local repository (docker registry docker container at localhost:5000)
  - local kubernetes (virtualbox + minikube)
  - templates (repo, drone & kube)

- Developer creates initial E2E tests for all functions to be created
- Developer creates unit tests for 100% for their code (ideal world)
- Developer creates code and tests it manually
- Developer creates deployment files (if not present) and pushes the code to VCS which triggers automatic pipelne


## Environment variables
The following environment variables will be used across all applications with given values:

- `ENVIRONMENT`
  - `development`
  - `sit`
  - `staging`
  - `production`
- `LOG_LEVEL`
  - `DEBUG`
  - `INFO`
  - `WARN`
  - `ERROR`
