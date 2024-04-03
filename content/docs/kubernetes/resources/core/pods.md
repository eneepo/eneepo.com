---
title: "Pods"
description: "Pods are the smallest and simplest Kubernetes objects. They represent a single instance of a running process in a cluster. Pods can contain one or more containers, such as Docker containers. They share network and storage resources, and can be created, deployed, and managed as a unit. Pods run on nodes, which are the individual machines within a Kubernetes cluster."
summary: ""
date: 2024-04-03T20:22:39+02:00
lastmod: 2024-04-03T20:22:39+02:00
draft: false
weight: 1003005
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Pods are the smallest and simplest Kubernetes objects. They represent a single instance of a running process in a cluster. Pods can contain one or more containers, such as Docker containers. They share network and storage resources, and can be created, deployed, and managed as a unit. Pods run on nodes, which are the individual machines within a Kubernetes cluster.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** Yes
* **Shortnames:** 
  * po
* **Verbs:**
  * create
  * delete
  * deletecollection
  * get
  * list
  * patch
  * update
  * watch

{{< /callout >}}

## Example
Imperative command:
```bash
kubectl run my-nginx --image=nginx --labels="app=my-app,env=prod" --port=80 --env="NGINX_PORT=80" --restart=Always
```

Yaml specification for the command above:
```yaml
apiVersion: v1              # Specifies the Kubernetes API version being used for this resource.
kind: Pod                   # Indicates that this YAML defines a Kubernetes Pod resource.

metadata:                   # Metadata section contains information about the Pod.
  creationTimestamp: null     # The timestamp when this Pod was created, initially set to null.
  labels:                     # Labels are key-value pairs used to identify and categorize the Pod.
    app: my-app               # Label indicating the application name is 'my-app'.
    env: prod                 # Label indicating the environment is 'prod'.
  name: my-nginx              # The name assigned to this Pod.

spec:                       # The specification section defines the desired state of the Pod.
  containers:                 # List of containers running inside this Pod.
  - env:                      # Environment variables to be set within the container.
    - name: NGINX_PORT        # Name of the environment variable.
      value: "80"             # Value assigned to the NGINX_PORT environment variable.
    image: nginx              # The Docker image to be used for this container.
    name: my-nginx            # Name of this container within the Pod.
    ports:                    # List of ports to be exposed by this container.
    - containerPort: 80       # The container will listen on port 80.
    resources: {}             # Resource requests and limits can be specified here.
  dnsPolicy: ClusterFirst     # Defines the DNS resolution policy for this Pod.
  restartPolicy: Always       # Specifies the Pod's restart policy, which is set to "Always."

status: {}                    # The current status of the Pod (empty in this YAML as it's an initial state).

```

## Pod states
* **Pending:** Pod has been accepted by Kubernetes but is not running yet.
* **Running:** Pod has been bound to a node and all containers are running.
* **Succeeded:** All containers in the Pod have terminated successfully and won't be restarted.
* **Failed:** All containers in the Pod have terminated, and at least one container terminated in failure.
* **Unknown:** State of the Pod could not be obtained.

## Commands
```bash
# Create a Pod from a YAML file
kubectl create -f <pod.yaml>

# Get information about all Pods in the current namespace
kubectl get pods

# Get detailed information about a specific Pod
kubectl describe pod <pod_name>

# Get logs from a Pod
kubectl logs <pod_name>

# Follow logs from a Pod
kubectl logs -f <pod_name>

# Execute a command in a Pod
kubectl exec -it <pod_name> -- <command>

# Delete a Pod
kubectl delete pod <pod_name>

# Delete all Pods in the current namespace
kubectl delete pods --all

# Quickly generate a new pod definition 
kubectl run <pod_name> --image nginx --dry-run=client -o yaml > pod-definition.yaml

# Start the nginx pod using the default command, but use custom arguments (arg1 .. argN) for that command
kubectl run nginx --image=nginx -- <arg1> <arg2> ... <argN>

# Start the nginx pod using a different command and custom arguments
kubectl run nginx --image=nginx --command -- <cmd> <arg1> ... <argN>

# Generate a pod definition out of an exisiting pod
kubectl get pod <pod_name> -o yaml > pod-definition-get.yaml
```