# Group Names : BIVOLAROV Stoyan and AHMAD-Shukran Sozan

The files that you will find here are describing the first Practical
Session of the class TLC.

We divided the two different parts in two different directories.

In the first one : "Nginx and LoadBalancer" -> you will find
the docker-compose file that let us launch 4 nginx servers with a load balancer.


In the second one : "LoadBalancer and Java App" -> you will find
a Dockerfile and a docker-compose file.

The Dockerfile let us launch the Java Application described in the practical session.
The docker-compose file let us launch 4 instances of this application and a load balancer.
Later, when we launch it we can see the redirection that the load balancer makes between the users
and the application.
