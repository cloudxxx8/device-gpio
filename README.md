# GPIO Device Service
[![Build Status](https://jenkins.edgexfoundry.org/view/EdgeX%20Foundry%20Project/job/edgexfoundry/job/device-gpio/job/main/badge/icon)](https://jenkins.edgexfoundry.org/view/EdgeX%20Foundry%20Project/job/edgexfoundry/job/device-gpio/job/main/) [![Go Report Card](https://goreportcard.com/badge/github.com/edgexfoundry/device-gpio)](https://goreportcard.com/report/github.com/edgexfoundry/device-gpio) [![GitHub Latest Dev Tag)](https://img.shields.io/github/v/tag/edgexfoundry/device-gpio?include_prereleases&sort=semver&label=latest-dev)](https://github.com/edgexfoundry/device-gpio/tags) ![GitHub Latest Stable Tag)](https://img.shields.io/github/v/tag/edgexfoundry/device-gpio?sort=semver&label=latest-stable) [![GitHub License](https://img.shields.io/github/license/edgexfoundry/device-gpio)](https://choosealicense.com/licenses/apache-2.0/) ![GitHub go.mod Go version](https://img.shields.io/github/go-mod/go-version/edgexfoundry/device-gpio) [![GitHub Pull Requests](https://img.shields.io/github/issues-pr-raw/edgexfoundry/device-gpio)](https://github.com/edgexfoundry/device-gpio/pulls) [![GitHub Contributors](https://img.shields.io/github/contributors/edgexfoundry/device-gpio)](https://github.com/edgexfoundry/device-gpio/contributors) [![GitHub Committers](https://img.shields.io/badge/team-committers-green)](https://github.com/orgs/edgexfoundry/teams/device-gpio-committers/members) [![GitHub Commit Activity](https://img.shields.io/github/commit-activity/m/edgexfoundry/device-gpio)](https://github.com/edgexfoundry/device-gpio/commits)

> **Warning**  
> The **main** branch of this repository contains work-in-progress development code for the upcoming release, and is **not guaranteed to be stable or working**.
> It is only compatible with the [main branch of edgex-compose](https://github.com/edgexfoundry/edgex-compose) which uses the Docker images built from the **main** branch of this repo and other repos.
>
> **The source for the latest release can be found at [Releases](https://github.com/edgexfoundry/device-gpio/releases).**

## Documentation

This device service is contributed by [Jiangxing Intelligence](https://www.jiangxingai.com)

For latest documentation please visit https://docs.edgexfoundry.org/latest/microservices/device/services/device-gpio/Purpose

## Build Instructions

1. Clone the device-gpio repo with the following command:

        git clone https://github.com/edgexfoundry/device-gpio.git

2. Build a docker image by using the following command:

        make docker

3. Alternatively the device service can be built natively:

        make build

## Build with NATS Messaging
Currently, the NATS Messaging capability (NATS MessageBus) is opt-in at build time.
This means that the published Docker images do not include the NATS messaging capability.

The following make commands will build the local binary or local Docker image with NATS messaging
capability included.
```makefile
make build-nats
make docker-nats
```

The locally built Docker image can then be used in place of the published Docker image in your compose file.
See [Compose Builder](https://github.com/edgexfoundry/edgex-compose/tree/main/compose-builder#gen) `nat-bus` option to generate compose file for NATS and local dev images.

## Packaging

This component is packaged as docker image.

For docker, please refer to the [Dockerfile] and [Docker Compose Builder] scripts.

[Dockerfile]: Dockerfile
[Docker Compose Builder]: https://github.com/edgexfoundry/edgex-compose/tree/main/compose-builder

## License
[Apache-2.0](LICENSE)

