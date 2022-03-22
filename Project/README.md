# Group names : BIVOLAROV Stoyan and AHMAD-Shukran Sozan

Here you will find our work for the project presented during the class
of TLC.

The project is separated in two parts: api (which is the backend) and front (javascript application).

In the back-end part (api), we add it the missing service in the docker-compose file which is the
quarkus service. As we know quarkus depends on mysql for the socket connection, we add it also
to the docker-compose file a health check command that checks if the mysql container is up and running
good without any problem, before starting the communication between the quarkus app and mysql.


In the front-end part (front), we add it multiple things.
Here it is :
  - A Dockerfile that basically runs the javascript application inside an nginx server.
  - An nginx.conf file that helps set up the connection between the front and the back.
    Also, All the proxy passes, so we can avoid the CORS Policy and make it work.

  - A docker-compose file that launch the front-end application.
  - an UML diagram that describes the whole architecture of the project.
