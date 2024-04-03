---
title: "Persistentvolumes"
description: PersistentVolumes in Kubernetes provide durable storage resources for containerized applications. They abstract underlying storage infrastructure and are not namespaced, making them available cluster-wide. PVs are consumed by PersistentVolumeClaims and support various storage types, access modes, and features such as dynamic provisioning and reclaim policies. Administrators manage PVs to ensure efficient utilization and availability of storage resources across the Kubernetes cluster."
summary: ""
date: 2024-04-03T20:41:26+02:00
lastmod: 2024-04-03T20:41:26+02:00
draft: false
weight: 1003020
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
PersistentVolumes (PVs) in Kubernetes are a way to provide durable storage for containerized applications. They abstract underlying storage infrastructure, allowing administrators to provision storage resources independently of the pod or workload consuming it. PVs are not namespaced, meaning they are available cluster-wide and can be accessed by any pod within the Kubernetes cluster. 

A PersistentVolume represents a piece of storage in the cluster that has been provisioned by an administrator. It can be a physical disk, network storage, or cloud storage. PVs are consumed by PersistentVolumeClaims (PVCs), which are requests for storage made by pods. PVCs bind to PVs based on matching criteria such as access mode, storage class, and capacity.

PVs support various storage types and access modes, providing flexibility for different application requirements. They also support features like storage class, reclaim policy, and volume expansion. PVs are dynamically provisioned or statically configured by cluster administrators, depending on the storage infrastructure and policies in place.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** No
* **Shortnames:** 
  * pv
* **Verbs:**
  * create
  * delete
  * get
  * list
  * patch
  * update
  * watch

{{< /callout >}}
