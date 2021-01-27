# ROS ydlidar x4 node in Docker [![](https://img.shields.io/docker/pulls/frankjoshua/ros-ydlidar-x4)](https://hub.docker.com/r/frankjoshua/ros-ydlidar-x4) [![CI](https://github.com/frankjoshua/docker-ros-ydlidar-x4/workflows/CI/badge.svg)](https://github.com/frankjoshua/docker-ros-ydlidar-x4/actions)

## Description

Runs a ros ydlidar x4 in a Docker container. Probably need --network="host" because ROS uses ephemeral ports.

## Example

```
docker run -it \
    --network="host" \
    --env="ROS_IP=$ROS_IP" \
    --env="ROS_MASTER_URI=$ROS_MASTER_URI" \
    --device="/dev/ttyUSB0:/dev/ydlidar" \
    frankjoshua/ros-ydlidar-x4
```

## Building

Use [build.sh](build.sh) to build the docker containers.

<br>Local builds are as follows:

```
./build.sh -t frankjoshua/ros-ydlidar-x4 -l
```

## Testing

Github Actions expects the DOCKERHUB_USERNAME and DOCKERHUB_TOKEN variables to be set in your environment.

## License

Apache 2.0

## Author Information

Joshua Frank [@frankjoshua77](https://www.twitter.com/@frankjoshua77)
<br>
[http://roboticsascode.com](http://roboticsascode.com)
