# YelpApp
haha

#DataBase URL
jdbc:mysql://ec2-52-6-179-144.compute-1.amazonaws.com:3306/test

#How to visit cloud database
 mysql -h ec2-52-6-179-144.compute-1.amazonaws.com
 
#How to deploy war to cloud
scp -i newcckey.pem <name of the war> ec2-user@ec2-52-6-179-144.compute-1.amazonaws.com:./
sudo su
mv /home/ec2-user/<name of the war> /usr/share/tomcat7/webapps/
mv /usr/share/tomcat7/webapps/ROOT /usr/share/tomcat7/webapps/<ROOT+version#>
mv /usr/share/tomcat7/webapps/<name of the war> /usr/share/tomcat7/webapps/ROOT
service tomcat7 restart

