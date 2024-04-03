---
title: "Configmaps"
description: "ConfigMaps are Kubernetes objects used to store non-sensitive configuration data in key-value pairs. They provide a way to decouple configuration artifacts from container images, allowing for more flexible and portable applications. ConfigMaps can be mounted as volumes or exposed as environment variables within containers, providing configuration data to applications at runtime. This separation of configuration from code simplifies application management and promotes best practices for configuration management in a Kubernetes environment."
summary: ""
date: 2024-04-03T20:40:51+02:00
lastmod: 2024-04-03T20:40:51+02:00
draft: false
weight: 1003011
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
ConfigMaps are Kubernetes objects used to store non-sensitive configuration data in key-value pairs. They provide a way to decouple configuration artifacts from container images, allowing for more flexible and portable applications. ConfigMaps can be mounted as volumes or exposed as environment variables within containers, providing configuration data to applications at runtime. This separation of configuration from code simplifies application management and promotes best practices for configuration management in a Kubernetes environment.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** Yes
* **Shortnames:** 
  * cm
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

