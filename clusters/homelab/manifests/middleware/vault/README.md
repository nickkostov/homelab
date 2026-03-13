## After installation steps:

These need to be executed, because we have to initialize and unseal vault.

export VAULT_ADDR=https://vault.range.local:443
export VAULT_SKIP_VERIFY=true

vault operator init

vault operator unseal