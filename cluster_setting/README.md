
<img width="1182" height="902" alt="image" src="https://github.com/user-attachments/assets/290ad282-f762-4545-bcb6-4357ac7dc468" />

Reason of failed applied due to lack of permission.

cronjobs.batch is forbidden: User "system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller" cannot create resource "cronjobs" in API group "batch" in the namespace "ldap-sync"
serviceaccounts is forbidden: User "system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller" cannot create resource "serviceaccounts" in API group "" in the namespace "ldap-sync"

https://access.redhat.com/solutions/7007638
oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n ldap-sync

For ldap-sync, need to add the scrert of AD ldap user.
oc create secret generic ldap-bind-password --from-literal=bindPassword=${BIND_PASSWORD} -n ldap-sync

