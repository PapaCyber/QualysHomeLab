# Qualys Vulnerability Management HomeLab
 ### [Video Demonstration](https://www.loom.com/share/60a8d19134794321ae40ea8c001a5337?sid=8b2610fa-5cb1-420e-b749-c78f318be88e)
<h2>Description</h2>
This is my first home lab project in existence. In this project, I used a Qualys Virtual Scanner appliance on the Qualys Cloud Platform to scan for vulnerabilities on a Windows 10 virtual machine, using Oracle VM Virtual Box. I purposely installed outdated versions of VLC and Firefox to test if the Qualys scanner could pick up those vulnerabilities. To begin the process I started off with a non-credential scan and finished it off with a credential scan to show the difference in results. After scanning the environment with credentials I began to remediate the vulnerabilities by uninstalling VLC and Firefox. Finally, I performed another scan to verify my results. 

<b>FYI, The video results are different from the results at the bottom of this page because I did a test run of the scanner and patched Windows 10 before recording the recent results.</b>

<h2>Software & Applications Used</h2>

- <b>Oracle VM VirtualBox</b> (7.0)
- <b>Qualys Community Edition</b>
- <b>Qualys Virtual Appliannce</b>
- <b>VLC</b> (v1.1.1)
- <b>Mozilla Firefox</b> (104.0b7)
<h2>Environments Used </h2>

- <b>Windows 10</b> (22H2)

<h2>Results:</h2>

<B>Basic Scan (No Credentials):</b>

<br/>

  <img src="https://i.imgur.com/i48m4al.png" height="90%" width="90%"/>

With this basic scan, I was only able to find 20 vulnerabilities, 1 of which was confirmed with a risk score of 2 out of 5.  This scan is not accurate due to no credentials. To get a more accurate report, I need to add credentials to the next scan.


<B>Credential Scan:</b>
<br/>

  <img src="https://i.imgur.com/81pU1fo.png" height="90%" width="90%">

With a credential scan, the results were more accurate. A total 258 vulnerabilities were found with a maximum risk score of 5 out of 5. 

89 Vulnerabilities were confirmed with 5 vulnerabilities with a severity of 5.

Just as intended, Firefox and VLC media player vulnerabilities were found. Not only that, Windows 10 needed to be patched, along with many other issues.

To remediate these vulnerabilities I can either update or delete these applications. In this case, I will delete the deprecated applications and update Windows 10 and scan again to verify that these vulnerabilities are remediated. 


<B>Credential Scan After Remediation:</b>
<br/>

  <img src="https://i.imgur.com/A9ML61J.png" height="90%" width="90%">
  
After this scan, 89 confirmed vulnerabilities were reduced by a whopping 91% with 8 confirmed vulnerabilities left.

I am not satisfied with the results since the average security risk is still 4 out of 5. 

I will remediate more vulnerabilities to reduce the security risk and rescan.
<br />

<B>Credential Scan After Remediation Part 2:</b>
<br/>

  <img src="https://i.imgur.com/823YuzL.png" height="90%" width="90%">
  
I removed 4 more confirmed vulnerabilities by following the solutions from the CVE report and reduced the average risk score from 4 to 3. This concludes the home lab Qualys project.

