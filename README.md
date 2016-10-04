# Docker Builders

A collection of Docker deployments for various purposes.

## Gitlab

The [Gitlab CE][gitlab_ce] Docker image. Uses [Postgres][]
and [Redis][] images for database persistence. Uses external volumes
to persist data; for initial set up, run:

    docker volume create --name vdb
    docker volume create --name gitlab_config
    docker volume create --name gitlab_data
    docker volume create --name gitlab_logs

Then just

    cd gitlab-ce
    docker-compose up -d

Gitlab takes a few minutes to start and configure
itself. Incidentally, this means Redis and Postgres are ready by the
time it runs.

## Load Balancers

We can use either Nginx or HA Proxy as a load balancer, and put two
instances of Gitlab behind either as a minimal "balanced" web
layer. Use git tags to switch to either:

    git checkout haproxy
    git checkout nginx

[gitlab_ce]: https://hub.docker.com/r/gitlab/gitlab-ce/
[Postgres]: https://hub.docker.com/_/postgres/
[Redis]: https://hub.docker.com/_/redis/
