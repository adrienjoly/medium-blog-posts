---
title: Thanks for this article!
date: '2018-09-15T12:25:42.631Z'
excerpt: 'FYI, here’s what I had to run to completely upgrade my mongodb service:'
layout: post
---
Thanks for this article! It helped my upgrade from Mongodb 3.2 to 3.4.17 on my Ubuntu 16.04 DigitalOcean instance.

FYI, here’s what I had to run to completely upgrade my mongodb service:

*   `$ apt-get install mongodb-org=3.4.17`
*   `$ mongod -v` => still 3.2...

    $ dpkg -l | grep mongo  
    ii  mongodb-org                       3.4.17                                     amd64        MongoDB open source document-oriented database system (metapackage)  
    ii  mongodb-org-mongos                3.2.19                                     amd64        MongoDB sharded cluster query router  
    ii  mongodb-org-server                3.2.19                                     amd64        MongoDB database server  
    ii  mongodb-org-shell                 3.2.19                                     amd64        MongoDB shell client  
    ii  mongodb-org-tools                 3.2.19                                     amd64        MongoDB tools
    $ sudo apt-get install mongodb-org-tools=3.4.17  
      
    $ sudo apt-get install mongodb-org-shell=3.4.17  
      
    $ sudo apt-get install mongodb-org-server=3.4.17  
      
    $ sudo apt-get install mongodb-org-mongos=3.4.17  
      
    $ dpkg -l | grep mongo  
    ii  mongodb-org                       3.4.17                                     amd64        MongoDB open source document-oriented database system (metapackage)  
    ii  mongodb-org-mongos                3.4.17                                     amd64        MongoDB sharded cluster query router  
    ii  mongodb-org-server                3.4.17                                     amd64        MongoDB database server  
    ii  mongodb-org-shell                 3.4.17                                     amd64        MongoDB shell client  
    ii  mongodb-org-tools                 3.4.17                                     amd64        MongoDB tools  
      
    $ mongod -v  
    2018-09-15T12:17:05.803+0000 I CONTROL  [initandlisten] db version v3.4.17  
      
    $ sudo service mongodb restart

More info: [https://github.com/openwhyd/openwhyd/issues/162#issuecomment-421559639](https://github.com/openwhyd/openwhyd/issues/162#issuecomment-421559639)
