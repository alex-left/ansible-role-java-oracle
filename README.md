Role Name
=========

Install oracle java directly from oracle website without third's repositories (webupd usually) in debian / ubuntu systems

Requirements
------------
NA

Role Variables
--------------


In ./defauts

(example)
~~~
java:
  download_url: http://download.oracle.com/otn-pub/java/jdk/8u112-b15/server-jre-8u112-linux-x64.tar.gz
  download_path: /tmp/java.tgz
  install_path: /opt/java
  version_path: jdk1.8.0_112
  default: true
~~~

Dependencies
------------

NA


License
-------

MIT

Author Information
------------------

Alex Left
