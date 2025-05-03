# add-ssl-cert-to-agw-from-keyvault
here is az cli command for add certificate into application gateway.

resourceGroup='resource_group_name'
agwName='appgw_name'
certName='example_com'
kvSecretId='https://kv-xxxx-cert-sea.vault.azure.net/secrets/xxxxxx'

az network application-gateway ssl-cert create \
  --resource-group $resourceGroup \
  --gateway-name $agwName \
  -n $certName \
  --key-vault-secret-id $kvSecretId
