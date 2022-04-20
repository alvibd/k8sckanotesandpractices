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

- ### We can also ask if a label is one of a set of values:
    `kubectl get pods --selector="app in (alpaca,bandicoot)"`

- ### There are also “negative” versions of each of these

| Operator                  | Description                        |
| ------------------------- | ---------------------------------- |
| key=value                 | key is set to value                |
| key!=value                | key is not set to value            |
| key in (value1, value2)   | key is one of value1 or value2     |
| key notin (value1, value2)|  key is not one of value1 or value2|
| key                       | key is set                         |
| !key                      | key is not set                     |

- ### Similarly, you can combine positive and negative selectors together as follows:
    `kubectl get pods -l 'ver=2,!canary'`