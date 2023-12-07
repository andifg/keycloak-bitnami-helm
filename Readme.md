# Keycloak test


1. Activate OCI

```bash
export HELM_EXPERIMENTAL_OCI=1
```

2. Install chart

Edit values inside `values.yaml`

```bash
helm install keycloak oci://registry-1.docker.io/bitnamicharts/keycloak --version 17.3.5 -f values.yaml
```

3. Create config map to be used to import realm

```bash
oc apply -f configmap.yaml
```

