# EFREI_ST2VAS_Project
A vagrant script to build a pair of Ubuntu based VMs (master and worker) with MicroK8s and Docker installed in order to experiment with Kubernetes

## Kubernetes Distribution

For this deployment, we are using __Kubeadm__ :

Schema of our infrastructure:

| Master  | Worker         |
| :------ |---------------:|
| master  | worker1        |
|         | worker2        | => not done with the vagrant file
|         | worker3        | => not done with the vagrant file

>[Code reference](https://github.com/scriptcamp/vagrant-kubeadm-kubernetes)

>[CNI](https://github.com/cilium/cilium)

## Application

> stoll some issue

[__Helm__](https://ibm.github.io/helm101/Lab1/)

__Helm__ helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application.

## Monitoring

For the __monitoring__ we are using [__Prometheus__](https://github.com/prometheus/prometheus)

For the __logging__ we are using [__Fluentd__](https://github.com/fluent/fluentd)

And for the __tracing__ we are using [__Jaeger__](https://github.com/jaegertracing/jaeger)

> We may add some dashboard using __Grafana__

## Security

[__Open policy agent__](https://github.com/open-policy-agent/opa)

The __Open Policy Agent__ is an open source, general-purpose policy engine that unifies policy enforcement across the stack. OPA provides a high-level declarative language that lets you specify policy as code and simple APIs to offload policy decision-making from your software. You can use OPA to enforce policies in microservices, Kubernetes, CI/CD pipelines, API gateways, and more.

## Storage

We used the default configuration of [__Rook-ceph__](https://github.com/rook/rook) as our storage solution.

Pods in Kubernetes are designed to be __ephemeral__. So, in order to keep the data, we need to save it on Persistent Volume (PV).
One of the ways to dynamically provision PV, is by using rook-ceph.
__Ceph__ is a highly scalable distributed storage solution for block storage, object storage, and shared filesystems. It is software-based, meaning it doesn’t rely on specific hardware features.
__Rook__ is an operator that Rook simplifies the deployment of Ceph in a Kubernetes cluster.

## Service-mesh

> done

[__Linkerd__](https://github.com/linkerd/linkerd2)

__Linkerd__ is a service mesh for Kubernetes. It makes running services easier and safer by giving you runtime debugging, observability, reliability, and security—all without requiring any changes to your code.

## Feature of your choice

[__Envoy proxy__](https://github.com/envoyproxy/envoy)

__Envoy__ is an open-source proxy created at Lyft. Envoy tries to solve the problems about Networking and Observability by making networks more transparent to applications. It also provides a way to better collect stats so that it’s easier to debug and trace the issues.

[__Chaos Engineering with Chaos Mesh__](https://github.com/chaos-mesh/chaos-mesh)

__Chaos Mesh__ is a cloud-native Chaos Engineering platform that orchestrates chaos on Kubernetes environments.
