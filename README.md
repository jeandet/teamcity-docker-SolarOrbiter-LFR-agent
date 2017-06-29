# LPP Solar Orbiter LFR Flight Software teamcity image

This image is derived from our [base image](https://hub.docker.com/r/jeandet/teamcity-docker-minimal-agent/). It is based on Fedora and OpenJDK.
It has been designed to work either as standalone docker agent or with [TeamcityDockerCloudPlugin](https://github.com/JeanRev/TeamcityDockerCloudPlugin).
This image is used to build and test LFR Flight Software in a clean and reproductible environment.

You can pull the ready-to-use image from the Docker Hub repository

`docker pull jeandet/teamcity-docker-SolarOrbiter-LFR-agent`


To start the container manually just remember to set TC server URL var:

```
docker run -it -e SERVER_URL="<url to TeamCity server>"  \
    -v <path to agent config folder>:/data/teamcity_agent/conf  \
    jeandet/teamcity-docker-SolarOrbiter-LFR-agent
```
