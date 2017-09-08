# Kubernetes cluster orchestration system

## Cluster
Kubernetes coordinates a highly available cluster of computers that are connected to work as a single unit.

Kubernetes automates the distribution and scheduling of application containers across a cluster in a more efficient way.

Consists of two types of resources:
 * *master* - cluster coordination
    * scheduling applications
    * maintaining applications' desired state
    * scaling applications
    * rolling out new updates
 * *nodes* - workers which run the application
    * is a VM or a physical computer
    * has a *Kubelet* for management und master communication
    * communicate with the master using the *Kubernetes API*


## Deployment and Lifecycle
 - the Deployment finds place in the *master*
 - Once you've created a Deployment, the Kubernetes master schedules mentioned application instances onto individual Nodes in the cluster.
 - Once the application instances are created, a Kubernetes Deployment Controller continuously monitors those instances. If the Node hosting an instance goes down or is deleted, the Deployment controller replaces it. This provides a self-healing mechanism to address machine failure or maintenance

## Pods
A Pod is a group of one or more application containers (such as Docker or rkt) and includes shared storage (volumes), IP address and information about how to run them.

Containers should only be scheduled together in a single Pod if they are tightly coupled and need to share resources such as disk.

 -  are mortal and have a lifecycle


## Tools

External:
 * Minikube for local cluster testing -> https://kubernetes.io/docs/getting-started-guides/minikube/
 * Helm applies configs to shards, revisioning

Integrated/Provided:
 * Kubectl for cluster interaction
  * *kubectl proxy* exposes deployed apps via http
  * kubectl get - list resources
  * kubectl describe - show detailed information about a resource
  * kubectl logs - print the logs from a container in a pod
  * kubectl exec - execute a command on a container in a pod
* Kubernetes dashboard

##### Credits, sources and some links of interest for further reading:
 * https://kubernetes.io/docs/tutorials/kubernetes-basics/
