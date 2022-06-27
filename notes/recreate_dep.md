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