# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Upload project files to a server

This action uploads new files to a server using Rsync

## Usage example

```yaml
      - name: Upload App files
        uses: juzt-studio/juzt-github-actions/rsync-files@master
        with:
          server-host: ${{ secrets.PRODUCTION_SSH_HOST }}
          server-port: ${{ secrets.PRODUCTION_SSH_PORT }}
          server-user: ${{ secrets.PRODUCTION_SSH_USER }}
          project-dir: ${{ vars.REMOTE_PATH }}
          project-folder: ${{ env.app_folder }}
```

## Parameters

---

### Server Host

Server HOST for SSH connect

**Required:** true

**Default:** ---

---

### Server User

Server USERNAME for SSH connect

**Required:** true

**Default:** ---

---

### Server Port

Server PORT number for SSH connect

**Required:** false

**Default:** 22

---

### Project Directory

Project location directory started from root

**Required:** true

**Default:** ---

---

### Project Folder Name

Project root folder name

**Required:** true

**Default:** ---

---

### Upload ignore file

Filename which contains list of files/dirs to ignore while copying

**Required:** false

**Default:** .rsyncignore

---

### Upload source folder

Path which contains source files to copy (in an action container)

**Required:** false

**Default:** .
