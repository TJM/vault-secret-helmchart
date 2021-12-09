# vault-secrets

Helm chart to create a VaultSecret

While using Terraform to manage all of our infrastructure, we needed the ability to create [VaultSecret](https://github.com/ricoberger/vault-secrets-operator) objects (CRD).

This solution is being used internally with success, but there is no support! ;)

Please feel free to submit Pull Requests with suggestions for improvement.

## Install

* `helm repo add vault-secrets-helmchart https://tjm.github.io/vault-secrets-helmchart/`
* `helm upgrade --install vault-secrets-helmchart/vault-secret`

## Terraform

The actual use for this helm chart would be terraform, so here is a terraform example:

```hcl
resource "helm_release" "my_vault_secret" {
  name      = "my_vault_secret"
  namespace = "my_namespace"
  repo      = "https://tjm.github.io/vault-secrets-helmchart/"
  chart     = "vault-secret"
  set {
    name  = "vaultSecret.path"
    value = "secret/path/my_secret"
  }
}
```
