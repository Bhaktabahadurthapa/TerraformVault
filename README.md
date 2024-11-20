# TerraformVault

Secret managemnt in Terraform via Vault Integration: first Create an AWS EC2 instance with Ubuntu machine,
and following steps to be execute Install Vault on the EC2 instance

[Documentation ](https://developer.hashicorp.com/vault/tutorials/getting-started/getting-started-install)

**Update the package manager and install GPG and wget**
```
sudo apt update && sudo apt install gpg wget
```
**Download the signing key to a new keyring**
```
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
**Verify the keyring**
```
gpg --no-default-keyring --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg --fingerprint
```

**Add the HashiCorp repository.**

```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

```
**Finally, Install Vault**
```
sudo apt update && sudo apt install vault

```
**Start Vault.**
To start Vault, you can use the following command:

```
vault server -dev -dev-listen-address="0.0.0.0:8200"
```
**Run the Public_ip:8200 port ** to access the vault, you can see dashboard

<img width="1539" alt="image" src="https://github.com/user-attachments/assets/3066a18e-74ea-4ccc-9518-d20b3bc0920a">


<img width="1451" alt="image" src="https://github.com/user-attachments/assets/7962d2fa-f246-4c5c-a708-926ba748005c">

