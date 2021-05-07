# Devfile Registry

## What is a Devfile Registry?

A Devfile Registry is a service that stores and provides [devfile stacks](https://docs.devfile.io/devfile/2.0.0/user-guide/index.html) to Kubernetes developer tools like [Odo](https://odo.dev/), [Eclipse Che](https://www.eclipse.org/che/) and the OpenShift Developer Console. Devfile registries are based on the [OCI Specification](https://opencontainers.org/), and Devfile stacks are stored as OCI-artifacts in the registry. 

Each devfile stack corresponds to a specific runtime or framework (such as NodeJS, Quarkus, Wildfly, etc) and contains the following:
- A [devfile.yaml](https://docs.devfile.io/devfile/2.0.0/user-guide/index.html) (Required)
- A stack logo (Optional)
- Outer loop resources, such as Dockerfiles, and Kubernetes manifests (Optional)
- Plugins (Optional)

## Types of Devfile Registries

There are multiple types of Devfile registries that are used to provide devfile stacks to tools and users.

### Public Community Registry

This registry is hosted at [registry.devfile.io](https://registry.devfile.io) and provides stacks for various community tools to consume. Examples of such stacks include [NodeJS](https://registry.devfile.io/devfiles/nodejs), [Quarkus](https://registry.devfile.io/devfiles/java-quarkus), and [Open Liberty](https://registry.devfile.io/devfiles/java-openliberty).

The source repository for the stacks in this devfile registry is located at the [devfile/registry](https://github.com/devfile/registry) repository. 

### OpenShift Product Registry

(Not yet available, see https://github.com/devfile/api/issues/320) The devfile registry that hosts Red Hat-specific product stacks, such as JBoss EAP.

### On-Cluster Devfile Registry

Private, on-cluster devfile registries can be configured on your own Kubernetes cluster, deployed using either the [Devfile Registry Operator](https://github.com/devfile/registry-operator), or the [Devfile Registry Helm Chart](https://github.com/devfile/registry-support/tree/master/deploy/chart/devfile-registry). These devfile registries can be configured with custom devfile stacks suited to your own or your organization's needs.
