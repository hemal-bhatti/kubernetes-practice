Init container:
 It is a container which is run before root container or actual container run


SideCar container:
    run all the time with main containar and provide some input and take some output from main containe..
    also know as helper container



    1) run pod.yml first
     => check status of pod

            ```
            NAME             READY   STATUS     RESTARTS   AGE
            init-container   0/1     Init:0/1   0          31s
            ```


    2) run ref-deployment.yml
    3) run ref-svc.yml
     => again check status of pod again  



    check direct container's env variables :-
     kubectl exec -it pod/init-container -- printenv




      we have multiple init-container for different perpose like...
      => our requirement is create db pod and create database than running some other pods nd etc...