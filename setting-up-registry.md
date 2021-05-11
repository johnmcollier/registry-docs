# Setting Up Your Own Devfile Registry

The following documents the steps to set up your own Devfile Registry.

## Create a Git Repository

First, we need to set up a Git repository to store the devfile stacks that will then be packaged into the devfile registry.

The repository can be named however you like, but there are some basic requirements:

1) A `stacks/` folder for storing the devfile stacks in your registry. Each folder under `stacks/` must correpond to a specific stack (e.g. `stacks/java-wildfly/`)
2) An `extraDevfileEntries.yaml` in the root of the repository if any external devfile stacks/samples need to be packaged in the devfile registry
    
    - For the format of this file, please see [its schema](extra-devfile-entries-schema.md)

You may find it useful to instead fork the [devfile/registry](https://github.com/devfile/registry) and add/remove any stacks as needed from there, as it already includes the necessary build tools (Dockerfile, build scripts, etc) and test resources.

## Add Your Own Stacks

Each devfile stack that you add to the devfile registry must contain a devfile.yaml file minimally.

Additionally, any other files required for the stack to function can be included as well, such as:

- VSX plugins
- Outerloop resources (such as Dockerfile or Kubernetes Manifests)

Please consult the [Stack authoring guide](https://docs.devfile.io/devfile/2.0.0/user-guide/authoring-stacks.html) for assistance on creating your own devfile stack

## Build Registry

**Note:** We strongly recommend doing these steps as part of a build-stage in a multi-stage Docker build. For an example on how this can be done, consult the [devfile/registry repository's Dockerfile](https://github.com/devfile/registry/blob/master/.ci/Dockerfile)

If you wish to run the registry build outside of a Docker build, please consult the [devfile registry build tools readme](https://github.com/devfile/registry-support/tree/master/build-tools).

## Deploy Registry

ToDO
