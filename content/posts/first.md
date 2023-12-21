---
title: How to Deploy Applications to Kubernetes
date: 2023-11-14T16:12:16+02:00
draft: false
tags: ["html","css"]
categories: ["tech"]
---
Kubernetes simplifies the running of containerized application by automating scaling, self-healing, high-availability, service discovery, load balancing, updates and rollbacks. This is enabled by a unified API ( Controller Manager, Scheduler, etcd, Kubelet, Kube-proxy ) that allows for applications to be defined declaratively in yaml, handle configuration management, persistent storage and RBAC. When the API is extended, with CRD's (Custom Resource Definitions), Admissions Controllers and 
with Controllers/Operators, Kubernetes then becomes more than 'an orchestrator of containers' 

With all these automation features that have made things easy comes complexity; that's  because the underlying is complex. Once again the new goal is to abstract away this complexity and try and make things 'simpler'. It's possible, with a wrapper layer, to deploy an application to Kubernetes without having to know the basic Kubernetes resources (objects) as shown below, yet sooner or later when there is a problem it's going to be worth knowing the *underlying kubernetes resources :*
#### namespace,nodes,deploy,pod,rs,service,ingress,hpa,netpol,limits,quota ... pv,pvc
![k8s Exposed Pod](/static/img/k8s-exposed-pod.png) 
<!-- <img src="/home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="Basic K8s cluster resource"> - this does not render either-->
<img src="https://github.com/kubernetes/community/blob/master/icons/docs/k8s-exposed-pod.png?raw=true" alt="K8s Resources">

<img src="home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="K8s Resources">

<img src="/static/img/k8s-exposed-pod.png" alt="K8s Resources">

There are many ways to deploy applications to Kubernetes.  What is the optimal way? In the following post I am going to explore the following methods:
1. kubectl
2. Operator framework
3. Helm
4. Kustomize
5. Acorn
6. Cue
7. Kubefirst




