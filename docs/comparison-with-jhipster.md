---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Comparison with Jhispter
nav_order: 10
---
## [About Jhipster](https://www.jhipster.tech/)
JHipster is a development platform to quickly generate, develop, and deploy modern web applications and microservice architectures. It supports many frontend technologies, including Angular, React, and Vue. It even has mobile app support for Ionic and React Native. On the backend, it supports Java, Node.js, and .NET. It embraces cloud native principles with Docker and Kubernetes. Deployment support exists for AWS, Azure, Google Cloud Platform, Heroku, and OpenShift.

## Saral vs Jhipster
- **Design Language** - Jhispter uses a proprietary design language to build applications. Whereas, Saral lets you build applications in plain old java.
- **Custom code** - Jhipster allows you to inject custom code in the generated application. However, to plugin your code you would have to understand the jhispter generated code. On the other hand, Saral lets you provide the custom code in the project design. There is no code generation involved with Saral. It adds natively supported capabilities to the provided project design through annotations.
- **Syntax** - Jhipster uses entities definition as the syntax to specify project design. Whereas, Saral uses Domain driven design terminology as the syntax. DDD has been proven to work in the long term for large enterprise systems.
- **Lifecycle** - Jhipster is foccussed on project generation to give a head start for PoCs. Whereas, Saral is focussed on end to end lifecycle of the project including - development, testing, deployment, monitoring, improvements.