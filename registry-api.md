# Devfile Registry API

The following document outlines the Devfile Registry REST API, and expected responses from each endpoint.

## Get Devfile Registry Stack Index

Gets the index.json containing metadata about the Devfile stacks in the devfile registry

**URL:** `/` and `/index`

**Method:** `GET`

## Get Devfile Registry Sample Index

Gets the index.json containing metadata about the Devfile samples in the devfile registry

**URL:** `/index/sample`

**Method:** `GET`


## Get Entire Devfile Registry Index

Gets the combined index.json containing metadata about the Devfile stacks **and** samples in the devfile registry.

**URL:** `/index/all`

**Method:** `GET`

## Get Devfile

Gets the requested devfile for a given stack in the devfile registry

**URL:** `/devfiles/<stack-name>`

**Method:** `GET`
