# gz-docker
Docker configs for developing gazebo simulator

`./work` is the working volume mounted to your local machine.\
You should use vcs to import repos for building gazebo in `./work/gazebo/src/GZ_REPOS`\
see [gazbo source install](https://gazebosim.org/docs/garden/install_ubuntu_src) for how to build using `colcon`

### Building Image and running container
`docker compose build` in the repo's source directory\

****It is assumed you have and nvidia gpu and have setup the container-toolkit for gpu passthrough. If you don't have an nvidia gpu just delete `docker-compose.override.yml` before starting a container****\


`./run_dev.sh` to start a container.
If a container is already running, you can use\
`docker attach CONTAINER_NAME` to connect to it.