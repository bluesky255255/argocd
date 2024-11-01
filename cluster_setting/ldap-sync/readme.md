[root@rhel9 ldap-sync]# oc create secret generic ldap-secret --from-literal=bindPassword=${BIND_PASSWORD}
secret/ldap-secret created
[root@rhel9 ldap-sync]# oc create configmap ca-config-map --from-file=ca.crt=/root/ocp4_post/rootCA.pem
configmap/ca-config-map created

[root@rhel9 ldap-sync]# oc adm policy add-cluster-role-to-group cluster-admin OCP-Admins
clusterrole.rbac.authorization.k8s.io/cluster-admin added: "OCP-Admins"
