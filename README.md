<h1>Creating Organizationsal Units, Groups, and Users</h1>

<h2>Description</h2>
This project provides a Standard Operating Procedure (SOP) for guiding individuals through the process of creating and managing Organizational Units (OUs), security groups, and user accounts in Windows Active Directory Domain Services (AD DS). The document is designed to help users organize the Active Directory structure, create departmental OUs, configure security groups, add users, and manage group memberships using Active Directory Users and Computers (ADUC).
<br />

<h2>Objectives</h2>

* <b>Provide clear, step-by-step instructions for creating and organizing Organizational Units (OUs) within Windows Active Directory Domain Services (AD DS).</b>
* <b>Guide users through the process of creating and managing security groups to support centralized access control.</b>
* <b>Demonstrate how to create, configure, and manage user accounts and assign users to the appropriate security groups.</b>
* <b>Create a standardized procedure for organizing Active Directory resources that can be used for training, onboarding, and IT administration.</b>


<h2>Intended Audience</h2>

* <b>System administrators</b>
* <b>Windows Server administrators</b>
* <b>IT support staff</b>
* <b>Students and IT trainees learning Windows Server and Active Directory</b>
* <b>IT professionals responsible for server deployment and domain infrastructure</b>


<h2>Project walk-through:</h2>
<p align="center">
First, open Server Manager. In the upper right hand corner open Tools and scroll down to Active Directory Users and Computers: <br/>
<img width="677" height="615" alt="image" src="https://github.com/user-attachments/assets/0e55c6ef-edb8-4308-b3c2-87f865640fcf" />
<br />
Select the domain in which you created/wish to use. Clicking the arrow to the left of the domain will allow you to view all OUs for this domain. To add an OU, right click on the domain, scroll down to New, and pan down to Organizational Unit: <br/>
<img width="975" height="682" alt="image" src="https://github.com/user-attachments/assets/72d49527-bc41-4724-b751-a95cf97457dd" />
<br />
Choose the name of your OU and click OK:<br/>
<img width="641" height="422" alt="image" src="https://github.com/user-attachments/assets/3e2c3c6b-b1bc-4987-8ddf-d2cda3978e34" />
<br />
Now decide how you are going to group your employees, either by location or department/job role. I find that job role is easier, especially when you have many locations. Right click on Employees, scroll to New, and select Group:
<br/>
<img width="975" height="763" alt="image" src="https://github.com/user-attachments/assets/f4718370-9608-4670-b505-398b7e37e952" />
<br />
Choose your Group name, the Group Scope you want is Global and the Group Type is Security, now click OK. I am going to repeat this step and create Sales, IT, and Accounting Groups:<br/>
<img width="675" height="589" alt="image" src="https://github.com/user-attachments/assets/4b435794-7d59-49c4-aa47-d7815c459589" />
<br />
Next, we are going to create Users for our Groups. Right click on our Employee OU, scroll to New, and select User:<br/>
<img width="975" height="779" alt="image" src="https://github.com/user-attachments/assets/4fe9a5d0-31d5-4a12-8a9c-4000af95c794" />
<br />
Fill in the User information. Do not get too complicated with the logon name, if you are a smaller company maybe use wfisher or if you’re larger and worry about people sharing first initial and last names maybe use william.fisher. Now click Next:
<br />
<img width="975" height="656" alt="image" src="https://github.com/user-attachments/assets/55399929-94c2-4ec2-b9fc-9f25e42a33b4" />
<br />
Now you create William’s password, this needs to meet the minimum criteria for password creation but doesn’t need to be too complicated. We are going to checkmark User must change password at next logon so William will be able to create his own password that he will more easily remember. Select Next then Finish. I will repeat this step so there will be a total of 6 employees: <br/>
<img width="738" height="641" alt="image" src="https://github.com/user-attachments/assets/d5a16716-288d-4768-8120-74c68e1d8d06" />
<br />
Now we are going to assign these users we created into Groups. Right click on the user and select Add to a group: <br/>
<img width="975" height="680" alt="image" src="https://github.com/user-attachments/assets/512eb499-a4f0-48ad-b362-10a73670d6ed" />
<br />
You will have to type the group you wish to add the user to in the Enter the object names to select field and click OK. Now repeat this step with every User: <br/>
<img width="975" height="685" alt="image" src="https://github.com/user-attachments/assets/e33ee9a8-1dc2-4b7a-84a1-e3ed1e080ab2" />
<br />
To make sure that the Users were added to the group successfully double click on the department and select the members tab:  <br/>
<img width="975" height="642" alt="image" src="https://github.com/user-attachments/assets/5fc02189-bb5a-42e6-be52-f7d287bbaf9c" />
<br />
Now lets double check everything in Command Prompt. Type cmd in your bottom search bar and open the application: <br/>
<img width="975" height="914" alt="image" src="https://github.com/user-attachments/assets/dcb2372f-4655-4fcf-8a69-308cc02c1a52" />
<br />
To view all of our OUs type dsquery ou. You will see our new Employees OU listed:  <br/>
<img width="975" height="141" alt="image" src="https://github.com/user-attachments/assets/31f5dd19-7f23-4e9b-9187-d33086f336dc" />
<br />
Next, we want to view all our groups. Type net group /domain to view every group. As you can see, our Accounting, IT and Sales departments are listed: <br/>
<img width="975" height="501" alt="image" src="https://github.com/user-attachments/assets/9cd462ee-011d-40ae-bb81-04f2f50adab9" />
<br />
Lastly, we want to check our users. Type net user /domain to view all users on the domain. If you want to view users within a specific group, type net group “IT Department” /domain:  <br/>
<img width="975" height="360" alt="image" src="https://github.com/user-attachments/assets/ccd443bd-e342-494a-a2b0-e7886b96e8a1" />
</p>

<h2>Importance of Creating Organizational Units, Groups, and Users in AD DS</h2>
<p>Creating Organizational Units (OUs), security groups, and user accounts in Active Directory Domain Services (AD DS) is essential for organizing and managing network resources within a Windows domain. OUs provide a logical structure for managing users and applying administrative policies, while security groups simplify permission management by allowing administrators to assign access rights to multiple users at once. Properly creating and organizing these Active Directory objects improves administrative efficiency, enhances security, and supports centralized user and resource management. Following a standardized process helps ensure consistency, reduces configuration errors, and establishes a well-organized Active Directory environment that is easier to manage and maintain.</p>
