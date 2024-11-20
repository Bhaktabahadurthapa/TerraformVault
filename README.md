# TerraformVault

Secret managemnt in Terraform via Vault Integration: first Create an AWS EC2 instance with Ubuntu machine,
and following steps to be execute Install Vault on the EC2 instance

[Documentation ](https://developer.hashicorp.com/vault/tutorials/getting-started/getting-started-install)

**Update the package manager and install GPG and wget.
**
```
sudo apt update && sudo apt install gpg wget
```
**Download the signing key to a new keyring
**
```
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
