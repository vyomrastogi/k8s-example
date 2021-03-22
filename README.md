# Kubernetes Definition Examples

All are tested on a single node cluster setup using microk8s

### Pods Examples 

- simple-pod-definition.yaml
  - Output sample : 

  ```
  microk8s kubectl get pods
  NAME                 READY   STATUS    RESTARTS   AGE
  nginx-loadbalancer   1/1     Running   0          73s
  ```

### Replication Controller Examples

- simple-rc-definition.yaml
  - Output sample :
  ```
   microk8s kubectl apply -f replicas/simple-rc-definition.yaml 
   replicationcontroller/nginx-rc created
  ```
  - To get all replication controllers
  ```
  microk8s kubectl get replicationcontroller
  NAME       DESIRED   CURRENT   READY   AGE
  nginx-rc   3         3         3       78s
  ```
  - Note : the name of pod is generated from name of replication controller
  ```
  microk8s kubectl get pods
  NAME             READY   STATUS    RESTARTS   AGE
  nginx-rc-lnmzv   1/1     Running   0          88s
  nginx-rc-5hrhj   1/1     Running   0          88s
  nginx-rc-f64vv   1/1     Running   0          88s
  ```