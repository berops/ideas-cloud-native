# K8s interactive RBAC visualizer

## Problem

Troubleshooting workload permission issues, especially with more complex RBAC setups, is difficult. If there's a need to restrict permissions, figuring out which (cluster)role to touch and what are the consequences on other service-accounts or groups involved is cumbersome and error prone task. Similarly, in order to add a permission to a workload might not always be straightforward in these scenarios. Moreover, when hardening the security with RBAC, a full list of privileges would be handy.

## Solution

A GUI app that would show the list of actors, the (cluster)roles and (cluster)rolebindings. Dynamic filtering would be useful (e.g. for being able to clean-up roles without any rolebinding). Namespace filtering would be useful. Generator of full permission list for an actor would be userful, moreover being able to show for each permission (e.g. upon a mouse-click) which role(s) and rolebinding(s) are responsible for granting that particular permission.
