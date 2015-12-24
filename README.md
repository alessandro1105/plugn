# plugn [![Build Status](https://img.shields.io/circleci/project/dokku/plugn/master.svg?style=flat-square "Build Status")](https://circleci.com/gh/dokku/plugn/tree/master)

Hook system that lets users extend your application with plugins

## Installation
```
    wget -qO /tmp/plugn_latest.tgz https://github.com/dokku/plugn/releases/download/v0.1.0/plugn_0.1.0_linux_x86_64.tgz
    tar xzf /tmp/plugn_latest.tgz -C /usr/local/bin
```

## Usage
```
$ PLUGIN_PATH=/var/lib/dokku/plugins plugn

Available commands:
  config                       Plugin configuration
  disable                      Disable a plugin
  enable                       Enable a plugin
  help                         Shows help information for a command
  init                         Initialize an empty plugin path
  install                      Install a new plugin from a Git URL
  list                         List all local plugins
  source                       Source commands for sourcable plugins
  trigger                      Triggers hook in enabled plugins
  uninstall                    Remove plugin from available plugins
  update                       Update plugin and optionally pin to commit/tag/branch
```

## Building & Testing (in docker)
```
$ docker-machine create -d virtualbox plugn-dev
$ eval $(docker-machine env plugn-dev)
$ make build-in-docker
$ make test
```

## License

BSD
