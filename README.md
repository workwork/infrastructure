# Work-Work infrastructure

#### Because we can


## Initialize

### 1: Create docker-server

One, easy, way to do this is to set up `docker-machine` and use the command: `docker-machine create --driver DRIVERNAME --driver-specific-options driver-specific-value NAME`. 

We use digital ocean so the command looks like this: `docker-machine create --driver digitalocean --digitalocean-region ams2 --digitalocean-size 1g --digitalocean-access-token KLpLpQgsmFElYIjlPTVP3GXZj3Sx6v7CaOT1uLSN4sWvNtsAZFPELk9G3Fq9Gw3O --digitalocean-image ubuntu-14-04-x64 servername`
<sub><sup><sub><sup><sub><sup><sub><sup><sub><sup><sub><sup><sub><sup><sub><sup>Of course we didn't give you our real key, silly you.</sup></sub></sup></sub></sup></sub></sup></sub></sup></sub></sup></sub></sup></sub></sup></sub>


### 2: Create docker network bridge

We use a network bridge. This can be created with the following command:

`docker network create -d bridge nginx-proxy`

### 3: Boot the whole thing

Now we need to build and boot up everything. This can be done with the command

`docker-compose up -d`

### 4: Have fun

Yes.


