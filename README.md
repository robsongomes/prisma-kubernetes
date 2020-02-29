# Deploying

Deploying the project is easy with kustomize. The **postgres/kustomization.yml** defines the sequence of applying resources. Use the command below under the postgres directory to deploy Prisma and Postgres.

`$ kubectl apply -k .`

If you prefer, you can apply each file individually:

`$ kubectl apply -f postgres-configmap.yml`

# Acessing

After deploying the project, kubernetes will expose two services:

- postgres on ports:
  - 30432 (external)
  - 5432 (internal)
- prisma on ports:
  - 30466 (external)
  - 4466 (internal)
