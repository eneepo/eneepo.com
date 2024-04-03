---
title: "Endpoints"
description: "Endpoints in Kubernetes provide a way to connect services to the pods that they target. They are automatically created and managed by the Kubernetes control plane. Endpoints maintain a mapping between a service and the set of pods it routes traffic to. When a service is created, Kubernetes automatically creates an Endpoint object with the same name, which initially contains no endpoints. As pods come and go, the Endpoints object is updated to reflect the current set of endpoints for the service. "
summary: ""
date: 2024-04-03T20:43:12+02:00
lastmod: 2024-04-03T20:43:12+02:00
draft: false
weight: 1003080
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Endpoints in Kubernetes provide a way to connect services to the pods that they target. They are automatically created and managed by the Kubernetes control plane. Endpoints maintain a mapping between a service and the set of pods it routes traffic to. When a service is created, Kubernetes automatically creates an Endpoint object with the same name, which initially contains no endpoints. As pods come and go, the Endpoints object is updated to reflect the current set of endpoints for the service. 

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** Yes
* **Shortnames:** 
  * ep
* **Verbs:**
  * create
  * delete
  * deletecollection
  * get
  * list
  * patch
  * update

{{< /callout >}}
