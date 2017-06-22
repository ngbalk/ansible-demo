# ACE Ansible Demo

###### 1) Configure your inventory

Add your server's ip address to your inventory file (this file is called 'inventory').  One of the following will be assigned to you:


1.	104.196.177.189 
2.	35.190.129.186 	
3.	35.185.33.24 	
4.	35.185.50.211 	
5.	104.196.24.249 	
6.	35.190.151.175

Your inventory file should like like this, respectively:
```
[localhost]
127.0.0.1

[main-server]
10.3.8.69
```

NOTE: When writing Ansible code, formatting is VERY important (remember, Ansible is written in YAML format).  I always use Sublime or Atom, but vim or vi is good too if you're comfortable with it.

###### 2) Run your playbook

```sh
ansible-playbook --private-key id_rsa -i inventory http-server-fedora.yml
```

Verify your HTTP server is running by typing your server's IP address in a browser address bar and hitting ENTER.
You should see some default page displayed.

###### Practice 

Improve the playbook to configure the http server to display custom content.  You must create a file called index.html in /var/www/html/ on your remote server.  Add tasks to your ansible-playbook to create and add content to that file.  Its okay to use Google or the Ansible Documentation online.

###### Bonus

Configure HTTP server to listen on port 8080 instead of 80 (default). HINT: Apache httpd configuration is located in /etc/httpd/conf/httpd.conf
