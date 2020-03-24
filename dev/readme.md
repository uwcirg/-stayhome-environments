# Development Environment

Sets up a clone of the production environment locally for development use.


## Setup

First, clone this repo:

```sh
$ git clone https://gitlab.cirg.washington.edu/psbrandt/stayhome-environments.git && cd ./stayhome-environments/dev
```

Then, start the containers:

```
$ docker-compose up
```

Finally, navigate to the client: https://client.local.stayhome.app:4400


## Credentials

| Account          | Username | Password |
| ---------------- | -------- | -------- |
| Database Admin   | postgres | postgres |
| Keycloak Admin   | admin    | admin    |
| Application User | test     | test     |

## Clean Up

To remove all StayHome Docker resources, run:

```sh
$ docker rm -f dev_stayhome-keycloak_1 dev_stayhome-db_1 dev_stayhome-ingress_1 dev_stayhome-client_1 dev_stayhome-fhir_1; docker volume rm dev_stayhome-data; docker network rm dev_stayhome-network
```