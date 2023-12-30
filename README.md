<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration and Ticket Lifecycle</h1>
This tutorial outlines the post-install configuration and ticket lifecycle of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Configuration Steps</h2>

Step 1:

![image]()

Configure Roles
- Log into http://localhost/osTicket/scp/login.php with the admin username and password that was set up in the previous installation of osTicket
- Navigate into the admin panel > agents > roles
- Add a new role called "Supreme Admin" that includes all checked access

Step 2:

![image]()

Configure Departments
- Navigate into admin panel > agents > departments
- Add a new department called "System Administrators" and hit create

Step 3:

![image]()

Configure Teams
- Navigate into admin panel > agents > teams
- Add a new team called "Level 1 Support" and "Level 2 Support"

Step 4:

![image]()

Allow anyone to create tickets
- Navigate into admin panel > settings > user settings
- Registration Required: require registration and login to create tickets

Step 5:

![image]()

Configure Agents (Workers)
- Navigate to admin panel > agents > add new
- Create two new agents and they can be named anything
- Reminder to create a password for those two agents

Step 6:

![image]()

Configure Users (Customers)
- Navigate to agent panel > users > add new
- Create two new users named anything
- Make sure to hit register to create a password for the two user accounts
- Create and remember the password

Step 7:

![image]()

Configure SLA
- Navigate to admin panel > manage > SLA
- Add a new SLA and call it Sev-A with a grace period of 1 hour, 24/7
- Add a new SLA and call it Sev-B with a grace period of 4 hour, 24/7
- Add a new SLA and call it Sev-C with a grace period of 8 hour, business hours

Step 8:

![image]()

Configure Help Topics
- Navigate to admin panel > manage > help topics
- Add a new help topic and name it Business Critical Outage, remember to set the SLA to Sev-A in the second tab and create
- Add a new help topic and name it Personal Computer Issues, remember to set the SLA to Sev-B or C in the second tab and create
- Add a new help topic and name it Equipment Request, remember to set the SLA to Sev-B or C in the second tab and create
- Add a new help topic and name it Password Rest, remember to set the SLA to Sev-B or C in the second tab and create

Ticket Lifecycle



