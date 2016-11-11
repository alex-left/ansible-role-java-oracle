Role Name
=========

Install oracle java directly from oracle website without third's repositories (webupd usually) in debian / ubuntu systems

Usage
------------
Install the role and modify the download url to desired version (also "version_path" variable) and others variables if you want. You can use the role as dependency after checks if java exists, for example:

		  pre_tasks:
	      - name: check if java is installed
	        command: java -version  
	        failed_when: false
	        register: check_java
	      roles:
	      - { role: java, when: check_java.rc != 0 }

Role Variables
--------------

All variables are stored in defaults. the more relevant are the download_url and version_path. The variable "default" use the command "update-alternatives" to make java the default jvm. 

(example)
~~~
java:
  download_url: "http://download.oracle.com/otn-pub/java/jdk/8u112-b15/server-jre-8u112-linux-x64.tar.gz"
  download_path: "/tmp/java.tgz"
  install_path: "/opt/java"
  version_path: "jdk1.8.0_112"
  default: true
~~~

Dependencies
------------

Ansible version => 2.2


License
-------

MIT

Author Information
------------------

Alex Left
