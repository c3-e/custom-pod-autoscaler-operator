[![Build](https://github.com/jthomperoo/custom-pod-autoscaler-operator/workflows/main/badge.svg)](https://github.com/jthomperoo/custom-pod-autoscaler-operator/actions)
[![codecov](https://codecov.io/gh/jthomperoo/custom-pod-autoscaler-operator/branch/master/graph/badge.svg)](https://codecov.io/gh/jthomperoo/custom-pod-autoscaler-operator)
[![go.dev](https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white&style=flat)](https://pkg.go.dev/github.com/jthomperoo/custom-pod-autoscaler-operator)
[![Go Report Card](https://goreportcard.com/badge/github.com/jthomperoo/custom-pod-autoscaler-operator)](https://goreportcard.com/report/github.com/jthomperoo/custom-pod-autoscaler-operator)
[![License](http://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

# Custom Pod Autoscaler Operator
This is the operator for managing Custom Pod Autoscalers (CPA). This allows you to add 
your own CPAs to the cluster to manage autoscaling deployments, enabling this is a 
requirement before you can add your own CPAs.  

The Custom Pod Autoscaler Operator is part of the 
[Custom Pod Autoscaler Framework](https://custom-pod-autoscaler.readthedocs.io/en/latest/).

## Installation
### Quick start
Run this to install the Operator and Custom Pod Autoscaler definition with cluster-wide scope on your cluster:
```
VERSION=v0.6.0
curl -L "https://github.com/jthomperoo/custom-pod-autoscaler-operator/releases/download/${VERSION}/cluster.tar.gz" | tar xvz --to-command 'kubectl apply -f -'
```
### Advanced
See the [install guide](INSTALL.md) to see more in depth installation options, 
such as namespace specific installs.

## Usage
See the [usage guide](USAGE.md) to see some simple usage options. For more indepth
examples, check out the 
[Custom Pod Autoscaler repo](https://github.com/jthomperoo/custom-pod-autoscaler).

## Developing

### Environment

Developing this project requires these dependencies:

* Go >= 1.13
* Golint
* [operator-sdk](https://github.com/operator-framework/operator-sdk) - 
[install guide](https://github.com/operator-framework/operator-sdk/blob/master/doc/user/install-operator-sdk.md)

### Commands

* `make` - builds the image for the operator
* `make lint` - lints the codebase
* `make generate` - generates boilerplate and YAML config for the operator