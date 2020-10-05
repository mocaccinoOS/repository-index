# Mocaccino Repository index

This repository it is automatically built and contains the mocaccino repository index (built with luet).

You can also build this repo locally if you wish:
```sh
$ make deps
$ LUET=$GOPATH/bin/luet make build-all create-repo
```
To consume this repository with Luet, add in the `luet.yaml`:

```yaml
repositories:
- name: "mocaccino-repository-index"
  description: "MocaccinoOS Repository index"
  type: "http"
  enable: true
  cached: true
  priority: 1
  urls:
  - "https://raw.githubusercontent.com/mocaccinoOS/repository-index/gh-pages"
  - "https://get.mocaccino.org/mocaccino-repository-index"
```
