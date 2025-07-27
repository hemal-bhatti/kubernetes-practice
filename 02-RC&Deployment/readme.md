# ReplicaController :-
```
=> Old we to do a replication in kubernetes
=> selector not supported.
```


# Replicaset :- 
```
=> New Way to Declare Replication in kubernetes
=> We have selector filed in which we can matchLabels to replilcate existing pods with same labels-name.

```



# For Scalling a pods :-
```
1) we have option of HPA & VPA  (Later we discuss)
2) we can manually apply change to .yml file and again apply it
3) we can also use kubectl edit rs/<replicationSet-Name>
4) use kubectl scale --replicas=4 rs/<replicationSetName> 
```



# Deployment :-

```
=> As a Devops Engnieer we create Deployment and then that deployment create a replica-set.

=> It will provide some additional functionality => version Example  V1.1 => V1.2
(1) roll-out 

```

# apply change in deployment by commands :-

```
=> kubectl set image deployment/nginx-deployment \          nginx-app<conainerName>=<ImageName> -n <namespace>
```  

# Check for Rollout history :-
```
=> kubectl rollout history deployment/nginx-deployment
```


# rollout undo (go to back version)
```
=>  kubectl rollout undo deployment/nginx-deployment
``` 