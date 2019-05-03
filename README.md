# Devops Manifest
The central DevOps repo for <project> development

# Dev Manifesto

### Agile software development
PLease familiarize yourself with [Agile Manifesto](./AGILE_MANIFESTO.md)

-------------------------------------------------------------------------------
# 12 Factor App
Please see [here](https://12factor.net/)

-------------------------------------------------------------------------------
# Decision making process
All Engineers are involved in decision making process

Every thought and proposition is highly valued

Even if you think your idea might not be the best, it actually can be very valuable

Here is [a list](./DECISIONS.md) of decisions to be made and decisions made (and documented in appropriate place)

Feel free to add whatever technical/design and procedural to WE_NEED_TO_DECIDE section


-------------------------------------------------------------------------------
# Naming convention

Naming convention and names decided can be found [here](./NAMING.md)

-------------------------------------------------------------------------------
# CI/CD

### Continuous integration
All developers will have the same environment to work on, to minimise integration issues

All developers are responsible for updating their development environment as often as possible/needed

All code is maintained in Version Control System (VCS)

Each task developers are working on should be achievable within 1 day

If certain task takes longer, it should be split into smaller subtasks

Each code merge will contain the following components:

- Code

- Unit tests

- Integration definition(s)

- Documentation

  - Installing / Getting started
  - How to start developing
  - How to build
  - How to publish
  - Configuration 
  - Relevant links

- Pull/Merge request information

  - Description of changes
  - Relevant tickets
  - Tests description
  - Types of review required


-------------------------------------------------------------------------------
## Continuous delivery
We will aim to have the code merged several time a day to catch merge conflict as early as possible.

Smaller the change, faster delivery and faster overall product progress.

Every commit produces artifact via automated build triggered from VCS.

All artifacts are stateless

All artifacts are run as non-elevated user (root is forbidden)


-------------------------------------------------------------------------------
## Continuous deployment

### Environments
There are 4 environments with different use cases

##### Production
Live Environment

- Receives changes upon User Researcher request/approval
- Code changes are applied upon all E2E, Load, Performance, Security tests are passed

##### Staging
User Acceptance Testing

- Stable environment
- Code changes are applied automatically upon all E2E and security tests passes

##### SIT
System Integration Testing

- developers merge and test code here
- if code change breaks environment developer reverts changes and works on fix locally
    - in rare case local fix is not possible coordination with other SIT users is required to avoid unnecessary disruption

##### DEV
Development environment

- crack on here :)


-------------------------------------------------------------------------------
## CI/CD Pipeline
Detailed description are available here: [PIPELINE](./PIPELINE.md)


-------------------------------------------------------------------------------
## Development process

#### Foundations
Each developer works locally. Ideally whole stack is brought up on the local development machine

If not possible, any non offensive/non destructive integrations will reach relevant parts of SIT environment


#### Branching out
Branch creation process include the following steps:

- Branch names should have format of <STORY-NUMBER>_<short_description>
- Developer starts working on code which is branched out from `master` branch

#### Versioning
Each artifact will be tagged with unique ID

Microservices architecture allows to use various combinations of different versions of artifact to build the final system

Therefore there will be only the Current Version of the System, with pre-defined microservices' tags

All previous Version configurations will be stored in Version control for history and legal purposes

#### Code
The following needs to be defined for code:

- formatting
- linting

#### Merging
- All commits should be squashed to reasonable number of them
- Meaningful commit messages is a must
- Agreed pre-commit hooks should be enforced, e.g.

  - Checking for existence of secrets
  - Formatting/linting verification/automatic updates

- Merge/Pull Requests should use one of the templates provided

#### Continous Documentation
- All functions have simple explanation:

  - Self-explanatory function names should be used
  - Short arguments and outcome descripion

- All files have information required to pick up code easily (quite fuzzy - define more)
- All parts of the system are documented and documentation is tested (e.g. by non-technical person)


-------------------------------------------------------------------------------
## Infractructure
All applications will run inside containers on <cluster>.
Data storage solutions will be provisioned on <storage> 

-------------------------------------------------------------------------------
## Technology stack
Please see [Pipeline](./PIPELINE.md)


-------------------------------------------------------------------------------
## Data

### Storage 

### Backup & Recovery



-------------------------------------------------------------------------------
## Security
Security information can be found [here](./SECURITY.md)


-------------------------------------------------------------------------------

## Testing
Testing strategy can be found [here](./TESTING.md)


-------------------------------------------------------------------------------
## Operations

### Glossary
Please see [GLOSSARY.md](./GLOSSARY.md)


### Procedures
List of procedures can be found [here](./PROCEDURES.md)

### Monitoring
Please see [MONITORING.md](./MONITORING_AND_ALERTING.md)

### Logging
Please see [LOGGING.md](./LOGGING.md)

