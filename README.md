# Eduwallet integration

The configuration and tools to bind several services together in one running system.

So that we can:
- refer to one commit/tag for a specific deployment or build
- have overrides for config as they are used on the servers
- have overrides for config as they differ between stages (demo, test, prod etc)
- have scripts (ansible?) to automate the building of the servers on which this runs
- have one place to host all the CI config and setup

## docker-compose

Demo is ran through docker-compose. A docker-compose file binds the services together.
There may be multiple docker-compose files if we have multiple logical
clusters, but for now one is enough.

In future we may use it to power test and dev servers too.

So that we can:
- build any service in docker containers and publish them on a container registry. unified.
- use simple yaml to describe the networking, environment vars, and other dependencies
- have simple tooling to deploy new versions of, or new dependencies for, -services

## caddy

All services are hosted through a reverse proxy on the host machine. 

So that we can:
- proxy to multiple docker-compose clusters
- have easy, zero-config ssl
- have a really simple config

## Quickstart

TODO: describe how to boot a server, provision it, and then deploy the integration infra on it,
and then deploy the services on it.

### Install

TODO: describe what's needed to get going. Docker, compose, ?.

### Run

TODO: describe how to run a:
- new provisioning
- update
- deploy

### Test

TODO: how can we test this, if at all?
