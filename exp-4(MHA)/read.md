# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<br>
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/MH%201.png?raw=true" width="800" alt="Mail Header Screenshot" />



<br>
<br>


- Select all the text in the header and copy it.

<br>
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/MH%204.png?raw=true" width="800" alt="Mail Header Screenshot" />


<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>

  <img width="1918" height="868" alt="Screenshot 2025-09-01 220401" src="https://github.com/user-attachments/assets/dae904d6-1eba-450d-968e-facacf4b0b93" />

<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/MH%206.png?raw=true" width="800" alt="MH 6 Screenshot" />


### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>
<img src="https://github.com/Harini-Kannan1802/image/blob/0c208522e4e401df1c3954a5b57200e77d51f0d7/MH%208.png?raw=true" width="800" alt="MH 8 Screenshot" />

<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="1817" height="864" alt="Screenshot 2025-09-01 220659" src="https://github.com/user-attachments/assets/340b4075-857a-4caf-b211-db5312a6af79" />

<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1885" height="786" alt="image" src="https://github.com/user-attachments/assets/c1d13cf5-5ccf-4e59-8ca2-7a252dc37c77" />
