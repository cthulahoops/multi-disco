Example for running multiple Disco projects from a single GitHub repo.

Setup (without all the mistakes along the way):

```
$ disco projects:add --name disco-multi-client --github cthulahoops/multi-disco --domain multi-disco-client.dco.cthulahoops.org
$ disco env:set DISCO_JSON_PATH=disco.client.json --project disco-multi-client
$ disco projects:add --name disco-multi-flask --github cthulahoops/multi-disco --domain multi-disco-flask.dco.cthulahoops.org
$ disco env:set DISCO_JSON_PATH=disco.flask.json --project disco-multi-flask
$ curl https://multi-disco-client.dco.cthulahoops.org/
Hello, Disco
$ curl https://multi-disco-flask.dco.cthulahoops.org/
hello from disco!!! the datetime is 2025-10-02 16:39:15.190643
```
