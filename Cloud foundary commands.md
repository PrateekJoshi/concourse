# Cloud Foundry

### Login into your org and targerted space

```
cf lofin -a <api_endpoint> -u <user_name> -p <password> -o <target_org> -s <target_space>
``` 

### List deployed apps

```
cf apps
```

### Restart app

```
cf restage <app_name>
cf restage my-app-v1-1-0
```

### Bind a service (like mysql) to an app

```
cf cs <service_name> <plan_name> <your_binded_service_name>
cf cd p-mysql 100mb my-app-db
```

### View recent logs of an app

```
cf logs <app_name> --recent
cf logs my-app-v1-1-0 --recent
```