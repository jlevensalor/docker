sudo docker build jleve/oracle (OR) sath89/oracle-xe-11g
sudo docker pull jleve/oracle
docker run --name orcldb -d -p 8080:8080 -p 1521:1521 jleve/oracle
docker ps (get the information to connect with)
docker port orcldb (verify ports are open)
docker exec -it orcldb bash  (OR) hash 449dxx

From the bash prompt run sqlplus
user-name: system password: oracle  (change this)

Create Oracle user
Create a user called OE with unlimited quota on SYSTEM tablespace and password as OE. First, drop the OE user if it already exists.
 
DROP USER OE;
CREATE USER OE QUOTA UNLIMITED ON SYSTEM IDENTIFIED BY OE;
Grant CONNECT and RESOURCE roles to the OE user.
GRANT CONNECT, RESOURCE TO OE;
 
The OE user gets created.


Creating an Oracle Database Table
 
Create an Oracle Database table OE.WLSLOG with the following SQL statement.
 
CREATE TABLE OE.WLSLOG(time_stamp VARCHAR2(45) PRIMARY KEY,category VARCHAR2(25),type VARCHAR2(25),servername VARCHAR2(25),code VARCHAR2(25),msg VARCHAR2(45));
 
The OE.WLSLOG table gets created.

Add data to the OE.WLSLOG table with the following SQL statements.
 
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:16-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000365','Server state changed to STANDBY');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:17-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000365','Server state changed to STARTING');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:18-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000365','Server state changed to ADMIN');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:19-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000365','Server state changed to RESUMING');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:20-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000331','Started WebLogic AdminServer');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:21-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000365','Server state changed to RUNNING');
INSERT INTO OE.WLSLOG VALUES('Apr-8-2014-7:06:22-PM-PDT','Notice','WebLogicServer','AdminServer','BEA-000360','Server started in RUNNING mode');


Select * from oe.wlslog; 


