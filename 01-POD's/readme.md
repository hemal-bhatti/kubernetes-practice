- by imprerative way to create a pod.

kubectl run nginx-pod --image=nginx:latest




kubectl run nginx-pod --image=nginx:latest --dry-run=client -o yaml > newPod.yaml



# get labels of pods 
kubectl get pods --show-labels
