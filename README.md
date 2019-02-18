# kubernetes
Repository that demonstrates work on kubernetes

# dashboard (Bearer token generation to use in the Dashboard for login)
- Contains a template that can be used to create a new user via service account mechanism of k8s.
- User will be granted with admin permissions.
- Dashboard can be used to login using Bearer token tied to the user.

## commands
- Apply the template to the k8 cluster
  - kubectl apply -f dashboard/dashboard.yml
- Following could be used to get the token tied to the user
  - kubectl describe secrets shashi-user-token-x4vkt --namespace=kube-system
- Use token in the Web UI for dashboard to login
