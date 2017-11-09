### Build docker image

```bash
docker build --name analytics/zeppelin:1.0 .
```

Run Container with docker compose:
```bash
docker-compose up
```

Notebooks are saved into `./notebooks`
Data can be loaded form `./data`

Open browser at:
```bash
localhost:8080
```

Login with usernames:
```bash
giorgio = distilled123!
martin = distilled123!
john = distilled123!
david = distilled123!
priyanka = distilled123!
rory = distilled123!
```

## Minishift

### load template
```bash
oc process -f ./templates/minishifrt.yml | oc create -f -
```

### build image
oc start-build bc/zeppelin --from-dir .

### Delete existing instances/services
oc delete scv --all
oc delete svc --all
oc delete dc --all
oc delete bc --all
oc delete routes --all
oc delete is --all


## Openshift
WIP
