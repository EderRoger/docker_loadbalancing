## Docker container with haproxy loadbalancing ##
Show one example with HAProxy container balancing other web applications

### Run it! ###

``$ vagrant up --provision``

### Test it! ###

``open web browser  http://10.0.0.115``

### HAProxy stats ! See our nodes ###

``open web browser http://10.0.0.115/haproxy?stats``

### Gerenate logs with apache benchmark ###

``$ ab -c 40 -n 10000 http://10.0.0.115/ ``

### Open kibana  to check nginx default access log ###

``open web browser  http://10.0.0.115/5601``

### Have fun :-) ###
