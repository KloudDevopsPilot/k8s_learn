# Replication Controller

## References

* <https://kubernetes.io/docs/concepts/workloads/controllers/replicationcontroller/>

## Why Replication Controller

![why_rc](../img/rc/why_rc.png)

## What is Replication Controller (Master Node ControllerManager ---> ReplicationController)

* responsible for managing the pod lifecycle(creates and manages the pods).
* It is responsible for ensuring that the specified number of pod replicas are running at any point in time.
* It has the capability to bring up or down the specified no of pods.

![rc](../img/rc/rc.png)

`Advantages`:-

* High Availability
* Load Balancing
* Scaling

## How Replication Controller Manages Pod's?

* using labels and selectors.

## Replication Loop

![replication_loop](../img/rc/replication_loop.png)

## YAML Walkthrough

![rc_yaml_walkthrough](../img/rc/rc_yaml_walkthrough.png)

`Note:-`

* Replication Controller replaced with newer version called `ReplicaSet`

![rc_note](../img/rc/rc_note.png)