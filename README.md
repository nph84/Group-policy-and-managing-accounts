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
<img src="https://github.com/user-attachments/assets/22bf1ea4-38bc-40c0-a89e-01fe00b7790b" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/b6ab9c2b-8bee-43a8-a102-cfed05d5e38d" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/aea31472-71b8-4a42-a388-88a3c8c9e622" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/fc9c3773-e97f-4eaa-948a-43b986bcab4b" height="80%" width="80%" />  
</p>
<p>
First, we're going to configure a domain password lockout policy for Active Directory using Group Policy editor.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/35a22760-d1c3-433d-b663-a3068feba53b" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/7592f75b-8938-497d-9bd1-0e6b576c3113" height="80%" width="80%" />
</p>
<p>
Now, we will log in as the administrator to force the policy to update so we don't have to wait for the automatic 90-minute policy update time window.
</p>
<br />




<p>
<img src="https://github.com/user-attachments/assets/267217b4-67ae-4e4c-90b1-ff0521552cbe" height="80%" width="80%" />
</p>
<p>
Then, we'll pick a random user account that was previously created.
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
<img src="https://github.com/user-attachments/assets/8615b92e-71bd-4f64-ae5f-2a032c59065b" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/adb7253f-a4ab-4438-a398-188a73dc5d15" height="80%" width="80%" />
</p>
<p>
Observe that the account has been locked within Active Directory.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/22ac5e35-537e-430d-a1e8-88ca644985d7" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/59270e72-cdb8-4b9c-9785-7cb6940418e3" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/de42b606-be90-4c02-8225-83aef1e520a6" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/19142556-0f68-4ed0-8a4b-86eea9c47496" height="80%" width="80%" />
</p>
<p>
Reset the password.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/20e906f0-0b61-438b-a795-748b74f3b46b" height="80%" width="80%" />
</p>
<p>
Unlock the account.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/c9a892bd-0c1a-4396-bc0f-d203a8ec062e" height="80%" width="80%" />
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





































































