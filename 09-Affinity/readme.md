use for pods schedulling..

requiredDuringSchedulingIgnoredDuringExecution:
     if Labels is matching than only scheduling a pod.

preferredDuringSchedulingIgnoredDuringExecution:
    It is check for labels,, if labels is not matching than also schedulling a pod based on weight


    both are not impate on existing running pods it will only impate new created pods..



    --- 
    we also have Exists operator which is only need for -key,, it matches key and based on that it will schelluing a pod.


    ---
    we add affinity to a pod and it will check a node's label and it matches than it will schedulling a pod. 