# Mocaccino Repository index

This repository it is automatically built and contains the mocaccino repository index (built with luet).

You can also build this repo locally if you wish:
```sh
$ make deps
$ LUET=$GOPATH/bin/luet make build-all create-repo
```
To consume this repository with Luet, run:

```
sudo luet install repository/mocaccino-community
