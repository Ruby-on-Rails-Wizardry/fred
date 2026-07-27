# fred

Demo Rails 8 + Hotwire app for **[docker-mise-cluster](https://github.com/Ruby-on-Rails-Wizardry/docker-mise-cluster)**.

## Cluster usage

This repo is a **git submodule** of `docker-mise-cluster` at path `fred/`.

```bash
# from cluster root
git submodule update --init --recursive
bin/setup
bin/compose up fred
# via nginx: http://localhost:8080/fred/
```

Development expects the cluster Postgres/Redis services (`DATABASE_URL`, `REDIS_URL`) when run under compose.

## Standalone

```bash
bundle install
bin/rails db:prepare
bin/rails server
```

Requires Ruby from the Gemfile (`ruby "…"`) and Node/Yarn if you run JS tests.
