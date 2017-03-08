# Upgrade Cloudera Manager

## API calls

### Api version

`curl -u hadrien:cloudera http://84.39.48.222:7180/api/version`

result : `v14`


### CM Version

`curl -u hadrien:cloudera http://84.39.48.222:7180/api/v14/cm/version`

result :

```json
{
  version: "5.9.1",
  buildUser: "jenkins",
  buildTimestamp: "20170112-1158",
  gitHash: "a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1",
  snapshot: false
}
```

### CM Users

`curl -u hadrien:cloudera http://84.39.48.222:7180/api/v14/users`

result :

```json
{
  items: [
    {
      name: "admin",
      roles: ["ROLE_ADMIN"]
    },
    {
      name: "hadrien",
      roles: ["ROLE_ADMIN"]
    },
    {
      name: "minotaur ",
      roles: ["ROLE_OPERATOR"]
    },
    {
      name: "minotaur2",
      roles: ["ROLE_CONFIGURATOR"]
    }
  ]
}
```

### Scm Database

`curl -u hadrien:cloudera http://84.39.48.222:7180/api/v14/cm/scmDbInfo`

result :
```json
{
  scmDbType: "MYSQL",
  embeddedDbUsed: false
}
```
