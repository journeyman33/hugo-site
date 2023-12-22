---
title: How to Deploy Applications to Kubernetes
date: 2023-11-14T16:12:16+02:00
draft: false
tags: ["html","css"]
categories: ["tech"]
---
Kubernetes simplifies the running of containerized application by automating many things like scaling, self-healing, high-availability, service discovery, load balancing, updates and rollbacks. This is enabled by a unified API ( Controller Manager, Scheduler, etcd, Kubelet, Kube-proxy ) that allows for applications to be defined declaratively in yaml, handle configuration management, persistent storage and RBAC. When the API is extended, with CRD's (Custom Resource Definitions), Admissions Controllers and 
with Controllers/Operators, Kubernetes then goes beyond 'an orchestrator of containers' 

With all these automation features that have made things easy comes complexity. That's  because the underlying is complex. Once again the new goal is to abstract away this complexity and try and make things 'simpler'. It's possible, with a wrapper layer, to deploy an application to Kubernetes without having to know the  Kubernetes resources (objects) as shown below. Yet it's probably worth just knowing, especially if you want to appreciate what ever layer that does get put on top,  the <span style="color: green">**underlying kubernetes resources:**</span> 
#### <span style="color:green;"> -namespace,deploy,pods,rs,service,ingress,hpa,netpol,limits,quotas </span>
![k8s Exposed Pod](/static/img/k8s-exposed-pod.png)

<!-- <img src="/home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="Basic K8s cluster resource"> - this does not render either-->

<!--  <img src="https://github.com/kubernetes/community/blob/master/icons/docs/k8s-exposed-pod.png?raw=true" alt="K8s Resources">   -->

<!--   <img src="home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="K8s Resources">  -->

<!--    <img src="/static/img/k8s-exposed-pod.png" alt="K8s Resources">   -->

#### <span style="color:green;">- persistent volume, persistent volume claim </span>
<!--  ![pv](/static/img/k8s-resources/pv-128.png)  -->

<!--  <img src="/static/img/k8s-resources/pv-128.png" alt="pv" width="100" height="100">
  -->


![pv](/static/img/k8s-resources/pv-128.png)  ![pvc](/static/img/k8s-resources/pvc-128.png)]


<!--  <img src="https://github.com/kubernetes/community/blob/master/icons/png/resources/labeled/c-role-128.png" alt="cluster role">  -->
 
There are many ways to deploy applications to Kubernetes.  What is the optimal way? In the following posts I am going to explore the following methods:
1. **Kubectl**
    - [Kubectl](/posts/kubectl/kubectl/): Content related to Kubectl.

2. **Operator Framework**
    - [Operator Framework](/posts/operator-framework/operator-framework/): Content related to the Operator Framework.

3. **Helm**
    - [Helm](/posts/helm/helm/): Content related to Helm.

4. **Kustomize**
    - [Kustomize](/posts/kustomize/kustomize/): Content related to Kustomize.

5. **Acorn**
    - [Acorn](/posts/acorn/acorn/): Content related to Acorn.

6. **Cue**
    - [Cue](/posts/cue/cue/): Content related to Cue.

7. **Kubefirst**
    - [Kubefirst](/posts/kubefirst/kubefirst/): Content related to Kubefirst.




