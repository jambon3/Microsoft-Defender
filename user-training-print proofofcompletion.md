Microsoft Defender for Office 365 Attack Simulation Training does not natively generate a printable certificate of completion for users. It tracks training completion, due dates, and reporting metrics, but there is no built-in "Certificate PDF" feature.

### Option 1: Automatic Certificate via Power Automate (Recommended)

When a user completes training:

Export or retrieve training completion data from Microsoft Defender reporting.
Use Power Automate to detect completed training.
Generate a PDF certificate using:
Word template + Power Automate
SharePoint document template
Adobe PDF services (optional)
Email the certificate automatically to the user.

Certificate example:



### Option 2: Send a Completion Email Instead


Simpler and often sufficient for compliance.

Subject: Cyber Security Training Completed

<strong>${firstName} ${lastName},</strong>

<p>
Congratulations! You have successfully completed your assigned Cyber Security Awareness Training.
</p>

<p>
Your completion has been recorded and no further action is required.
</p>

<p>
Completion Date: <strong>${CompletionDate}</strong><br>
Training Campaign: <strong>${CampaignName}</strong>
</p>

<p>
Thank you for helping keep iCompany secure.
</p>

<p>
Regards,<br>
<strong>Cyber Security Team</strong><br>
iCompany
</p>