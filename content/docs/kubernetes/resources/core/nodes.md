---
title: "Nodes"
description: ""
summary: ""
date: 2024-04-03T20:41:01+02:00
lastmod: 2024-04-03T20:41:01+02:00
draft: false
weight: 1003002
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Nodes in Kubernetes are individual machines (physical or virtual) in a cluster that run containerized applications. They are responsible for hosting and running pods, which are the basic unit of work in Kubernetes. Each node has a Kubernetes agent called Kubelet, which manages the node and communicates with the master to ensure pods are running and healthy. Nodes also run various Kubernetes system components, such as the container runtime (e.g., Docker), kube-proxy for networking, and others.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** No
* **Shortnames:** 
  * no
* **Verbs:**
  * create
  * delete
  * get
  * list
  * patch
  * update
  * watch

{{< /callout >}}
