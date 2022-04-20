Kubernetes CKA Commands & Notes
===============================

- ### List Pod with specific labels: 
  `kubectl get pods --selector="ver=2"`

- ### Labels can also be applied (or updated) on objects after they are created: 
    `kubectl label deployments alpaca-test "canary=true"`

- ### You can also use the -L option to kubectl get to show a label value as a column: 
    `kubectl get deployments -L canary`

- ### You can remove a label by applying a dash suffix: 
    `kubectl label deployments alpaca-test "canary-"`