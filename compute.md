---



copyright:
  years: 2016
lastupdated: "2016-10-31"



---

{: shortdesc: .shortdesc}
{: codeblock: .codeblock}
{: screen: .screen}
{: new_window: target="_blank"}

# Compute
{: #apidocs}

{{site.data.keyword.Bluemix_short}} is a flexible platform that has multiple options for deploying your code. There are four *compute options* that allow you to run all of your applications in {{site.data.keyword.Bluemix_notm}}. You must choose the right option for your applications and infrastructure.
{: shortdesc}

The four compute options available in {{site.data.keyword.Bluemix_notm}} are:
* **IBM {{site.data.keyword.Bluemix_notm}} OpenWhisk (OpenWhisk)**: OpenWhisk is an event-driven platform where you can run applications that have logic responding to events from {{site.data.keyword.Bluemix_notm}} services or external sources.
* **Instant Runtimes (Cloud Foundry)**: {{site.data.keyword.Bluemix_notm}} runtimes are based on Cloud Foundry, an open source Platform as a Service (PaaS) environment where you can build, deploy, and run your applications.
* **IBM Containers (Docker)**: IBM Containers are Docker-based containers, which are lightweight virtual machines that have all of the code, runtime, and dependencies that your application needs.
* **Virtual Servers (OpenStack)**: IBM Virtual Servers gives you a virtual machine (VM) with preinstalled operating systems that you can use to run your applications.

## Choosing the right option for you

Based on your applications and the infrastructure needs you have, you will need to choose the right compute option. Consider the following features and comparisons of each option.

| Feature | OpenWhisk | Cloud Foundry | Containers | Virtual Servers |
|--------- |----------- |--------------- |------------ |-----------------|
|Workload characteristics | <ul><li>stateless and short-living</li> <li>uses a well-defined group of languages</li></ul> | <ul><li>stateless</li><li>http(s) and websockets</li></ul> | <ul><li>longer-living</li><li>uses any protocol</li><li>custom OS (binaries required)</li></ul> | <ul><li>allows OS customizations and full OS control</li><li>stronger isolation requirements</li></ul> |
|Workload examples | <ul><li>API / microservice / web app implementations</li><li>mobile backends</li><li>reaction to streaming / data IoT, Cognitive, etc. events</li></ul> | high-volume web apps / APIs | <ul><li>Continuously running processes (such as game engines)</li><li>distributed technologies (such as mongodb or zookeeper)</li></ul> | <ul><li>apps having special OS requirements</li><li>apps packaged into existing VM images</li><li>live-videostreams (resource-heavy)</li></ul> |
|Time to provision | milliseconds | seconds/minutes | seconds/minutes | minutes |
|Utilization | highest | higher | higher | high |
|Ability to reuse existing apps | low | lower | medium | high |
|Charging granularity | blocks of ms execution time | hours | hours | hours |
|Developer view | app code only | app code only | container | VM |
|Autoscaling | inherent, no delay | management funtion | management function | management function|
|Artifact | action code, trigger, rule | app code | container | VM |
|Developer usage | <ul><li>uploads artifacts only</li><li>no explicit management of computing resources required</li><li>no starting and stopping of applications required</li></ul> |<ul><li>uploads complete application using a CF supported runtime</li><li>explicitly binds services to application</li><li>explicitly starts/stops the cloud application</li><li>entire application is atomically packaged and executed</li><li>changes require deployment of the entire application</li></ul> | <ul><li>creates application or microservices and packages in a container</li><li>deploys the container to the server</li><li>must manage loading Docker components and all communication between containers</li></ul> |<ul><li>installs or clones an existing OS, packages the OS in a VM image, and deploys to the server</li><li>developer must start and stop the entire VM</li></ul> |
{: caption="Table 1. Feature comparison of compute options" caption-side="top"}
