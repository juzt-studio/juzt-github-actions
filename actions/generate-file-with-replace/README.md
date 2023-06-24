# Juzt Studio: Reusable GitHub actions

[← GO BACK](../README.md)

## Generate file with replacement

This action will take a file as a template, copy it to a new file and make content replacement. 

This can be very useful in case of generating:

 - .env files
 - Service confirmation files (Google, Yandex, Mailru, etc.) 
 - Robots.txt
 - etc.

## Usage example

```yaml
  - name: Generate .env file
    uses: juzt-studio/juzt-github-actions/actions/generate-file-with-replace@master
    with:
      file-source: .env.example # optional
      file-target: .env         # optional
      variables: |
        VAR_FOR_REPLACEMENT_1=${{ secrets.SOME_VALUE }}
        VAR_FOR_REPLACEMENT_2=Juzt Studio
        VAR_FOR_REPLACEMENT_3=123456789
        # You may add as much variables as you need
```

## Parameters



### Source File 

Template file which will be used for making a copy.

**Required:** false  

**Default:** .env.example 

**Usage:** 

```yaml
file-source: .env.example
#or 
file-source: src/templates/file.txt
```

This file can contain replacement marks which will be replaced by variables values. **Important** replacement marks should be the same as variable name and wrapped in double brases:

```dotenv
SITE_API_URL={{VAR_FOR_REPLACEMENT_1}}
COMPANY_NAME={{VAR_FOR_REPLACEMENT_2}}
COMPANY_PHONE={{VAR_FOR_REPLACEMENT_3}}

# Replacement marks can have duplicates they all will be replaced
COPYRIGHT_BY={{VAR_FOR_REPLACEMENT_2}}
```


### Target File

The name of result file and where it should be placed after generating.

**Required:** false

**Default:** .env

**Usage:**

```yaml
file-target: .env
#or 
file-target: build/file-generated.config
```



### Variables

List of variables for replacement. 

**Required:** true

**Default:** .env.example

**Usage:**

```yaml
variables: |
    VAR_FOR_REPLACEMENT_1=${{ secrets.SOME_VALUE }}
    VAR_FOR_REPLACEMENT_2=Juzt Studio
    VAR_FOR_REPLACEMENT_3=123456789
```

There is no limitations for the number of variables. But the names should fit the replacements marks (see above)


```
# This variable's value 
VAR_FOR_REPLACEMENT_1

# will replace this mark
{{VAR_FOR_REPLACEMENT_1}}
```
