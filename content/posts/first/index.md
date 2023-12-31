---
title: How to Deploy Applications to Kubernetes
date: 2023-11-14T16:12:16+02:00
draft: false
tags: ["html","css"]
categories: ["tech"]
resources:
  - src: "/assets/img/k8s-resources/*"
    name: "k8s-resources"
    title: "k8s-resources"

---
Kubernetes simplifies the running of containerized application by automating many things like scaling, self-healing, high-availability, service discovery, load balancing, updates and rollbacks. This is enabled by a unified API ( Controller Manager, Scheduler, etcd, Kubelet, Kube-proxy ) that allows for applications to be defined declaratively in yaml, handle configuration management, persistent storage and RBAC.

 When the API is extended, with CRDs (Custom Resource Definitions), Admissions Controllers and with Controllers/Operators, Kubernetes then goes beyond an 'orchestrator of containers':

- to provision cloud infrastructure or custom applications through Crossplane created CRDs,
- to enforce security policies through a Kyverno Admission Controller,
- to synchronize the cluster manifests with the source of truth on Github through ArgoCD's CRDs,
- to provision an Istio service mesh or other side car patterns like Knative or Dapr,
- to enable an environment of application-specific-controllers, or operators, to  manage applications:

    - with the Operator Framework or Red Hat's Openshift.
    - with Charmed Operators on Ubuntu.
    - with VMware's Tanzu.  



With all the automation features (on vanilla Kubernetes) that have made things easy comes complexity. That’s because the underlying is complex. However, once again, the new goal, it seems,  is to abstract away this complexity and try and make things ‘simpler’. It is possible, with one CRD wrapper layer (from acorn.io) to create and deploy an application to Kubernetes without having to know the Kubernetes resources (objects), shown below. Yet it’s probably worth just knowing, especially if you want to appreciate what ever layer that does get put on top of the <span style="color: green">**underlying kubernetes resources:**</span> 
#### <span style="color:green;"> (1) namespace, deployment, pod, replicaset ,service, ingress, horizontal autoscaler, network policy, limits, quotas </span>
![k8s Exposed Pod](/static/img/k8s-exposed-pod.png)

<!-- <img src="/home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="Basic K8s cluster resource"> - this does not render either-->

<!--  <img src="https://github.com/kubernetes/community/blob/master/icons/docs/k8s-exposed-pod.png?raw=true" alt="K8s Resources">   -->

<!--   <img src="home/charles/hugo/third-site/static/img/k8s-exposed-pod.png" alt="K8s Resources">  -->

<!--    <img src="/static/img/k8s-exposed-pod.png" alt="K8s Resources">   -->

#### <span style="color:green;"> (2) persistent volume, persistent volume claim, config map, secret, endpoint, service account, role, cluster role, cluster role binding and pod security policy </span>
<!--  ![pv](/static/img/k8s-resources/pv-128.png)  -->

<!--  <img src="/static/img/k8s-resources/pv-128.png" alt="pv" width="100" height="100">
  -->

<!--   ![pv](/static/img/k8s-resources/pv-128.png)  ![pvc](/static/img/k8s-resources/pvc-128.png)]     -->

<!-- {{ $image := resources.Get "img/k8s-resources/*.png }}   -->

<!--  {{< img  "/assets/img/k8s-resources/pv-128.png" "50" "PV" >}}
      {{< img  "/assets/img/k8s-resources/pvc-128.png" "50" "PVC" >}}   -->
![pv]({{ .Resources.Get "pv-128.png" | relURL }})




![pv](/static/img/k8s-resources-40/pv-128.png)
![pvc](/static/img/k8s-resources-40/pvc-128.png)
![cm](/static/img/k8s-resources-40/cm-128.png)
![secret](/static/img/k8s-resources-40/secret-128.png)
![ep](/static/img/k8s-resources-40/ep-128.png)
![sa](/static/img/k8s-resources-40/sa-128.png)
![role](/static/img/k8s-resources-40/role-128.png)
![c-role](/static/img/k8s-resources-40/c-role-128.png)
![crb](/static/img/k8s-resources-40/crb-128.png)
![psp](/static/img/k8s-resources-40/psp-128.png)
<!--  <img src="/assets/img/k8s-resources/pod-128.png" alt="Pod">    -->

<!-- Resizing; page resource method 1 -->

<!--
{{ $image := resources.Get "k8s-resources/pv-128.png" }}
{{ with $image }}
  {{ $resized := $image.Resize "70x" }}
  ![pv]( {{ $resized.RelPermalink }} )
{{ end }}
-->


<!-- Resizig page resourde method 2 -->
<!--  
{{ $pv := .Page.Resources.GetMatch "k8s-resources/pv-128.png" }}
{{ $pv := $pv.Resize "77x" }}
<img src="{{ $pv.RelPermalink }}" width="{{ $pv.Width }}" height="{{ $pv.Height }}">
-->

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




