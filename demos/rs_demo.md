# Pod Workshop

## nginx-rs.yaml

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: nginx-rs
  labels:
    app: guestbook
    tier: frontend
spec:
  replicas: 3
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: nginx
        image: nginx
```

## Deploy ReplicaSet
>
  kubectl apply -f <FILENAME.YAML>

## Display ReplicaSet (rs)
>
  kubectl get rs
  kubectl get rs <RS-NAME> -o wide
  kubectl get rs <RS-NAME> -o yaml
  kubectl get rs -l <LABEL>

## Displaying Pods
>
  kubectl get pods
  kubectl get pods -l <LABEL>

## Print Details of ReplicaSet
>
  kubectl describe rs <RS-NAME>

## Print Details of ReplicaSet
>
  kubectl scale rs <RS-NAME> --replicas=[COUNT]

## Editing ReplicaSet
>
  kubectl edit rs <RS-NAME>

## Running operations directly on the YAML file
>
  kSYNTAX: kubectl [OPERATION] –f [FILE-NAME.yaml]

  kubectl get –f [FILE-NAME.yaml]
  kubectl describe –f [FILE-NAME.yaml]
  kubectl edit –f [FILE-NAME.yaml]
  kubectl delete –f [FILE-NAME.yaml]
  kubectl create –f [FILE-NAME.yaml]

## Deleting ReplicaSet
>
  kubectl delete rs <RS-NAME>
