### Install CSI
##### vSphere 7.0 U1
```
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0u1/rbac/vsphere-csi-controller-rbac.yaml
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0u1/deploy/vsphere-csi-node-ds.yaml
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0u1/deploy/vsphere-csi-controller-deployment.yaml
```

##### vSphere 7.0 U1
```
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0/rbac/vsphere-csi-controller-rbac.yaml
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0/deploy/vsphere-csi-node-ds.yaml
oc apply -f https://raw.githubusercontent.com/kubernetes-sigs/vsphere-csi-driver/master/manifests/v2.1.0/vsphere-7.0/deploy/vsphere-csi-controller-deployment.yaml
```

##### Verify CSI
```
kubectl get deployment --namespace=kube-system
kubectl get daemonsets vsphere-csi-node --namespace=kube-system
kubectl describe csidrivers
kubectl get CSINode
```