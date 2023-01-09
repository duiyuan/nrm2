> Fork [nrm](https://github.com/Pana/nrm) and rewrite all code with typescript, fixed some issues.

# nrm2 -- NPM registry manager

[![NPM version][npm-image]][npm-url]

`nrm2` can help you easy and fast switch between different npm registries,
now include: `npm`, `cnpm`, `taobao`, `nj(nodejitsu)`.

## How to configure yarn to use private registry ?

just add .yarnrc in your project’s directory and write there:
`registry “http://your.registry”`

Or you can configure it in your HOME directory's .yarnrc

## Install

```
$ npm install -g nrm2
```

## Example

```
$ nrm2 ls  // or nrm2 list

* npm ---------- https://registry.npmjs.org/
  yarn --------- https://registry.yarnpkg.com/
  tencent ------ https://mirrors.cloud.tencent.com/npm/
  cnpm --------- https://r.cnpmjs.org/
  taobao ------- https://registry.npmmirror.com/
  npmMirror ---- https://skimdb.npmjs.com/registry/

```

```
$ nrm2 use cnpm  //switch registry to cnpm

    Registry has been set to: http://r.cnpmjs.org/

```

## Usage

```
Usage: nrm2 [options] [command]

  Commands:

    ls|list                               List all the registries
    current                               Show current registry name
    use <registry>                        Change registry to registry
    add <registry> <url> [home]           Add one custom registry
    login <registry> [value]              Set authorize information for a registry with a base64 encoded string or username and pasword
      -a  --always-auth                     Set is always auth
      -u  --username <username>             Your user name for this registry
      -p  --password <password>             Your password for this registry
      -e  --email <email>                   Your email for this registry
    set-hosted-repo <registry> <value>    Set hosted npm repository for a custom registry to publish packages
    set-scope <scopeName> <value>         Associating a scope with a registry
    del-scope <scopeName>                 Remove a scope
    set <registryName>                    Set custom registry attribute
      -a  --attr <attr>                    Set custorm registry attribute
      -v  --value <value>                  Set custorm registry value
    del <registry>                        Delete one custom registry
    rename <registryName> <newName>       Set custom registry name
    home <registry> [browser]             Open the homepage of registry with optional browser
    publish [<tarball>|<folder>]          Publish package to current registry if current registry is a custom registry. The field 'repository' of current custom registry is required running this command. If you're not using custom registry, this command will run npm publish directly
      -t  --tag [tag]                        Add tag
      -a  --access <public|restricted>       Set access
      -o  --otp [otpcode]                    Set otpcode
      -dr --dry-run                          Set is dry run
    test [registry]                       Show the response time for one or all registries
    help                                  Print this help

  Options:

    -h  --help     output usage information
    -V  --version  output the version number
```

## Registries

- [npm](https://www.npmjs.org)
- [yarn](https://yarnpkg.com)
- [cnpm](http://cnpmjs.org)
- [nodejitsu](https://www.nodejitsu.com)
- [taobao](http://npm.taobao.org/)
