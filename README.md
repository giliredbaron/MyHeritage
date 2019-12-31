# MyHeritage 

This script creates and destroys web cluster (1 or many) web servers 
And a load balancer 

By editing the parameter file (swarm_vars.yml) before running build_cluster_HA_web.yml we can change the cluster state 
We can also use external vars for that (Shutdown the cluster): 

- ansible-playbook build_cluster_HA_web.yml -e mh_stuck_state=absent


Build_apache_container.yml - this script creates the web server custom image 
The image contains one costume page (as instructed) 
Ans a status page (so I can prove that the load-balancer is switching the connections between the servers) 
The image will have this structure:  name:tag
For this example, I used: mh-web:v1
For every time a new image needed - please change the tag name.


