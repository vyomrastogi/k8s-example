# Kubernetes Definition Examples

All are tested on a single node cluster setup using microk8s

- simple-pod-definition.yaml
  - Output sample : 

  ```
  microk8s kubectl get pods
  NAME                 READY   STATUS    RESTARTS   AGE
  nginx-loadbalancer   1/1     Running   0          73s
  ```