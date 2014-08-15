Project is sceleton of the JSF project with IceFace libs build in maven from the scratch (with no Dynamic Web Eclipse project).
Also it contains definition of tomcat7 deployment plugin - to use autodeploy after build.

MVN building with command:
$ mvn clean install tomcat7:redeploy

it needs the server definition on the mvn settings.xml:
$ sudo gedit /etc/maven/settings.xml

   <server>
      <id>tomcat7</id>
      <username>kropla</username>
      <password>123</password>
	<configuration></configuration>
    </server> 

.. and tomcat-users.xml:
$ sudo gedit /etc/tomcat7/tomcat-users.xml

 <role rolename="manager-gui"/>
  <role rolename="admin-gui"/>
  <role rolename="manager-script"/>
 <user username="kropla" password="123" roles="manager-gui,admin-gui,manager-script"/>
