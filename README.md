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

![image](https://i.imgur.com/I38gaVr.jpg)

Configure Roles
- Log into http://localhost/osTicket/scp/login.php with the admin username and password that was set up in the previous installation of osTicket
- Navigate into the admin panel > agents > roles
- Add a new role called "Supreme Admin" that includes all checked access

Step 2:

![image](https://i.imgur.com/Z3RwjYA.jpg)

Configure Departments
- Navigate into admin panel > agents > departments
- Add a new department called "System Administrators" and hit create

Step 3:

![image](https://i.imgur.com/XaAxA1q.jpg)

Configure Teams
- Navigate into admin panel > agents > teams
- Add a new team called "Level 1 Support" and "Level 2 Support"

Step 4:

![image](https://i.imgur.com/k5sqndg.jpg)

Allow anyone to create tickets
- Navigate into admin panel > settings > user settings
- Registration Required: require registration and login to create tickets

Step 5:

![image](https://i.imgur.com/BtWor57.jpg)

Configure Agents (Workers)
- Navigate to admin panel > agents > add new
- Create two new agents and they can be named anything
- Reminder to create a password for those two agents

Step 6:

![image](https://i.imgur.com/Tm2gfTX.jpg)

Configure Users (Customers)
- Navigate to agent panel > users > add new
- Create two new users named anything
- Make sure to hit register to create a password for the two user accounts
- Create and remember the password

Step 7:

![image](https://i.imgur.com/7N0wj5F.jpg)

Configure SLA
- Navigate to admin panel > manage > SLA
- Add a new SLA and call it Sev-A with a grace period of 1 hour, 24/7
- Add a new SLA and call it Sev-B with a grace period of 4 hour, 24/7
- Add a new SLA and call it Sev-C with a grace period of 8 hour, business hours

Step 8:

![image](https://i.imgur.com/90iGTtB.jpg)

Configure Help Topics
- Navigate to admin panel > manage > help topics
- Add a new help topic and name it Business Critical Outage, remember to set the SLA to Sev-A in the second tab and create
- Add a new help topic and name it Personal Computer Issues, remember to set the SLA to Sev-B or C in the second tab and create
- Add a new help topic and name it Equipment Request, remember to set the SLA to Sev-B or C in the second tab and create
- Add a new help topic and name it Password Rest, remember to set the SLA to Sev-B or C in the second tab and create


<h2>Ticket Lifecycle</h2>

The SLA and incident response procedures will be periodically reviewed and updated to align with evolving system requirements and industry best practices.

<h2>Ticket SLA Examples</h2>

- Sev-A (1 Hour, 24/7) For instance, in the event of a Sev-A Data Breach, unauthorized access has been identified in the organization's database, posing a severe threat to the confidentiality and integrity of sensitive information. The incident demands an immediate response, with a targeted resolution time of 1 hour from detection, supported by continuous 24/7 coverage. The escalation path involves alerting the Information Security Team and top-level management for urgent and immediate attention.

- Sev-B (4 Hours, 24/7) For example, in response to a Sev-B Adobe Upgrade Issue in the accounting department, an immediate and comprehensive resolution plan has been activated. Recognizing the critical impact on operational efficiency, the incident response team is committed to a swift resolution within a 4-hour timeframe, operating around the clock. A post-incident review will subsequently analyze response efficiency, leading to continuous improvement and refinement of incident response procedures for ongoing operational excellence.

- Sev-C (2 Hours, Business Hours) Furthermore, a Sev-C incident has been identified involving performance issues with the Chief Financial Officer's (CFO) laptop, specifically slowness. The incident response team is committed to an immediate response within the designated business hours, aiming for a resolution within 2 hours of identification. The incident will be systematically addressed, from identification through acknowledgment and diagnostic procedures, to the implementation of necessary measures for resolution.

<h2>End user (Customer) Example</h2>

An end user using osTicket, might submit a ticket with the following example:

Subject: Unable to Access Email Account

Message:
"Hi Support Team,

I hope this message finds you well. I am currently experiencing issues accessing my email account. Whenever I try to log in, I receive an error message stating that my login credentials are incorrect. I have double-checked my username and password, but the problem persists. This issue is affecting my ability to communicate with clients and complete essential tasks. Could you please investigate and resolve this matter at your earliest convenience? My email address is Matt@example.com. Thank you for your assistance.

Best regards,
Matt"

<h2>Agent (IT Support Worker) Response</h2>

The support team's response in osTicket might look something like this:

Subject: Re: Unable to Access Email Account

Message:
"Dear Matt,

Thank you for reaching out to our support team. We understand the importance of accessing your email account, and we apologize for any inconvenience this issue may have caused.

To assist you further, we kindly request the following information:

Confirm your email address: Matt@example.com
Are you accessing your email through a web browser or an email client (e.g., Outlook, Thunderbird)?
Have you recently changed your password?
Once we receive this information, we will promptly investigate the issue and work towards a resolution. If you have any additional details or screenshots that may help us understand the problem better, please feel free to attach them to your response.

Thank you for your cooperation, and we appreciate your patience as we work to resolve this matter.

Best regards,
Jason"



