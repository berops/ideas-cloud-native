# Open-Source Ideas: Cloud-Native

This is a maintained list of ideas for cloud-native open-source projects.

## Purpose

We think there's a reason for creating such a list for two reasons:
1. Simply, there are many ideas around for solving outstanding problems.
2. We have been meeting people who were interested in starting an open-source project, but were unsure about the problem to be worked on.

Obviously, such a collection of ideas shall be an open-source repository itself too.

## Workflow

The envisioned workflow is the following:
1. A new idea is logged via a Pull-Request (PR). The scope of this repo is limited to cloud-native topics.
2. During a staging phase (2 weeks), it receives positive and/or negative votes.
3. If there's more positive than negative votes after the staging phase, the PR is merged. Otherwise it's declined. The same (or similar PR) can be submitted more than once.
4. The PR carries the necessary description of the idea, written in at least two paragraphs (1. problem, 2. solution).
5. If the idea makes it to real-world and turns into an open-source project, the link (or links, if there are more projects spawned) are added into this list accordingly.
6. If the time tells, that an idea, which has been added to a list some time ago is not relevant anymore, a PR is created to remove it. Again, 2 weeks of staging followed by the same evaluation principles apply.

## Ideas

[K8s cluster setup validation workload](k8s-setup-validation-workload.md) A workload that will be deployed after a cluster is created in order to run a series of conformance tests (e.g. on available capacity, connectivity, DNS resolution)

[K8s RBAC interactive visualizer](k8s-rbac-interactive-visualizer) A GUI app for displaying a cluster RBAC setup, with links among groups, service-accounts, roles and bindings. This includes basic interaction with the user, i.e. displaying the details of the role upon selection or describing a consolidated list of privileges.