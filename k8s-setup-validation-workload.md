# K8s Cluster Setup Validation Workload

## Problem

We deploy clusters in very heterogeneous environments, not always on a HW under our control and often combined with various public cloud provider IaaS. After a cluster is spawned on such an infrastructure, how can we run basic sanity checks before declaring the setup truly successful and handing it over for consumption?

## Suggestion

There are several criterias of a successful setup that can be validated by deploying a special workload. For example:
- cluster/namespace capacity (check by deploying pods with defined `.specs.containers.requests.{cpu,memory}` configuration)
- network connectivity, (internal, external) incl. `NetworkPolicy` setup (check by running client/server connections between pods as per the needs)
- DNS resolution tests

The workload requirements would be described in form of an input for a central test controller. Based on this inputs, the controller would run a series of tests, then collect and present the results.
