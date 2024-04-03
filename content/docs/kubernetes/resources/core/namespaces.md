---
title: "Namespaces"
description: "Namespaces are a way to divide cluster resources into logically named scopes. They provide a way to organize objects and segregate them within a Kubernetes cluster. Each namespace acts as a virtual cluster within the actual Kubernetes cluster, enabling multiple users, teams, or projects to share the same physical cluster without interfering with each other's work. Resources created within a namespace are isolated and accessible only to other resources within the same namespace, unless explicitly exposed."
summary: ""
date: 2024-04-03T20:40:01+02:00
lastmod: 2024-04-03T20:40:01+02:00
draft: false
weight: 1003007
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Namespaces are a way to divide cluster resources into logically named scopes. They provide a way to organize objects and segregate them within a Kubernetes cluster. Each namespace acts as a virtual cluster within the actual Kubernetes cluster, enabling multiple users, teams, or projects to share the same physical cluster without interfering with each other's work. Resources created within a namespace are isolated and accessible only to other resources within the same namespace, unless explicitly exposed.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** No
* **Shortnames:** 
  * ns
* **Verbs:**
  * create
  * delete
  * get
  * list
  * patch
  * update
  * watch

{{< /callout >}}
