# K8s Debugging Notes

Quick reference for common troubleshooting.

## Pod issues

- `kubectl describe pod <name>` - show events
- `kubectl logs <name> --previous` - logs from previous container
- `kubectl exec -it <name> -- sh` - shell into container

## Node issues

- `kubectl get nodes -o wide`
- `kubectl describe node <node>`

## Networking

- `kubectl run tmp --rm -it --image=nicolaka/netshoot -- /bin/bash`
- `kubectl port-forward svc/<svc> 8080:80`

## Contexts

- `kubectl config get-contexts`
- `kubectl config use-context <context>`
