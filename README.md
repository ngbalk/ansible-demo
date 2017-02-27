# ACE Ansible Demo

###### 1) Get on Red Hat VPN

###### 2) Configure your inventory

Add your server's ip address to your inventory file.  One of the following will be assigned to you:

1)	10.3.11.63
2)	10.3.11.82
3)	10.3.9.111
4)	10.3.11.58
5)	10.3.10.56
6)	10.3.11.85
7)	10.3.11.79
8)	10.3.11.84
9)	10.3.11.76
10)	10.3.11.70

###### 3) Run your playbook

```sh
ansible-playbook --private-key id_rsa -i inventory http-server-fedora.yml
```

Verify your HTTP server is running by typing your server's IP address in a browser address bar and hitting ENTER.
You should see some default page displayed.

###### Practice 

Improve the playbook to display custom content.  You must create a file called index.html in /var/www/html/  Use Ansible to both create and add content to that file.

###### Bonus

Configure HTTP server to listen on 8080 instead of 80 (default). 

