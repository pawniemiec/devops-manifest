# Naming Convention
All names should be as descriptive as possible.

Only if there is valid reason (e.g. name length limit), the names will be abbreviated.

## Service name
```
<service>
```
_____________________________________________________
## Environments

#### Name
    sit        (abbrev=sit)
    staging    (abbrev=stg)
    production (abbrev=prod)
      
#### DNS
```
SIT:
<URLs>
```

```
Staging:
<URLs>
```

```
Production:
<URLs>
```


#### Kubernetes Cluster
##### Namespaces
```
<namespaces>
```
  
###### Each namespace will contain the following services:
```
  - Service
     <service_name>-svc
    - Pod
       <service_name>
      - Containers
```

#### AWS S3
```
<ENV>:
<S3 bucket name and structure>
```

#### AWS RDS
```
<ENV>:
<RDS info>
```

#### AWS SQS
```
<ENV>:
<Queue info>
```

