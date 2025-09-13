apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: applications
spec:
  destination:
    namespace: namespace1
    server: https://kubernetes.default.svc
  source:
    path: applications
    repoURL: https://github.com/bluesky255255/argocd
    targetRevision: HEAD
  sources: []
  project: default
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
    syncOptions: []

<img width="1523" height="706" alt="image" src="https://github.com/user-attachments/assets/00a85e08-070c-4626-983d-bc79e9764711" />
