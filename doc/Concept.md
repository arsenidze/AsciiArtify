## Introduction

This document provieds overview of tools for using kubernetes in local environment.  
Reviwed candidates: minilube, kind, k3d. 
The document contains a list of characteristics of each solution, their advandatages/disadvantages and recommended solution to choose.

## Characteristics

| Characteristics                                     | minikube                                                                                                                                                                                                                              | kind                                                                                                                                                                                          | k3d                                                                                                                                                                                                                              |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supported OS                                        | Linux, macOS, Windows                                                                                                                                                                                                                 | Linux, macOS, Windows                                                                                                                                                                         | Linux, macOS, Windows                                                                                                                                                                                                            |
| Supported arch                                      | amd64, arm64                                                                                                                                                                                                                          | amd64, arm64                                                                                                                                                                                  | amd64, arm64                                                                                                                                                                                                                     |
| Advantages                                          | Easy to install and use, supports various hypervisors, extensive documentation and community support, add-on capability                                                                                                               | Easy CI/CD integration, stable, multi-node clusters                                                                                                                                           | Fast cluster setup, lightweight, good CI/CD integration, supports multi-node clusters                                                                                                                                            |
| Disadvantages                                       | Limited scalability, resource-intensive, less suitable for complex CI/CD pipelines                                                                                                                                                    | More complex setup, fewer additional features, longer deployment time                                                                                                                         | Less widespread documentation, potentially complex for beginners, some functionality limitations                                                                                                                                 |
| Time to go from 0 to successful k8s deployment(sec) | 61.457                                                                                                                                                                                                                                | 44.850                                                                                                                                                                                        | 32.488                                                                                                                                                                                                                           |
| Description from official sites                     | minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.   All you need is Docker (or similarly compatible) container or a  Virtual Machine environment, and Kubernetes is a single command away | kind is a tool for running local Kubernetes clusters using Docker container “nodes”.  kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI. | k3d is a lightweight wrapper to run  k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.   k3d makes it very easy to create single- and multi-node  k3s clusters in docker, e.g. for local development on Kubernetes. |

## Summary

I recommend to go with k3d options.  
Reasons: 
- the smallest execution time - important factor for local development
- simple installation process
- low resources requirements

## Demo

![Image](./images/demo.gif)

Source: https://asciinema.org/a/8EbbuRcNBWM5WHvG6qtSlkHpI


## Used resources

- minikube supported os/arch - https://minikube.sigs.k8s.io/docs/start/?arch=%2Flinux%2Fx86-64%2Fstable%2Fbinary+download
- kind supported os/arch - https://kind.sigs.k8s.io/docs/user/known-issues/
- k3d supported os/arch - https://github.com/k3d-io/k3d/releases
- Benchmark - https://minikube.sigs.k8s.io/docs/benchmarks/timetok8s/v1.32.0/
- "The Single-Node Kubernetes Showdown: minikube vs. kind vs. k3d" - https://oilbeater.com/en/2024/02/22/minikube-vs-kind-vs-k3d/