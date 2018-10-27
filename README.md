# concourse

### Running Conspurse

Go to the location where docker-compose.yml if located for Concourse, and run the command 

```
docker-compose up -d
```

### Login in to consourse

```
fly --target <target_space> login --concourse-url <concourse_deployed_url>
fly --target tutorial login --concourse-url http://127.0.0.1:8080 
```

### Setting a pipeline 

```
fly -t <target_space> set-pipeline -p <pipeline_name> -c <location_of_your_pipeline_config_file>
fly -t tutorial set-pipeline -p joshi -c ./pipeline/pipeline.yml
```

* In case of any change in pipeline.yml , re-run the above command to set the pipeline.

