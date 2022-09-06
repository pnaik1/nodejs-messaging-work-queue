# Messaging Work Queue Example for Node.js

[![Greenkeeper badge](https://badges.greenkeeper.io/nodeshift-starters/nodejs-messaging-work-queue.svg)](https://greenkeeper.io/)

## Purpose

This example application demonstrates how to dispatch tasks to a scalable
set of worker processes using a message queue. It uses the AMQP 1.0
message protocol to send and receive messages.

## Prerequisites

* Node.js version 12, 14 or 16

* The user has access to an OpenShift instance and is logged in.

* The user has selected a project in which the frontend and backend
  processes will be deployed.

## Deployment

Run the following commands to configure and deploy the applications.

```bash
$ oc create -f service.amqp.yaml

$ ./start-openshift.sh
```
## Modules

The `frontend` module serves the web interface and communicates with
workers in the backend.

The `worker` module implements the worker service in the backend.

### OpenTelemetry with OpenShift Distributed Tracing Platform

Clone this repository, switch the branch to `opentelemetry-js-rhosdt`
and follow the instructions on README.md

Or visualize the instructions via github https://github.com/nodeshift-starters/nodejs-messaging-work-queue/tree/opentelemetry-js-rhosdt#opentelemetry-with-openshift-distributed-tracing-platform
