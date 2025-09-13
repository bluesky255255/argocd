After install openshift-gitops
#oc edit argocd -n openshift-gitops

Ensure cluster-admins have admin role in argocd.
 80   rbac:
 81     defaultPolicy: ""
 82     policy: |
 83       g, system:cluster-admins, role:admin
 84       g, cluster-admins, role:admin


Test argocd

oc adm groups new cluster-admins
group.user.openshift.io/cluster-admins created

oc adm groups add-users cluster-admins USER
group.user.openshift.io/cluster-admins added: USER
