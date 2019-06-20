# Testing

We are aiming for all tests to be automated and build-in to build/deployment pipeline.

## Functional testing

### Unit testing

Each function should have unit tests written covering as many edge cases as possible.
100% code test coverage is not possible in real world, but we are aiming for it.

### Sanity testing

Sanity testing is the surface level testing where QA engineer verifies that all functions
and commands available in the product and project are working fine.

### Smoke testing

Also known as `Build Verification Testing`, is a type of system testing that comprises
of a non-exhaustive set of tests that aim at ensuring that the most important functions work.

### Interface testing

A testing technique used to identify the presence of defects is a product/system under test
by using Graphical User Interface [GUI].

### Integration testing

A level of system testing where individual units are combined and tested as a group.
The purpose of this level of testing is to expose faults in the interaction between integrated
units. These tests also includes verification of interaction with any external and/or 3rd party
systems, by either creating a mock version of them or directly interating with tests versions
of these systems.

### Non-functional testing

#### Performance Testing

Performance testing is the process of determining the speed, responsiveness and stability of
a system under a normal workload.

#### Load testing

Load testing is the process of determining the speed, responsiveness and stability of a system
under a workload expected at the peak time.

#### Stress testing

This test mainly determines the system on its robustness and error handling under extremely
heavy, increasing load conditions. It allows to set the boundaries for the system ingestion
limiting mechanizm.

#### Volume testing

Volume testing is done to analyze the system performance by increasing the volume of data
in the data store.

#### Compatibility testing

Compatibility Testing is a type of Software testing to check whether your system is capable
of running on different hardware, operating systems, applications, network environments
or Mobile devices.

#### Install testing

Most software systems have installation procedures that are needed before they can be used for
their main purpose. Testing these procedures to achieve an installed system that may be used
is known as installation testing. These procedure may involve full or partial upgrades, and
install/uninstall processes.

#### Recovery testing

Recovery testing is the activity of testing how well an application is able to recover from
crashes, hardware failures and other similar problems. Recovery testing is the forced failure
of the system in a variety of ways to verify that recovery is properly performed.

#### Reliability testing

Reliability testing is defined as a software testing type, that checks whether the system can
perform a failure-free operation for a specified period of time in a specified environment.

#### Accessibility testing

Accessibility Testing is defined as a type of Software Testing performed to ensure that the
application being tested is usable by people with disabilities like hearing, color blindness,
old age and other disadvantaged groups.

### Security testing

Security testing is a type of software testing that intends to uncover vulnerabilities of
the system and determine that its data and resources are protected from possible intruders.

### Regression testing

Known also as End-to-End (E2E) tests:

- When some sort of unit testing is not possible, end-to-end tests should cover the gap
- They also make sure that any code change introduced does not break well defined current
functionality
- Should be automated
- Should include automated sanity tests
- Should include automated smoke tests
- If in scope should include automated interface tests
- Should include integration tests
- Should include non-fnctional tests

### User Acceptance Testing

Performed by subset of Clients or End Users (Early Adopters) who are not employees of the
organization. Puprose of these testing is to obtain feedback from real Users and prioritize
the product improvements in the most effective way.

### Production Testing

Full set or most commonly, subset of Regression Testing run over Production systems periodically
as a means of live system monitoring.
