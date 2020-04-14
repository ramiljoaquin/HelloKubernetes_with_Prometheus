# Hello Kubernetes with Prometheus

![Kube architecture][logo]

[logo]: https://github.com/ramiljoaquin/HelloKubernetes_AKS/blob/master/assets/KubeArchitecture.png 'Kubernetes architecture'

## Course details

1h 10m Advanced Released: 8/7/2018

In order to prevent outages, it's essential that you leverage a monitoring and alerting tool in your Kubernetes environment. Prometheus—an open-source systems monitoring and alerting toolkit—pairs particularly well with Kubernetes. In this course, learn how this toolkit integrates with Kubernetes and works to monitor distributed systems. Instructor Robert Starmer steps through how to enable Prometheus monitoring and shares how Prometheus monitors Kubernetes systems. He also discusses monitoring application-specific data, adding sidecar containers for app data, filtering and combining metrics, and displaying metrics in the web console. To wrap up, he discusses how to create a simple alert in Prometheus and generate application-driven alerts.

## Learning objectives

Logging vs. monitoring
Enabling Prometheus monitoring
Capturing Kubernetes infrastructure data
Capturing container data with cAdvisor
Monitoring application-specific data
Filtering and combining metrics
Displaying metrics in the web console
Using Grafana as a dashboard
Using metrics data
Skills covered in this course
Prometheus.ioKubernetes

What they do
Software Developer Software Developer Technology Manager Software Developer Technology Manager
Where they work
IBM IBM Accenture Accenture Tata Consultancy Services Tata Consultancy Services AT&T AT&T Infosys Infosys

## Instructor

Robert Starmer
Robert Starmer
Cloud Advisor, Founder of Kumulus Technologies

## OVERVIEW

What is Prometheus?
Features
Components
Architecture
When does it fit?
When does it not fit?
What is Prometheus?

Prometheus is an open-source systems monitoring and alerting toolkit originally built at SoundCloud. Since its inception in 2012, many companies and organizations have adopted Prometheus, and the project has a very active developer and user community. It is now a standalone open source project and maintained independently of any company. To emphasize this, and to clarify the project's governance structure, Prometheus joined the Cloud Native Computing Foundation in 2016 as the second hosted project, after Kubernetes.

For more elaborate overviews of Prometheus, see the resources linked from the media section.

## Features

Prometheus's main features are:

a multi-dimensional data model with time series data identified by metric name and key/value pairs
PromQL, a flexible query language to leverage this dimensionality
no reliance on distributed storage; single server nodes are autonomous
time series collection happens via a pull model over HTTP
pushing time series is supported via an intermediary gateway
targets are discovered via service discovery or static configuration
multiple modes of graphing and dashboarding support
Components
The Prometheus ecosystem consists of multiple components, many of which are optional:

the main Prometheus server which scrapes and stores time series data
client libraries for instrumenting application code
a push gateway for supporting short-lived jobs
special-purpose exporters for services like HAProxy, StatsD, Graphite, etc.
an alertmanager to handle alerts
various support tools
Most Prometheus components are written in Go, making them easy to build and deploy as static binaries.

## Architecture

This diagram illustrates the architecture of Prometheus and some of its ecosystem components:

![Prometheus architecture][plogo]

[plogo]: https://github.com/ramiljoaquin/HelloKubernetes_with_Prometheus/blob/master/docs/architecture.png 'Kubernetes architecture'
