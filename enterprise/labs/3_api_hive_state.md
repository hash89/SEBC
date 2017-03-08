# API commands for Hive

## Starting Hive

`curl -u hadrien:cloudera -X POST http://84.39.48.222:7180/api/v13/clusters/hadrien/services/hive/commands/start`

## Stopping Hive

`curl -u hadrien:cloudera -X POST http://84.39.48.222:7180/api/v13/clusters/hadrien/services/hive/commands/stop`

## Hive Status

`curl -u hadrien:cloudera -X POST http://84.39.48.222:7180/api/v13/clusters/hadrien/services/hive/`
