# Mocaccino Repository index

This repository it is automatically built and contains the mocaccino repository index (built with luet).

You can also build this repo locally if you wish:
```sh
$ make deps
$ curl -LO https://storage.googleapis.com/container-diff/latest/container-diff-linux-amd64 && chmod +x container-diff-linux-amd64 && sudo mv container-diff-linux-amd64 /usr/local/bin/container-diff
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
  - "https://mocaccino.keybase.pub/repository-index"
```