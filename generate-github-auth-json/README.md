# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Generate GitHub auth file

This action will generate json file for github auth. 

## Usage example

```yaml
  - name: Generate auth.json file
    uses: juzt-studio/juzt-github-actions/generate-github-auth-json@master
    with:
      access-token: ${{ secrets.JUZT_PLUGIN_ACCESS_TOKEN }}
      file-path: .config/composer # optional
      file-name: auth.json        # optional
```

## Parameters



### GitHub Personal Access Token 

Owner of the token should have access to the repo with plugin

**Required:** true  

**Default:** ---

---

### File location path

Where file will be generated

**Required:** false

**Default:** .config/composer

---

### File name

What filename will be applied 

**Required:** false

**Default:** auth.json

