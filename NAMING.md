# Naming Convention

All names should be as descriptive as possible.

Only if there is valid reason (e.g. name length limit), the names will be abbreviated.

## Service name

```sh
<service>
```

_____________________________________________________

## Environments

### Name

```sh
  develpoment (abbrev=dev)
  sit         (abbrev=sit)
  staging     (abbrev=stg)
  production  (abbrev=prod)
```

### DNS

```sh
<ENV>:
<URLs>
```

### Kubernetes Cluster

#### Namespaces

```sh
<namespaces>
```
  
#### Each namespace will contain the following services:

```sh
  - Service
     <service_name>-svc
    - Pod
       <service_name>
      - Containers
```

#### AWS S3

```sh
<ENV>:
<S3 bucket name and structure>
```

#### AWS RDS

```sh
<ENV>:
<RDS info>
```

#### AWS SQS

```sh
<ENV>:
<Queue info>
```
