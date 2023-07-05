# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Set workflow timezone

This action will set a timezone for the workflow. 

By default, it will set **Europe/Moscow** timezone (Linux), but you can provide any on your wish.

This action depends on [szenius/set-timezone](https://github.com/szenius/set-timezone). In general, it's a wrapper over this action which provides default value.

## Usage example

```yaml
  - name: Init date/time
    uses: juzt-studio/juzt-github-actions/init-timezone@master
    with:
      timezone: 'Asia/Seoul' # Optional
```

## Parameters

### Time zone

A timezone what you want to use in a workflow. Full list you can [chech here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) in TZ identifier column

**Required:** false  

**Default:** Europe/Moscow

**Usage:**

```yaml
timezone: 'Europe/Lisbon'
# or 
timezone: 'Asia/Seoul'
# or
timezone: 'Pacific/Galapagos'
```
