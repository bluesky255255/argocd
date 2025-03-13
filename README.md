Test argocd
[root@rhel9 ~]# oc adm groups new cluster-admins
group.user.openshift.io/cluster-admins created
[root@rhel9 ~]# oc adm groups add-users cluster-admins kaicheng
group.user.openshift.io/cluster-admins added: "kaicheng"
