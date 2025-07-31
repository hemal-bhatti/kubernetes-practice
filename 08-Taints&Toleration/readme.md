ref :- screeen shot for this..

Add taint :-
kubectl taint node <node-name> gpu=true:NoSchedule

check: kubectl node describe <node-name>

Remove taint :-
kubectl taint node <node-name> gpu=true:NoSchedule-


Taint & Toleration:-
 Just prevent or restrict un-wanted pod to schedulling that tainted node.It's Does not gauranty to that toleration's pod schedule on that node. it may schedule if taint match or may not schedule even if taint is matched. 


 so we use selector for that
    give label to pod and node, and match that label for schedulling..

    if we don't give label to node..

    NAME           READY   STATUS    RESTARTS   AGE
    selectr-pod    0/1     Pending   0          6s


    Add labels on node :-
    kubectl label node <node-name> gpu=false

    Remove labels from node :-
    kubectl label node <node-name> <label-key>-   ==> like if gpu=false than only gpu  
    kubectl label node cka-main-cluster45-worker2 gpu-    
