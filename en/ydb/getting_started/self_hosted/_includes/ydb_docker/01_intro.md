---
sourcePath: en/ydb/ydb-docs-core/en/core/getting_started/self_hosted/_includes/ydb_docker/01_intro.md
---
# Running {{ ydb-short-name }} in Docker

For debugging or testing, you can run the YDB [Docker](https://docs.docker.com/get-docker/) container.

## Connection parameters {#conn}

As a result of completing the instructions below, you'll get a local YDB database that can be accessed using the following:

{% list tabs %}

- gRPC
  - [Endpoint](../../../../concepts/connect.md#endpoint): `grpc://localhost:2136`
  - [Database location](../../../../concepts/connect.md#database): `/local`
  - [Authentication ](../../../../concepts/connect.md#auth-modes): Anonymous (without authentication)

- gRPCs/TLS
  - [Endpoint](../../../../concepts/connect.md#endpoint): `grpcs://localhost:2135`
  - [Database location](../../../../concepts/connect.md#database): `/local`
  - [Authentication ](../../../../concepts/connect.md#auth-modes): Anonymous (without authentication)

{% endlist %}

