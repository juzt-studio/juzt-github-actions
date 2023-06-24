## Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

This actions can be used in any project. Simply add to your workflow cobe like below

```yml
  - name: Init date/time
    uses: juzt-studio/juzt-github-actions/<ACTION_FOLDER>@master
```

for detailed information check the exact action in list

## Shared actions

- [Initialize Timezone](./init-timezone/README.md)
- [Initialize variable with current date](./init-current-datetime/README.md)
- [Install SSH Private key](./install-ssh-key/README.md)
- [Generate file with replacement](./generate-file-with-replace/README.md)
- [Copy files to the server](./rsync-files/README.md)
