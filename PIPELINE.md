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


## Technology stack
- VCS: Github/GitLab/Other
- Build tool: [Jenkins/Drone/Other](https://Build_tool_URL/)
- Artifact repository: [ECR/Dockerhub/Artifactory](https://artifact_repository_URL/)
- Deployment provider: [iJenkins/Drone/other](https://CI_tool_URL/)
- Deployment cluster: DCOS/Kubernetes/EKS/Other

Application:
- NodeJS v8.11 (Frontend)
- Python v3.7 (Backend)
- Python Framework - Flask (REST API)
- etc

Data storage:
- PostgerSQL v10.4 (Main data storage)
- AWS SQS (as main message queue system)
- S3 (main storage)
- S3 (backup storage)
- Glacier (historical backup storage)
- etc

Testing:
- Cucumber/Robotframework (Unit testing)
- SonarQube Scanner (Security Unit testing)
- Locust.io (Performance/Load testing)
- SSL Labs (Encryption testing)
- ClamAV (Antivirus scanning)
- OWASP ZAP proxy (Security pipeline tool)
- etc

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
