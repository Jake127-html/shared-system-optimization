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

**[9]** We will now comment in the work notes our findings, and email the client we beginning to uninstall suspicious applications.

<img width="1417" height="636" alt="SSO_Sc_18" src="https://github.com/user-attachments/assets/c025ede4-7983-42cd-8a5f-572e809b217d" />



<img width="1385" height="431" alt="SSO_Sc_20" src="https://github.com/user-attachments/assets/315dd67e-07c6-4d11-8a50-c760ef9bf3b0" />

**[10]** It is now time to begin uninstalling suspicious applications.

<img width="1021" height="765" alt="SSO_Sc_19" src="https://github.com/user-attachments/assets/e8aab6a4-2309-458e-8b1e-c849212a046d" />

<img width="1011" height="764" alt="SSO_Sc_21" src="https://github.com/user-attachments/assets/9b190b1c-c516-48ad-b7d1-5d876f54432b" />

We will go through the uninstall process for each of the applications.
