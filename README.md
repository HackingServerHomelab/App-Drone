# App-Drone

## First Time Prerequisites

1. Run [Traefik](https://github.com/HackingServerHomelab/App-Traefik)

## Running the Containers

1. Update the following volume in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/drone:/data`
2. Update the following environment variable in [docker-compose.yml](./Docker/docker-compose.yml)
    * `DRONE_SERVER_HOST: "localhost" # changeme`
    * `DRONE_RPC_SECRET: "bea26a2221fd8090ea38720fc445eca6" # Changeme`
    * `DRONE_GITHUB_CLIENT_ID: "changeme" # changeme`
    * `DRONE_GITHUB_CLIENT_SECRET: "changeme" # changeme`
    * `DRONE_GITEA_CLIENT_ID: "changeme"`
    * `DRONE_GITEA_CLIENT_SECRET: "changeme"`
    * `DRONE_GITEA_SERVER: "changeme"`
3. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.drone-server.rule=Host(`localhost`)"``
4. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
