# Qualys Vulnerability Management HomeLab
<h2>Description</h2>
This is my first home lab project in existence. I will be using Windows 10 on a virtual machine. I will install a deprecated version of Mozilla Firefox and VLC media player and use a Qualys Virtual Scanner Appliance on the Qualys Cloud Platform to scan the environment for vulnerabilities to test the scanner. The firewall will be disabled in the beginning and will be reenabled when I attempt to remediate the vulnerabilities. The first scan will be a basic scan with no credentials. The second scan will use credentials so I can compare the difference between a non-credential scan and a credential scan. After I complete the credential scan, I will review the results then remediate these vulnerabilities and verify that these vulnerabilities are removed.
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

With this basic scan, I was only able to find 20 vulnerabilities with a risk score of 2 out of 5.  This scan is not accurate due to no credentials. To get a more accurate report, I need to add credentials to the next scan.


<B>Credential Scan:</b>
<br/>

  <img src="https://i.imgur.com/81pU1fo.png" height="90%" width="90%">

With a credential scan, the results were more accurate. A total 258 vulnerabilities were found with a maximum risk score of 5 out of 5. 

89 Vulnerabilities were confirmed with 5 vulnerabilities with a severity of 5.

Just as intended, Firefox and VLC media player vulnerabilities were found. Not only that, Windows 10 needed to be patched, along with many other issues.

To remediate these vulnerabilities I can either update or delete these applications. In this case, I will delete the deprecated applications and update Windows 10 and scan again to verify that these vulnerabilities are remediated. The firewall will also be turned on since it was turned off at the beginning.


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
  
I removed 4 more confirmed vulnerabilities and reduced the average risk score from 4 to 3. This concludes the home lab Qualys project.

