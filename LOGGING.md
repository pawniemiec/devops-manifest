# Logging

Logging - as per [wiki](https://en.wikipedia.org/wiki/Tracing_(software)#Event_logging_versus_tracing)

In software engineering, tracing involves a specialized use of logging 
to record information about a program's execution. This information is 
typically used by programmers for debugging purposes, and additionally, 
depending on the type and detail of information contained in a trace log, 
by experienced system administrators or technical-support personnel and by 
software monitoring tools to diagnose common problems with software. 


## Format
Each application had global common logging function used across all modules.

Format of logging should be consistent across all environments and 

```
YYYY-MM-DD HH:MM:SS.ZZZ [<LOG_LEVEL>] <message>
```

## Levels and usage
The following LOG_LEVEL’s will be used:
- `DEBUG` - troubleshooting integration issues
   - DEV environment
   - SIT environment
   - Staging environment
- `INFO` - main functions of program
   - Staging environment
   - Production environment
- `WARN` - important  
   - Production environment
- `ERROR`
   - Production environment

Logging <LEVEL> is being read from Environment Variable LOG_LEVEL upon deployment.

## Location
All logging from docker images goes to `STDOUT` (both `STDERR` and `STDOUT`)

Kubernetes cluster grabs all logs sent to `STDOUT` and posts them 
to [ELK stack](https://<ELK_stack_URL>/app/kibana)
