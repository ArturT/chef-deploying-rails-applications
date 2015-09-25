# Tips

Create a new project:

    $ bundle exec knife solo init rdr_redis_example

Create a new vagrant machine:

    $ vagrant init ubuntu/trusty64
    $ vagrant up

User `private_network` option in `Vagrantfile`.


Add public key to root user:

    $ vagrant ssh
    $ sudo su
    $ cd && cd .ssh

    # add here your public key
    $ vim authorized_keys

    # now you can log in without password
    $ ssh root@192.168.33.10

Prepare machine:

    $ bundle exec knife solo prepare root@192.168.33.10

It generated file: `nodes/192.168.33.10.json`

## Create cookbook

    $ bundle exec knife cookbook create redis-server -o site-cookbooks

## Update node configuration

    $ bundle exec knife solo cook root@192.168.33.10
