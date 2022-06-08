# POD

## What is POD

>
* automic unit of scheduling.
* pods are the smallest, most basic deployable objects in Kubernetes.
* a pod represents a single instance of a running process in your cluster.
* each pod gets its own unique ip address, when POD dies a new unique IP address assigned to POD
*  
  * in normal use-cases, 1 POD = 1 Conatiner
  * in exceptional use-cases 1 POD = multiple containers
    * When a Pod runs multiple containers, the containers are managed as a single entity and share   pod's resources

![smalles_unit](../img/pod/unit.png)


## Pod deployment 

![smalles_unit](../img/pod/pod_deployment.png)

`Note:-`

* usally 1 POD = 1 Container.
* if load increase we will scaleup(create) pods, if load decrease we will scaledown(delete) the pods.

![pod_scaling](../img/pod/pod_scaling.png)


## Multi-Container POD

![multi_container_pod](../img/pod/multi_container_pod.png)