# Pod Workshop

## nginx-pod.yaml

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
  labels:
    app: nginx
    tier: dev
spec:
  containers:
    - name: nginx-container
      image: nginx:1.18
```

## Deploy Pods
>
    kubectl apply -f <FILENAME.YAML>

## Display Pods
>
    kubectl get pods
    kubectl get pods -o wide  # Print wide output of the Pod

    kubectl get pods -n <NAME-SPACE>     # Print Pods in particular NameSpace
    kubectl get pods -A                  # Print Pods in all namespace

    kubectl get pods <POD-NAME>
    kubectl get pods <POD-NAME> -o yaml  
    kubectl get pods <POD-NAME> -o json

    kubectl get pods --show-labels
    kubectl get pods -l app=nginx        # Print Pods with particular label

## Print Details of Pod
>
    kubectl describe pods <POD-NAME>

## Editing Pod which is running
>
    kubectl edit pods <POD-NAME>
    kubectl describe pods nginx-pod | grep Image

## Print Pod Logs
>
    kubectl logs <POD-NAME>
    kubectl logs <POD-NAME> -n <NAME-SPACE>

## Running operations directly on the YAML file
>
    SYNTAX: kubectl [OPERATION] –f [FILE-NAME.yaml]

    kubectl get –f [FILE-NAME.yaml]
    kubectl describe –f [FILE-NAME.yaml]
    kubectl edit –f [FILE-NAME.yaml]
    kubectl delete –f [FILE-NAME.yaml]
    kubectl apply –f [FILE-NAME.yaml]

## Deleting Pod
>
    kubectl delete pods <POD-NAME>