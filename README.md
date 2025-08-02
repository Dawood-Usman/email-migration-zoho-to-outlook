# email-migration-zoho-to-outlook

First, inform all your employees / Zoho users to:
 - enable IMAP in Zoho Mail settings [https://www.zoho.com/mail/help/imap-access.html]
 - create a Zoho app password (will be used later in the migration process) [https://t.ly/C5S3e]

Now you need to set up MS Office for your company:
 - buy an MS Office subscription
 - set up your domain (add & verify DNS records)
 - create all your employees/users accounts on Microsoft 365 with your company domain (e.g huzaifa@crumble.com)

1. Now open the Exchange Admin Center from the MS365 admin panel.
2. Click on Migrations in the side panel.
3. Click on Add migration batch: </br></br>
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/f96625c3-6865-4463-aaa7-26919c637c1e" /></br>

**1: Migration path**
 - Give the migration batch a unique name (crumble-migration)
 - select Migration to Exchange Online </br></br>
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/e1838e87-de63-48b3-ac37-0f705436f60e" /></br>

**2: Migration type**
 - Select migration type: IMAP migration </br></br>
<img width="1919" height="909" alt="image" src="https://github.com/user-attachments/assets/bb8268af-6bfc-4208-85fc-615c1f6bc888" /></br>

**3: Prerequisite**
 - Just read & verify the instructions.

**4: Migration endpoint**
 - Click on Create new endpoint. </br></br>
<img width="1919" height="908" alt="image" src="https://github.com/user-attachments/assets/2471bcf2-d98f-4a5e-8364-ea849edf4d55" /></br>

 - Name the migration endpoint (crumble-endpoint) and leave the rest of the settings as they are. </br></br>
<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/1e861e2b-1f05-49ca-815b-928acd1e0453" /> </br>

 - Enter IMAP server details: [https://www.zoho.com/mail/help/imap-access.html]
   - IMAP server: imap.zoho.com
   - Authentication: basic  
   - Encryption: SSL
   - Port: 993 </br></br>
<img width="1919" height="912" alt="image" src="https://github.com/user-attachments/assets/b77271c9-0930-4779-a7f9-e704c7bef338" /></br>

**5: Add users**
 - Now you will see an option to "Download a CSV file with headers only." Click and download that file.
 - Fill that CSV file with the following info of all your employees under the headers carefully:
   - EmailAddress: employee’s Microsoft/Outlook email address
   - UserName: employee’s Zoho email address
   - Password: employee’s Zoho app password
 - Verify the details and import that CSV file.

In the next two steps, (Configuration & Schedule) you can add some filters or schedule migrations, or you can leave the default options.
Save the migration, and it will start syncing the emails from Zoho.

It can cause issues for individual employees only if you misconfigured their details, but you’ll be notified specifically about the issue.
Create another migration batch and upload a CSV file with only the corrected info for those employees whose migration failed previously due to misconfigured details.
