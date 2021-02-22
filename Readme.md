| [![5G-VICTORI logo](doc/images/5g-victori-logo.png)](https://www.5g-victori-project.eu/) | This project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 857201. The European Commission assumes no responsibility for any content of this repository. | [![Acknowledgement: This project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 857201.](doc/images/eu-flag.jpg)](https://ec.europa.eu/programmes/horizon2020/en) |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |


# Message Broker

Messaging service for communication between microservices.

## What is this?

Messaging service as part of the of the [platform](https://gitlab.irt.de/5g-victori/platform) for media caching on trains. Allows communication between microservices. A service can send messages on specific topics, which other services can register to receive updates on (publish/subscribe). The message broker supports message replay, which means that a client which registers for a specific topic will instantly receive the last message sent on this topic. Service of the caching platform benefit from this feature when recovering from an error state. They do not miss messages which may be crucial for resuming operation.

## How does it work?

Message broker is an instance of [NATS streaming service](https://docs.nats.io/developing-with-nats-streaming/streaming).

## Install, build, run

**Note:** _Typically you would use the `up.sh` script from the [Platform](https://gitlab.irt.de/5g-victori/platform) project to install, build and run this service as part of a composite of docker services. Read on if you intend to run the service directly on your host system._

**Prerequesits**:

```bash
$ docker-compose up -d
```
