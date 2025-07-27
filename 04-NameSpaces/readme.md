make isolation env. for our pods we use nameSpaces..

by imperative way to create namespace;
    kubectl create ns <nameSpace-name>



    => communication with test namespace's pod  with default namespace's pod...

    exec into test namespace pod. and curl defaultNP's pod ip than we get respone..


    => we can curl into pods within a different namespace but in case of service can cannot do that direct curl on servicename

    use /etc/resolve.conf inside pod. know as FQDN (fully qualify domain name)
    get <namespacename.svc.cluster.local>

    inside a pod
    curl service-name.<namespacename.svc.cluster.local>