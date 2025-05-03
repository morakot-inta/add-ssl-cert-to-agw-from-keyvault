# add-ssl-cert-to-agw-from-keyvault

This command is used to add an SSL certificate from keyvault to an application gateway.
It works both within the same subscription and across different subscriptions.

```sh
resourceGroup='resource_group_name'
agwName='appgw_name'
certName='example_com'
kvSecretId='https://kv-xxxx-cert-sea.vault.azure.net/secrets/xxxxxx'

az network application-gateway ssl-cert create \
  --resource-group $resourceGroup \
  --gateway-name $agwName \
  -n $certName \
  --key-vault-secret-id $kvSecretId
```
