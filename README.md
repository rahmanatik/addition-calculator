# Basic Commands
### Start your registry
`docker run -d -p 5000:5000 --name registry registry:2`

### Pull (or build) some image from the hub
`docker pull matikbd/addition-calculator`

### Tag the image so that it points to your registry
`docker image tag matikbd/addition-calculator localhost:5000/myfirstimage`

### Push it
`docker push localhost:5000/myfirstimage`

### Now stop your registry and remove all data
`docker container stop registry && docker container rm -v registry`