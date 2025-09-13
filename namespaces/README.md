

apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: namespaces
spec:
  destination:
    namespace: ''
    server: https://kubernetes.default.svc
  source:
    path: namespaces
    repoURL: https://github.com/bluesky255255/argocd
    targetRevision: HEAD
  sources: []
  project: default

<img width="1154" height="884" alt="image" src="https://github.com/user-attachments/assets/e03ded78-50b0-4b33-a23a-acaa19eefe30" />
