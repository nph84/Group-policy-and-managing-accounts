<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the process of managing accounts through "Group Policy".<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Dealing with account lockouts
- Enabling and disabling accounts
- Observe logs

<h2>Deployment and Configuration Steps</h2>

**Dealing with account lockouts**


<p>
<img src="" height="80%" width="80%" />
</p>
<p>
First we're going to configure domain password lockout policy for Active Directory using group policy editor.
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/267217b4-67ae-4e4c-90b1-ff0521552cbe" height="80%" width="80%" />
</p>
<p>
Then we'll pick a random user account that was previously created.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/d9912e62-f2a8-4079-aff2-b18d30315427" height="80%" width="80%" />
</p>
<p>
Next, we will attempt to log in 10 times with a bad password.
</p>
<br />

<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Observe the account has been locked within Active Directory.
</p>
<br />



<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Unlock the account.
</p>
<br />



<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Reset the password.
</p>
<br />



<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Log in with the unlocked account.
</p>
<br />

---------

**Enabling and disabling accounts**

<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Disable the same account in Active Directory.
</p>
<br />



<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Attempt to log in with the disabled account while observing the error message.
</p>
<br />


------------------

**Observing Logs**

<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Observe the logs in the domain controller.
</p>
<br />




<p>
<img src="" height="80%" width="80%" />
</p>
<p>
Observe the logs on the client PC.
</p>
<br />





































































