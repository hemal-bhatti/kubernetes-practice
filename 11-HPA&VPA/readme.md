Autoscalling 

HPA => Horizontal Pod Autoscalling  (If mission critical than we have to use)
VPA => Vartical Pod Autoscalling  (Simple work load or if application can affored some down-time)
VPA will replace with 1CPU pod to 10CPU pod and it will need to restart... (stateless nature)


only HPA comes with kubernetes..

outher will we have configure and use some cloud provider like aws and etc... 


==> we need matrix server for that.. we have to expose the matric to hpa and based on that we have to scalling pods...

HPA keeps monitoring our resource every 50 sec (default) 

====> autoscalling by command 

kubectl get hpa
kubectl autoscale deploy <deployment-name> --cpu-percent=50 --min=1 --max=3