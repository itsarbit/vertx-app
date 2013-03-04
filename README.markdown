Vert.x Application Charm
==


juju charm to deploy a user-defined vert.x application
--

This is a [juju](http://https://juju.ubuntu.com) charm to deploy a user defined
vert.x app directly from your development machine.


Get Vert.x Charm
--

You can get it with:

~~
$ mkdir -p ~/charms/precise
$ cd ~/charms/precise
$ git clone  dali:/CharmVertxApp.git  ~/charms/precise/vertx-app
$ cd vertx-app
~~


Vert.x deploy
--

1. Copy your private key for accessing your git server into the charm directoy:
**Warning: Please make sure that the private key does not have passphrase**

		$ cp ~/.ssh/your_dali_private_key ~/charms/precise/vertx-app/

2. Edit __{myapp}.yaml__ referring to __config.yaml__ (For example:
   vertx-test.yaml)

3. Deploy it with:

		$ juju deploy --config __{myapp}.yaml__ --repository charms local:precise/vertx-app {myapp}


Application Expose
--

~~
$ juju expose {myapp}
~~

