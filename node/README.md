# Boilerplate for Node in Docker Containers

This boilerplate applies best practices and opinions to streamline the
bootstrapping of Node applications in Docker Containers.

## What does it contain?

Docker image is built from official Node image. The `Dockerfile` applies some
best practies when working with Node/npm and Docker.

It uses `docker-compose` for handling any differences between environments,
especially for setting up what you need for local development.

`package.json` installs `nodemon` for reloading files on changes, and `tap` as
the test suite runner. Both are completely optional.

It also applies `npm-shinkwrap` which reduces build time for Docker.

## How do I use this image?

1. Clone/export it
2. Change package name in `package.json`
3. Replace with a new upstream
4. Start coding!

## How do I code with this image?

1. Run `docker-compose run --rm app nodemon` and edit files in your favorite
   editor.

## How do I debug with this image?

1. Run `docker-compose run --rm app /bin/bash` to get an interactive instance.

## How do I add new packages?

1. Run `docker-compose run --rm app npm install --save [new-package]` or use the
   interactive instance above.

## How do I connect to the service in the container?

1. Run docker-compose with the argument `--service-ports` and the configured
   ports in your docker-compose.yml will be exposed to the host machine.
