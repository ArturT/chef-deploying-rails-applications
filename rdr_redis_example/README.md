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
