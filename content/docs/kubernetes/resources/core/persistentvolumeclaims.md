---
title: "Persistentvolumeclaims"
description: "PersistentVolumeClaims (PVCs) in Kubernetes are requests for storage resources by a user. They allow users to request specific types of storage, such as persistent storage, and provide an abstraction layer between users and storage implementation details. PVCs enable users to consume storage resources without needing to know the details of the underlying storage infrastructure. When a PVC is created, Kubernetes dynamically provisions the requested storage based on available PersistentVolumes (PVs) that match the PVC's requirements."
summary: ""
date: 2024-04-03T20:41:14+02:00
lastmod: 2024-04-03T20:41:14+02:00
draft: false
weight: 1003021
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
PersistentVolumeClaims (PVCs) in Kubernetes are requests for storage resources by a user. They allow users to request specific types of storage, such as persistent storage, and provide an abstraction layer between users and storage implementation details. PVCs enable users to consume storage resources without needing to know the details of the underlying storage infrastructure. When a PVC is created, Kubernetes dynamically provisions the requested storage based on available PersistentVolumes (PVs) that match the PVC's requirements.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** Yes
* **Shortnames:** 
  * pvc
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


