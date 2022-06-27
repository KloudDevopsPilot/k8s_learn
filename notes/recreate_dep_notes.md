# Recreate Deployment Strategy

![recreate](../img/deployment/recreate.png)

## inside yaml file

```yaml

spec:
  replicas: 3
  strategy:
    type: Recreate
  template:
    ...
    ...

```

## Link to demo

* [`Demo`](../demos/recreate_dep_demo.md)