# Pod
## pod 示例
``` yaml
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
spec:
  containers:
  - name: myapp-container
    image: nginx:1.13.6
```
> 参考：https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/