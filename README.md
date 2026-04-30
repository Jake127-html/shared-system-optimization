# 💼 Shared System Optimization
The purpose of this lab is to simulate the IT service engagement workflow through a real Google Business listing utilizing ServiceNow, the CompTIA 6-step methodology, and performance remediation. 

### *Scenario*:
**3/24/26, 10:32am**  
Customer calls, and requests laptop to be investigated for slow performance.  
They are unable to use required programs for work without severe performance issues.
Customer says they work from home at an Engineering firm and needs the device fixed ASAP. They have a project due on Monday **3/27/26**.
Says they share laptop with child son sometimes. 

<details><summary>Click to see Lab components</summary>
           
           
           Note: The Virtual Machine being operated on was utilized  
           in the precursor lab titled, "Dynamic Analysis of Malicious 3rd Party Software."

           Also, due to the innate nature of constrained processing power inside Virtual Machines, exact 
           performance metrics will not be recorded, however, in a real scenario those are important to identify the result.
           Hypervisor: Virtualbox Version 7.2.6 r172322 (Qt6.8.0 on windows)
           Host: Windows 10 Home 22H2 19045.6466
           Ticketing Software: ServiceNow PDI (Private Developer Instant)
          

</details>

## Service Intake
**3/24/26, 10:32am**  
**[1]** Firstly, before opening a new Incident we must navigate to the proper screen.
<img width="1920" height="890" alt="SSO_Sc_1" src="https://github.com/user-attachments/assets/cd96c0e4-2624-4eba-8b4f-02563fea4282" />

**[2]** Next, we will create a new Incident.
<img width="1920" height="907" alt="SSO_Sc_2" src="https://github.com/user-attachments/assets/114a64b0-1f07-46c9-8a5e-3230050e30fe" />

**[3]** Since customer has a project due, and is unable to work from home, this is a critical Incident so we will be selecting Emergency Response.
<img width="1920" height="911" alt="SSO_Sc_3" src="https://github.com/user-attachments/assets/c12af2f5-956a-4625-9b7a-a07419b2bffc" />

**[4]** This is a preview of our Emergency Incident Response Form.
<img width="1323" height="396" alt="SSO_Sc_4" src="https://github.com/user-attachments/assets/75d6cd40-af86-42c8-80f0-f4ccf7be86ca" />  
**[4A]** This is a preview of our Standard Incident Response Form. Note: Our Elite Support offer requests will always contain a "Critical" priority.
<img width="1324" height="392" alt="SSO_Sc_5" src="https://github.com/user-attachments/assets/7adf97e6-7e57-4c83-94fe-8d5af488173e" />
**[5]** Our Callers' Name is Fred Luddy.
<img width="989" height="675" alt="SSO_Sc_6" src="https://github.com/user-attachments/assets/0fd6a560-729a-4bd7-bf57-e895e3c5772d" />
**[5A]** Incident Record
```
Category: Software  
            *Customer is experiencing computer performance issues

Subcategory: Operating System
            *Customer is having trouble navigating Windows 11 and using and installed apps.

Service: IT Services
          *Customer is requesting IT Support.

Service offering: Customer has chosen Premium Support offering
                    *Customer requests Premium Support

Configuration Item: Windows 11
                    *Windows 11 Assigned to Fred Luddy, the Operating System customer is using.

Channel: Phone
          *Customer called Howell TechNow and requested support over the phone.

State: New
        *Incident Record is being Newly created.

Impact: 2 - Medium
         *Device is functional with performance degredation.

Urgency: 1 - High
          *Customer has work project due on Monday, and current performance degredation
           limits progress towards completetion.

Priority: 2 - High  
               *Matrix calculation between Impact & Urgency identifies this Incident as High priority.

Assignment group: Incident Management
                   *Group associated with providing support.

Assigned to: Jake Rivas
              *Group member providing support.
```
**[5B]** This is what are new Incident Record looks like so far.
<img width="1302" height="379" alt="SSO_Sc_9" src="https://github.com/user-attachments/assets/d8794c08-ee06-44aa-b35d-38125bc3d567" />

**[5C]** We have now filled out the remaining forms.
<img width="1308" height="393" alt="SSO_Sc_10" src="https://github.com/user-attachments/assets/e94da537-6a12-4154-95c8-9942277d4ad3" />

**[5D]** Notification of Incident Assignment
<img width="1218" height="437" alt="SSO_Sc_11" src="https://github.com/user-attachments/assets/b64e0765-754c-4ea8-882e-31817c9d6bbf" />

**[6]** We will now immediately notify our Customer that we have processed their request and are now working to fix their issue.
<img width="1916" height="422" alt="SSO_Sc_13" src="https://github.com/user-attachments/assets/0bc6914c-0136-4151-9141-592710e8e655" />

**[6A]** Preview of customer confirmation email. Note: Due to ServiceNow's handling of PDIs (Private Developer Instances) emails are not actually sent through SMTP. However, we can preview "sent" emails.
Additionally, in a production environment the ticket would not state that the "System Administrator" opened the Incident. Rather, this has to do with ServiceNow's methods of handling PDIs, despite 
using the "impersonate" tool and assigning the Incident to user Jake of Howell TechNow.  
  
Note: For the purposes of this lab, response and Incident Resolution times will not exactly align with real-time production requirements.
<img width="472" height="699" alt="SSO_Sc_14" src="https://github.com/user-attachments/assets/1184349e-120d-45a8-b175-46a947bebd4d" />

**[7]** Now we will "open" the suspect machine in Virtualbox. This is the immediate screen we are faced it. 

<img width="1019" height="768" alt="SSO_Sc_15" src="https://github.com/user-attachments/assets/42b94382-f626-401b-9918-c66c65a22f1b" />

**[8]** Now, we will gather information. We will open task manager and see what is using the most resources on idle.

<img width="1020" height="763" alt="SSO_Sc_16" src="https://github.com/user-attachments/assets/e1d2a03a-6c33-4e81-828c-10079cf34c2a" />

Immediately we see several suspicious applications which are eating up processing power. Further research will be conducted to identify unauthorized processes.

<img width="1016" height="762" alt="SSO_Sc_17" src="https://github.com/user-attachments/assets/f21a02c7-2816-435d-b9db-7667fabc03d0" />

**[9]** We will note the probable cause in the incident details.

<img width="629" height="266" alt="SSO_Sc_37" src="https://github.com/user-attachments/assets/191691ba-9bc6-4594-8afa-75084ceb8ff1" />



**[9A]** We will now comment in the work notes, our findings, email the client, and begin to uninstall suspicious applications.

<img width="1417" height="636" alt="SSO_Sc_18" src="https://github.com/user-attachments/assets/c025ede4-7983-42cd-8a5f-572e809b217d" />



<img width="1385" height="431" alt="SSO_Sc_20" src="https://github.com/user-attachments/assets/315dd67e-07c6-4d11-8a50-c760ef9bf3b0" />

**[10]** It is now time to begin uninstalling suspicious applications.

<img width="1021" height="765" alt="SSO_Sc_19" src="https://github.com/user-attachments/assets/e8aab6a4-2309-458e-8b1e-c849212a046d" />

<img width="1011" height="764" alt="SSO_Sc_21" src="https://github.com/user-attachments/assets/9b190b1c-c516-48ad-b7d1-5d876f54432b" />

**[10A]** We will go through the uninstall process for each of the applications. Please note that uninstalling "profile" or "user data" is important to removing the entirety of an apps signature on your computer. Also, after uninstalling one more apps the PC should be restarted.

<img width="632" height="485" alt="SSO_Sc_23" src="https://github.com/user-attachments/assets/6a02b1d2-ba36-496c-8b32-6393eb56cb44" />

**[10B]** **Important** Some software will actually hide from your apps list in the settings. You must manually locate the folders for these software, or investigate.

<img width="1020" height="765" alt="SSO_Sc_24" src="https://github.com/user-attachments/assets/943f7200-5e3f-4e26-bd69-a76fb35d5a04" />

**[10C]** To find out where this app's files are you must open the following menus:  

```
Right click -> Properties -> Shortcut -> Target & Shortcut
```

<img width="356" height="536" alt="SSO_Sc_26" src="https://github.com/user-attachments/assets/c39dd00a-cc4a-4767-a54d-26e5bd671c87" />

**[10D]** Then, locate and delete the files manually at the target and shortcut directories.

<img width="839" height="575" alt="SSO_Sc_28" src="https://github.com/user-attachments/assets/f9b0ac7f-27c9-4417-b2c1-01d3b9316e54" />

**[10E]** I actually ran into an issue where a process of iWin Games is running, which is preventing me from deleting the files currently in use.

<img width="1018" height="765" alt="SSO_Sc_29" src="https://github.com/user-attachments/assets/4af76cea-6413-4714-ba09-9e6e998d83fc" />

**[10F]** To fix this issue I navigated to the task manager in order locate and end any processes by iWin Games that are running.

<img width="705" height="672" alt="SSO_Sc_30" src="https://github.com/user-attachments/assets/8fded01a-1565-4368-899d-63848b3c0201" />


<img width="725" height="431" alt="SSO_Sc_31" src="https://github.com/user-attachments/assets/2e259d1f-c924-420c-916c-4035991551e6" />


**[10G]** I then tried again to delete the conents only to find that there are 1 or more processes still running. So I navigated back to task manager to track down the last process.

<img width="706" height="675" alt="SSO_Sc_32" src="https://github.com/user-attachments/assets/a3b42453-fd41-4aaa-b0dd-c5ff8805b26b" />

**[10H]** Success, iWin Games is sucessfuly uninstalled.

<img width="622" height="254" alt="SSO_Sc_33" src="https://github.com/user-attachments/assets/787be02c-9c81-4e2d-961b-7a3deefa3481" />

**[11]** Another software is giving the same issue as iWin Games. It is not uninstallable from menus, and I had to manually locate the program directory and delete it. This seems to be not uncommon in greyware.

<img width="1014" height="762" alt="SSO_Sc_34" src="https://github.com/user-attachments/assets/da790f1d-4d13-4987-92a9-cb0139990f4d" />

**[12]** We will now put in the work notes our progress on the device.

<img width="780" height="530" alt="SSO__Sc_36" src="https://github.com/user-attachments/assets/2237c151-142f-4f8c-adaf-bcaf0cc7c9ea" />

**[12A]** Additionally, we will notify our client, Fred, through email to assure him he will have his device back soon.

<img width="1102" height="570" alt="SSO_Sc_38" src="https://github.com/user-attachments/assets/b4429701-6983-4c87-9771-c9fd38ea3da8" />



**[13]** There are still remnants of iWin Games services so we will delete them manually in the CLI

<img width="946" height="584" alt="SSO_Sc_35" src="https://github.com/user-attachments/assets/5b84c29f-98b1-4e77-b3cc-e6022d8742d0" />

<img width="1020" height="765" alt="SSO_Sc_39" src="https://github.com/user-attachments/assets/6b08f0e5-fe20-455c-8173-a92fdca656f1" />

**[14]** We will run a FULL Microsoft Defender scan for a deeper search of the computer. It will take a while.

<img width="1015" height="765" alt="SSO_Sc_41" src="https://github.com/user-attachments/assets/860354ff-0922-47a1-9731-8632c96b865e" />

**[14A]** Windows Defender actually detected several highly suspicious files so those will be removed as well. There is even record of a previously detected Windows Defender Backdoor that tried to take advantage of a popular vulnerability in Windows 10, utilizing methods to disable Defender from functioning properly. Yet Defender pulled through! We will be entering this in documentation later to look for this in the future.

<img width="875" height="673" alt="SSO_Sc_42" src="https://github.com/user-attachments/assets/0678b710-aa9d-445a-bbf5-9c4bad71c779" />

<img width="1011" height="764" alt="SSO_Sc_43" src="https://github.com/user-attachments/assets/cf8612f3-337c-46ae-ad77-1b5142666b19" />

<img width="1017" height="762" alt="SSO_Sc_44" src="https://github.com/user-attachments/assets/6ec95c20-c215-4171-a838-03aef00c8936" />


**[14]** We will continue to search, now in the Registry, for further obsolete entries and delete them.

<img width="857" height="509" alt="SSO_Sc_40" src="https://github.com/user-attachments/assets/8367189e-2010-462a-beae-782151ee7e8c" />

**[15]** We are finished clearing the computer of PUPs and can now work on the incident record. After we finish the incident report we can notify Fred.

<img width="328" height="684" alt="SSO_Sc_45" src="https://github.com/user-attachments/assets/6bb9e226-a765-48b0-a829-1a0374648c13" />

```
Resolution Notes:

Hi, Fred. Your PC is back to normal performance, and is ready for pickup. I removed various unauthorized applications, Viruses, and Malware. In the future, I recommend if you share your work device with your family, to create separate accounts for each person. That way, you can enable protections that limit what a person can do on your computer to prevent this from happening the future. If you have any questions, or run into any problems please don't hesitate to contact us. Thank you, and good luck on your project!

Root Cause: Severe performance degradation caused by installation of Potentially Unwanted Programs and resulting in various active Malware and Viruses.

Solution: Returned performance through; Uninstalled 15 programs, various malicious Registry entries, and viruses.

Microsoft Defender is now the default Antivirus instead of web-downloaded software.

Microsoft Defender Backdoor removed at the following directories:

C:\Users\Jake\AppData\Local\Google\Chrome\User Data\Default\Cache\old_Cache_Data_000\f_0002d7

C:\Windows\System32\DefenderTamperingRestore

Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection
```

