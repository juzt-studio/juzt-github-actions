# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Install SSH Private key

This action add a private key to the workflow, which can be used after for connections to a server via ssh.

## Usage example

```yaml
  - name: Init date/time
    uses: juzt-studio/juzt-github-actions/actions/install-ssh-key@master
    with:
      ssh-private-key: ${{ secrets.PRIVATE_SSH_KEY }}
```

## Parameters

### Private Key

This is the only but required parameter. You should provide PRIVATE key of keypair to store in a workflow. Usually you can use secrets from a GitHub, but you are free to provide a string.

**Required:** true

**Default:** ---

**Usage:**

```yaml
ssh-private-key: ${{ secrets.PRIVATE_SSH_KEY }}
# or 
ssh-private-key: ${{ vars.PRIVATE_SSH_KEY }}
# or
timezone: 'pass here a string'
```
