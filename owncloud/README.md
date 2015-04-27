[![logo](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b6/OwnCloud2-Logo.svg/595px-OwnCloud2-Logo.svg.png)](http://owncloud.org/)

# Kudos

This repo was copied from dperson/owncloud. Full kudos to him for this. I changed the Dockerfile just to add some extra volume. Some other changes may follow.

# ownCloud

ownCloud docker container

# What is ownCloud?

ownCloud is a software system for what is commonly termed "file hosting". As
such, ownCloud is very similar to the widely used Dropbox, with the primary
difference being that ownCloud is free and open-source, and thereby allowing
anyone to install and operate it without charge on a private server, with no
limits on storage space (except for hard disk capacity) or the number of
connected clients.

# How to use this image

This ownCloud container was built with Nginx. It defaults to SQLite for the DB,
but you can choose PostgreSQL or MySQL, for more performance.


    /usr/bin/docker run -d --name="ownCloud" --net="bridge" -e SUBJECT="/C=COUTRY/ST=STATE/L=CITY/O=ORGANIZATION/OU=UNIT/CN=myhome.com" -p 8000:8000/tcp -v "/path/to/your/owncloud/data":"/var/www/owncloud/data":rw -v "/etc/localtime":"/etc/localtime":ro gfjardim/owncloud

Change the SUBJECT variable to reflect your scenario.

