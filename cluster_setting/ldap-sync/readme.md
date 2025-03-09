[root@rhel9 ldap-sync]# oc create secret generic ldap-secret --from-literal=bindPassword=${BIND_PASSWORD}

secret/ldap-secret created

[root@rhel9 ocp4_post]# oc create configmap ldap-ca --from-file=ca.crt=/root/ocp4_post/rootCA.pem
configmap/ldap-ca created


[root@rhel9 ldap-sync]# oc adm policy add-cluster-role-to-group cluster-admin OCP-Admins

clusterrole.rbac.authorization.k8s.io/cluster-admin added: "OCP-Admins"

oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n ldap-sync

oc adm policy add-cluster-role-to-group cluster-admin OCP-Admins

oc delete secrets kubeadmin -n kube-system

