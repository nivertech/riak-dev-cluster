# Riak Dev Cluster for OS X

Easily run a 3-node [Riak](http://wiki.basho.com/Riak.html) cluster on OS X.

* The names of the nodes are riak[1-3]@127.0.0.1
* The HTTP port of riak1 is 11098: <http://127.0.0.1:11098>
* Riak Control (Admin UI) is available here: <https://admin:admin@127.0.0.1:11088/admin> (User: admin, Password: admin)
* All nodes use the [eleveldb](http://wiki.basho.com/LevelDB.html) storage backend
  to support [secondary indexes](http://wiki.basho.com/Secondary-Indexes.html)
* Please see riak[1-3]/etc/app.config for the other ports and settings

## Getting started

There is a bootstrap script available that installs, starts and joins the riak cluster in one go:

    $ rake bootstrap

## Control commands

Start all nodes:

    $ rake start

Join all nodes as a cluster (only needed once):

    $ rake join

Stop all nodes:

    $ rake stop

Clear all data and restart the cluster:

    $ rake clear

## Other commands

See all available commands:

    $ rake -T

## Note

Depending on your erlang cookie, you may have to use the commands with `sudo`.

## Authors

* [Erick Dennis](https://github.com/edennis)
* [Sebastian Röbke](https://github.com/boosty)
