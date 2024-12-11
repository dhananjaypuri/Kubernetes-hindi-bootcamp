#### This is part 4 of the bootcamp

## another Sidecar container example 
https://github.com/thockin/kubectl-sidecar

## Pause container 
In Kubernetes when you launch a pod, there is also a pause container that gets spinned up. You can find the pauce.c file [here]()
ctr --namespace k8s.io containers list | grep pause


##PDB
Create deployment
Create pdb
Do rolling update

kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1
kubectl get pods -w

###DownwardAPI
kubectl apply -f downwardapipod.yaml


### QOS 
kubectl get pods nginx-guaranteed -oyaml | grep qos

## POD disruption

![image](https://github.com/user-attachments/assets/2405adcb-0882-466a-aaac-c6ae8245b5ca)

Pod disruptions can happen for various reasons, including:

# 1 . Planned Disruptions: 


  Node maintenance (e.g., upgrades, repairs)

  Scaling operations (adding or removing nodes)

# 2. Unplanned Disruptions:

  Node failures (hardware or software issues)

  Network partitions

  Evictions due to resource constraints
