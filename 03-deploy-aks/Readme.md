# Manage und update kubernetes cluster

## Setup environment
Zum Verwalten des kubernetes clusters wird `kubectl` verwendet.

Falls nicht vorhanden, kann dieses mit folgenden Befehlen runtergeladen und konfiguriert werden

```
# install kubectl
az aks install-cli

# configure login
az aks get-credentials --resource-group <rg-name> --name <aks-name>

# test 
kubectl get nodes
```