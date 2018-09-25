## Setting DNS in concourse 

If you get error failed to ping registry in docker then add DNS in docker-compose.yml of concourse

``` 
   environment:
      CONCOURSE_BASIC_AUTH_USERNAME: colthreepv
      CONCOURSE_BASIC_AUTH_PASSWORD: allthewin
      CONCOURSE_EXTERNAL_URL: http://dockerhost:8080
      CONCOURSE_POSTGRES_DATA_SOURCE: |-
        postgres://concourse:changeme@concourse-db:5432/concourse?sslmode=disable
    dns:
      - 8.8.8.8
      - 8.8.4.4
    restart: on-failure:10
```
