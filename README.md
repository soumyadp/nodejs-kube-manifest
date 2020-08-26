# nodejs-kube-manifest
Hosts a simple Kubernetes manifests file to expose a NodeJS server with the following config

- There are 10 replicas running.
- The deployment autoscales at average 50% cpu and 60% memory.
- Using a custom docker image hosted on ECR called nodejs-test:latest.
- Includes how to login and pull an image from ECR.
- Exposes the app on port 3000 via a classic load balancer.
- Any changes to the deployment always ensures at least 7 replicas are running at all times.
- Has higher priority than other pods.

Assumptions:

- The ECR registry has an image called nodejs-test with the latest tag
- You have logged in to your ECR instance and have access to the docker config file.
- You have a clasic LoadBalancer set up with IP 40.71.21.26
