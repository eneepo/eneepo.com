---
title: "Secrets"
description: "Secrets in Kubernetes are objects used to store sensitive information such as passwords, OAuth tokens, and SSH keys. They provide a way to securely store and manage sensitive data, ensuring that it is not exposed in plain text within container images or configuration files. Secrets can be mounted into pods as data volumes or exposed as environment variables, allowing applications to access the sensitive information securely at runtime."
summary: ""
date: 2024-04-03T20:41:59+02:00
lastmod: 2024-04-03T20:41:59+02:00
draft: false
weight: 1003013
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Secrets in Kubernetes are objects used to store sensitive information such as passwords, OAuth tokens, and SSH keys. They provide a way to securely store and manage sensitive data, ensuring that it is not exposed in plain text within container images or configuration files. Secrets can be mounted into pods as data volumes or exposed as environment variables, allowing applications to access the sensitive information securely at runtime.

{{< callout context="note" title="Resource details" icon="info-circle" >}}

* **Api group:** core
* **Namespaced:** Yes
* **Shortnames:** 
  * sec
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
