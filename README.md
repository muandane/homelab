# Homelab

configuration files and documentation for my homelab setup. The homelab consists of:

- A Raspberry Pi running Docker and Kubernetes
- A server also running Docker and Kubernetes
- Services deployed via Docker Compose, including:
  - Pihole for network-wide ad blocking

## Raspberry Pi

The Raspberry Pi acts as a Kubernetes master node and runs the following:

- Docker
- Kubernetes
- Portainer for container management

Services are deployed to the Pi via Docker Compose.

### Server

The server acts as a Kubernetes worker node. It runs:

- Docker
- Kubernetes kubelet

The server connects to the Pi as its Kubernetes master.

### Docker Compose

The docker-compose directory contains Docker Compose files to deploy services. This includes:

- Pihole - Network-wide ad blocking via DNS

### Kubernetes

Kubernetes provides orchestration and management of containers across the Pi and server.

- The Pi acts as the control plane and master node. The server joins as a worker node.

### Monitoring

Monitoring of containers and infrastructure is done via:

- Portainer on the Pi
- Kubernetes Dashboard

This provides visibility into the overall health of the homelab environment.
