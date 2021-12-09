# vault-secrets helm chart

Deploys VaultSecrets from terraform.

## 1.18.0 - Add Templated Secrets

* Added the ability to use templates in vaultsecret.

## v1.17.0 - Initial Public Release

* Added `secretEngine` variable to allow GCP secrets.
* Added some quoting
* Set default name to .Release.Name
* Set default values to be convenient for our use
* Added `CHANGELOG` ;)
