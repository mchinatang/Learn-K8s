### 创建 Deployment
```shell
$ kubectl apply -f merlink8s-deployment.yaml
```

### 获取 Deployment 信息
```shell
$ kubectl get deployments
NAME                   READY   UP-TO-DATE   AVAILABLE   AGE
merlink8s-deployment   3/3     3            3           9m57s
```

### 获取 RS(ReplicaSet) 信息
```shell
$ kubectl get rs
NAME                              DESIRED   CURRENT   READY   AGE
merlink8s-deployment-57f8bfb5bb   3         3         3       12m
```

### 获取 Pods 信息
```shell
$ kubectl get pods --show-labels
NAME                                    READY   STATUS    RESTARTS   AGE   LABELS
merlink8s-deployment-57f8bfb5bb-8sxmp   1/1     Running   0          14m   app=merlink8s-deployment-nginx,pod-template-hash=57f8bfb5bb
merlink8s-deployment-57f8bfb5bb-t6snf   1/1     Running   0          14m   app=merlink8s-deployment-nginx,pod-template-hash=57f8bfb5bb
merlink8s-deployment-57f8bfb5bb-tt52p   1/1     Running   0          14m   app=merlink8s-deployment-nginx,pod-template-hash=57f8bfb5bb
```