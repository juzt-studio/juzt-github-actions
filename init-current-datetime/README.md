# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Init current date/time variables

This action will set date and time variables to env, which can be used in the workflow 

## Usage example

```yaml
  - name: Init date/time
    uses: juzt-studio/juzt-github-actions/init-current-datetime@master
```

## Output

This action will set 3 variables to the env, which can be used like this:

```yaml
  - name: Example of usage
    run: |
      echo "${{ env.CURRENT_TIME }}"      # format: H-M
      echo "${{ env.CURRENT_DATE }}"      # format: Y-m-d
      echo "${{ env.CURRENT_DATETIME }}"  # format: Y-m-d_H-M
```
