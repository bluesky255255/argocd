After install openshift-gitops, default rbac have group cluster-admins have admin role.
To test argocd

oc adm groups new cluster-admins
group.user.openshift.io/cluster-admins created
<img width="429" height="50" alt="image" src="https://github.com/user-attachments/assets/319674bb-f70c-406b-b9ff-24138d048f0a" />

oc adm groups add-users cluster-admins USER

<img width="538" height="47" alt="image" src="https://github.com/user-attachments/assets/8177b403-ea79-4249-a6b9-99cd3e2ff4f6" />

group.user.openshift.io/cluster-admins added: USER

After login, it should have right to create application
<img width="816" height="262" alt="image" src="https://github.com/user-attachments/assets/29ca9951-0caf-4a19-a414-43adcbbe03a6" />
