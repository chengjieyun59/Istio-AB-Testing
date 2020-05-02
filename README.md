# Istio-AB-testing

## Problem:
Currently there is no GUI javascript solution for A/B testing deployments in Kubernetes with Istio Mesh Service. Lack of such a tool creates a larger workload on the DevOps team to manually participate in A/B testing deployments, especially in more loosely coupled applications.

## Solution:
Tikitaka aims to provide a simple-to-use Kubernetes operator that automates the promotion of A/B testing deployments using Istio routing for traffic shifting and Kiali for metrics analysis. Tikitaka brings a new approach, that packaging the common activities and best practices by development teams and create deployment automation procedures, so that the weight on DevOps teams will be decremented and a wider range of developers will be participating on continuous deployment and routing processes within projects that use Kubernetes for their micor-service orchestration.

## Implementation:
Tikitaka takes a Kubernetes deployment and a docker image and creates a series of objects (Kubernetes deployments, ClusterIP services, virtual services, and destinations rules). The current process that Tikitaka supports is A/B testing operations with sticky sessions within Kubernetes that uses Istio as their control plane, with Canary Release Management, Default Injections, Security Injections automations as built-in packages. Currently, Tikitaka uses Kiali for presenting visualization to users. Also, within 6 months, Tikitaka is planning to be totally solution-independent and the whole tracing and telemetry infrastructure is to be built using OpenTelemetry Standards.
