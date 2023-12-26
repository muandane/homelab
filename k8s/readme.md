# Bootstraping a K8s node on a machine

## Installing k3s on a machine

To install k3s on a machine, follow these steps:

1. Download the k3s installer script that also installs directly and sets up a k3s node on your target machine:

```sh
curl -sfL https://get.k3s.io | sh -
```

2. Verify that k3s is running:

```sh
sudo k3s kubectl get nodes
```

> [!NOTE]
> You can pass K3S_KUBECONFIG_MODE="644" variable to the install script to be able to use kubectl commands without sudo access.
> `curl -sfL https://get.k3s.io | K3S_KUBECONFIG_MODE="644" sh -`

This will install a lightweight Kubernetes distribution `k3s` on the machine.
