Kubernetes Request and Limits :-

Insufficient Resourses
OOM (Ont of Memory)


we need matric server file => this will expose matrix of our nodes (like cpu, Memory utilization, we need for HPA-VPA etc)


for getting nodes cpu&Memory utilization :-
    kubectl top nodes
    kubectl top pod <pod-name> -n <name-space>

====> getting from ref-out-memory.yml
    NAME              READY   STATUS      RESTARTS      AGE
    memory-request1   0/1     OOMKilled   2 (20s ago)   25s


===> in ref-out-memory-node.yml
    pod is going to in pending state => Insufficient Memory Resourses.
    pod need to 1000Gi for schedulling but node have not that much memory....