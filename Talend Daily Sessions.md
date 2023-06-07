## SESSION 1 - 11/01/2023 

TAC architecture / Talend data fabric

(Create, delete, modify ==> user )       TAC WEB UI 

6.3 => Default password / Talend 123
7.2 => Account => LDAP (Lightweight directory access protocol) ==> SSO/Password
7.3 => Based on the Project requirement

Read access or write access 
DEV => R/W access
PROD => R/W access

>!!code repo corrupt on 6.3!!

TAC accessors
ADMIN => Change Anything (access everything)
VIEWER => Only view can't modify 
OPERATIONAL/DESIGNER => Create or deploy project
For 7.3  => System Admin (extra)

TAC WEB UI
1. Users: Project wise, Prod mostly have read access
2. Monitoring: Viewer role
3. Dev: Viewer role/ Operational/ Designer
4. Admin: All 4 roles

PROJECTS (60 to 70 projects approx)

>New projects=>  AWS JOB server (**used to ingest data and to execute data profiling or to create sample data on the ingested data**)

1. ADD job into TAC => with WEB UI
2. Everyweek of Monday => allign
3. Daily/2/3 times... SET Triggers

If someone left with running job (not informed) => take remote (talend studio)
Lock the job in the studio itself
can contact admin team to modify the jobs

Locking jobs opt2 :
 DA approvals => wont open the lock
 5 to 10 members => they'll access (costly)
40Projects => to accounts.

>Talend admins => corrupted on specific SSO
   (Functional SSO) => Time on issues.

-----------------------------------------------------------------------
## SESSION 2 - 12/01/2023 

TAC => Admin team, Dev team, Operations team .
>Activity, monitor, Console, (AMC) UI

ADMIN: 
one=> stuck job => TAC DB => Log Checking

STATUS NOT UPDATED

sec1: Update the backend  of TAC => Running State to ready state .
sec2: TAC DB ready to run (status), but job ready => Duplicate the label

### Permanent Solution: 
> AWS Jobserver , on premise, TAC server 

Restart the services, jobservices, (kill the idle session)
Clean the cache ===> Mostly resolve on Restarting

### SATURDAY => Restart 
>(Duplicate job)
   Re-RUN Complete Successfully.

ISSUE: 
Job within 30min *buffer*
if exceeds=> 1hr => monitoring team raise the ticket.
Need to identify the issue (Whether belongs to Talend or Db issue or Dev issue)

Job level => Dev not have Triggers

Prod only have triggers, EP(Execution Plan) 
it'll be sequence

## JOB Conductor

> add the job (provide all details)
> Normal task, Respectively Label, JOB name 
> SAVE

*Generate* => Job'll be generating (changes on server from studio)
*Deploy* => Deploy the job (Completed)
*RUN*  => Run the job

NEXUS: ARTICRAFT REPOSITORY
>Replace for CMD, No waiting time (no generate)
>Straightly Deploy

3000 jobs down?? 
> Approvals from higher level 
> TAC restart

-----------------------------------------------------------------------
## SESSION 3 - 13/01/2023

JOB conductor => Execution task 
JOB 4j level => warn / debug (Detail Error)
Triggers ?=>

USER group => Platform team => so projects
> pls provide all (80) they will access to

1. Platform team/ group => 25
2. Operational team => 20 
3. Monitoring team => 10 
4. dev team => need the projects
>
>example: 69 named users (pop-up)
100=> 120 licenses
2-7PM crucial time => Concurrent people
opt : wait until TAC open

concurrent to named users => licenses update (based on develop)

*7 Days only log storage - TAC DB storage*

--------------------------------------------------------------------------------------------------

## SESSION 4 - 17/01/2023

Architecture similar across all the project
just little bit changes on NEXUS (repo) or (storage), whether that is AWS/ on premise

Production => Environment => Scenario
> Before 30min/1hr => But more than 7/8/20hrs.... more memory will occupy
    Production is an LIVE environment , so we cant create job in production
    only in dev / QA
    It'll impact, if we dont know the time for the job

>if new member => they'll test in QA Environment . there he can built the new or sample jobs 

DEV                                                       PRODUCTION

-- No time concerns                       -- Scheduled Jobs without any Delay (TAC services)
-- Not stable                                        -- Don't Shut down
                                                            -- 24/7 running time
                                                            -- Greenplum Databases
                                                            -- Stable version

GIT LEVEL=> TAC creating jobs
>27:00
Ticketing => GE (Service Now)

TALEND VENDOR => if 3000 jobs run, in long time
> For time being=> Restart the server, it'll resolve

But if repeats, Contact the vendor team (for the issue)
For issue : Vendor provide respective patches
then'll resolve.
>30:00

7.2 => 2020 upgraded
7.3 => 2022 upgraded

JOBLIST:
Every logs => ON TAC DB (one project TAC list)
>on weekly maintenance also.

PUTTY SESSION (SSH)
>Connect to server
>Admin have the access for user

-----------------------------------------------------------------------

## SESSION 5 - 18/01/2023 

SSO => face login issue
7.2, 7.3 => LDAP account

Talend studio => login

Production server URL / DEV also 

USERNAME    SSO
PASSWORD    SSO

MANAGE CONNECTIONS
>24:00

ISSUE:
> Remove the workspace folder , it may be corrupted
> URL: Check the issue
> GIT Token suggest to regenerate

-----------------------------------------------------------------------
## SESSION 6 - 19/01/2023

MENU => CMD line

ESB Infrastructure 
>An Enterprise Service Bus (ESB) is a type of infrastructure software that acts as an intermediary between different applications and systems. It is designed to facilitate the communication and integration of different software systems and applications within an organization. The ESB acts as a central hub for routing, transforming, and managing the flow of data between different systems.

USER Settings => GIT Login => GIT Password and Git token

SERVERS
>virtual servers, on prem 
>Based on load balancing
>IF Multiple on-premise server, it'll changed to virtual server. (For Load Balancing)

CONFIGURATION 
>Download log => Available
30:49

PUTTY Connecting : (AMAZON LINUX 2 AMI) EC2

ps -ef
bhi-master \ username
cd \ data
ls -ltr
exit
> JOB SERVER => Get cred from team

ps -ef | grep itac

1. Jobserve => hostname -i
2. ps -ef | grep -i jobservermain
3. sudo su - Talend Admin

--------------------------------------------------------------------

## SESSION 7th  23-01-2023

GIT (Enterprise)

Talend admin, if (no access admin (ONLY L3))

L1 and L2 as admin they can only (mostly) verify but can't provide access

URL for every environments

URL=> Copy => TAC => Save

Create a project on TAC, after git

1. Approved or not 
2. Check the URL
3. Respective project in the dev, then test on PROD

CREATION:

GIT => REPO => Click => new=> create => the url
Copy => url => Save on TAC

BH => Functional account (HAKIM)

### License Validation

1. Replacing the license file from CMD and restart the CMD services
2. Take a copy of license file
3. Replace it with new hard license file
4.  Re-start CMD line services

Then, Add new license on TAC UI.

GIT Commit - best practices

Code i'll be corrupted,  if new built => create a job on locally , then come to remote mode

REMOTE MODE : *drop down to local mode*

#### PROJECT CORRUPTED:

If see the braces, on project tag => Project is corrupted

Then, check on the GIT/CODE level

Reverting back => It'll loss the current developed project
Suggest: Try on local mode, And commit on remote mode

Any corruption, got?

but on TAC Web UI, GIT level, Studio => Also fine>>>>>

Mostly it's like dead server. IT won't take any actions.

===>

In the TAC server, WE've workspace (work and temp) folders.

SOLVE: We'll remove the temp folder for the respectivr folder.

And check on GIT, Whether it's good or bad commit.

===>
EXAMPLE:

if friday commited correctly....if we revert back on monday..make sure => backup taken.

NOTE : file size differs, on TAC after commit. like 1GB to 20-30MB

*Mostly file size decreased.*

===>
GIT Code 
1. check the file size 
2. remove from temp (with backup)
=>
What if , unable to open the studio level
=> login to respective git => whether the DEV / PROD => Commits

#### License Validation

(*only once in a year*)

1. Client purchase
2. 160 - licenses => 
3. Talend vendor team => 
4. share on server=> 
5. remove the old file =>
6. Restart the services.

Open => TAC  => Add => Browse => Upload

### Ticketing Tool

Three ticket types:

1. RITM
2. Incident
3. Change Request

> RITM (request item):
It is an access request (GIT, TAC, ITEM)
Related to access issues.

> INCIDENT:
> if Job unable to run, connect to studio, didn't see the job log , long running
> Then, It'll be consider as an incident.

>CHANGE REQUEST (CR):
>Modify or (done any implementations) on environment 
>Like (upgrade or modify) => go with the CR
>EX: Update py 3.6 to 3.8 on current environment
>
APPLYing new patches (UPGRADE)    |
Modify the config (MODIFY)              |    => After this upload the EVIDENCE of the respective CR 
Implementation.                                 |          with the (ticket's )TIMESTAMP

Can't do CR, Without approvals.
Incident, we can check.
RITM, mostly L1

Based on the priority , we'll start work on the ticket.

#### Best Practices:

 no corruptions?
 something on local or remotely.
 Escalate to DE
 => every dev'll follow the best practices

POWER Activites on GIT level:
1. Creation on yearly 
2.  weekly 10- 5 tickets (access)
===>

CHANGE MANAGEMENT PROCESS: 

1. Approvals
2. Cutoff date
3. Understand process (including tool to log changes)
      -- Full cycle change
      -- Emergency change
4. Take a window time.

Whether the implementaion, updation, Modify => Raise the CR

1. If on DEV, URGENCY : Take window time. 6PM - 7PM.
2. Send the plan maintenance (setting parameters).
3. If we have time, update CR on the weekly maintenance.

First (dev), then 15days monitor . 
looks good => then move to the production
without resolving DEV, NO PROD

===>
EXECUTION - CR

1. Outage => Server is down => without modifying => give the Outage notification
2.  Without any notifications, no modification or updation
3. if server down => mail on resepective DL or notify the team
===>

RCA (Root cause analysis) Process:

If repeated issue, we need to provide the RCA.

===>
Oneidm=> management / ticketing / ID tool
(action, domain, project, role. (Add to request))
Manager approves, once approved ...ticket'll be created.

----------------------------------
## SESSION 8th 24-01-2023

Before updation => Take backup of => current TAC, NEXUS, Directory.

#### 7.2 same config on 7.3

1. JDK Install, Software update, config
2. Set Schema on TAC
3. Creating Organization on GIT for 7.3

SCRIPTS AVAILABLE

Apply Patch => (Backup of config properties and Quartz properties)

=> Download the patch
=> Respective folder
=> Then copy the backup

MOSTLY, Occurs on Weekly maintenance.

if urgency, for dev => Weekdays after 9PM IST 

Patches are completely on LINUX Server.