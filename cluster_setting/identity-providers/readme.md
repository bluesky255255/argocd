# Double check secret value if it is expected.

oc create secret generic ldap-bind-password --from-literal=bindPassword=${BIND_PASSWORD} -n openshift-config

oc create configmap ldap-ca-cert --from-file=ca.crt=rootCA.pem -n openshift-config
