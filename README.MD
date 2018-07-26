# helm chart  example
 the example contains a directory structure to build a helm Chart，And how to apply template data in deployment，the deployment.yaml  contains template data the references values.yaml and Chart.yaml.
 You can visit my blog on how to use helm and Chart [kubernetes利器-helm](https://gitzl.github.io/2018/07/19/helm/)

## the content

```
 - deployment.yaml
 - service.yaml
 - Chart.yaml
 - values.yaml

```
## install the helm Chart example

```
cd helm
helm install .

# the install result log 

RESOURCES:
==> v1/Service
NAME      TYPE       CLUSTER-IP     EXTERNAL-IP  PORT(S)   AGE
jpt-test  ClusterIP  10.111.17.249  <none>       8080/TCP  0s

==> v1beta1/Deployment
NAME      DESIRED  CURRENT  UP-TO-DATE  AVAILABLE  AGE
jpt-test  1        1        1           0          0s

==> v1/Pod(related)
NAME                       READY  STATUS       RESTARTS  AGE
jpt-test-5bd49d546b-45dz8  0/1    Terminating  0         8d
jpt-test-5bd49d546b-75764  0/1    Pending      0         0s

```