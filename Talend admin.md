### TAC
Talend Adminstration center
TAC provides a centralized and web-based interface for managing and monitoring Talend jobs and projects. 
> user creation, mointoring jobs, managing projects, config servers

### User Creation 
 > Login to TAC
 > settings => users => Add 
 > Give the credentials (svn login , git login, type, role )
 > give the required access to the users
 > >we can assign specific projects and manage access in TAC for them 
 > >(whether dev, QA, PROD)
 
### Project Creation

Login to TAC
 > settings => projects => Add 
 >
    Give the credentials (Label, Active, reference, desc (job), Author, Project type, storage)
 > -- Advanced settings :: ( URL (git), login, password , commit mode)
 > 
 > give the required access for the projects 
 > >Assign the user for the project , whether choose what they can do with the projects.
 > click save.
 
### Project Access

Projects page => select the project 
Manage the access their, we can change the type, storage , label
we can add users for that projects 

### Configuration Page 

In configuration page we can download the logs

we can manage jobserver url, databases , artifact repository 
 and give and can change the required parameters 

### Job Conductor - Adding / checking the job

> add the job (provide all details)
> Normal task, Respectively Label, JOB name 
> SAVE

*Generate* => Job'll be generating (changes on server from studio)
*Deploy* => Deploy the job (Completed)
*RUN*  => Run the job

### Server status in WEB UI
 servers page in the conductor
 there we can check the status of the servers (running, stopped, unactive ) and details such as the IP address, the version, and the last connection date.

### Virtual servers

we can create new virtual server in the servers tab
give the name, port numbers, 
we can assign jobs to the server, monitor the performance of the server 
check the logs
(isolate the jobs, running on respective servers)

>virtual servers, on prem 
>Based on load balancing
>IF Multiple on-premise server, it'll changed to virtual server. (For Load Balancing)

### User settings
 there we can update the name , password, 
 Grant role, access projects

### Linux server how to check the TAC / job server:

connecting putty session , config with commands

PUTTY Connecting : (AMAZON LINUX 2 AMI) EC2
ps -ef
bhi-master \ username
cd \ data
ls -ltr
exit

> JOB SERVER => Get cred from team
ps -ef | grep itac

1. Jobserver => hostname -i
2. ps -ef | grep -i jobservermain
3. sudo su - Talend Admin

### Commandline uses 

we can run job, with context parameter and name, value
deploy jobs using commands 
create user 
check the server status

### Nexus 

it is an articraft repo 
>Replace for CMD, No waiting time (no generate)
>Straightly Deploy

### Connect Studio

open tac studio on local
welcome page => choose remote
give the url , login credentials
test connection
process
once connected we can view the project

### How to connect TAC

open TAC server URL
enter username and password
connect to TAC WEB UI