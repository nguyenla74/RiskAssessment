<h1>Risk Assessment Project</h1>

<h2>DESCRIPTION</h2>
The project is a “structured walkthrough” penetration test of a fictional company, Artemis, Incorporated (“Artemis”). A structured walkthrough is an organized procedure for a group of peers to review and discuss the technical aspects of various IT, IT Security, and IT Audit work products. The major objectives of a structured walkthrough are to find errors and to improve the quality of the product or service to be delivered.
<br />

<h2>UTILITIES USED</h2>

<p align="center">
<b>Nmap<br/></b>
<img src="https://i.imgur.com/3DWeAM5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
<b>Nessus<br/></b>
<img src="https://i.imgur.com/Y8eoYQb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
<b>OSINT Framework<br/></b>
<img src="https://i.imgur.com/ZwRXTJE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
<p align="center">
<b>CVSS v3.1 Calculator<br/></b>
<img src="https://i.imgur.com/kODaHeH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>I. SCOPE OF WORK</h2>

<b>1. Network Infrastructure:</b>
- Cisco, Fortinet, and Palo Alto firewalls
- F5 (Big IP) for load balancing
- Zscaler for secure remote application access
- SD-WAN and MPLS links
- Transition from Cisco to Fortigate devices
- On-premise servers and applications in Houston, Paris, Cairo, and Singapore
- Cloud-based assets on Amazon Web Services (AWS)

<b>2. Server and Application Environment:</b>
- On-premise servers running Linux and Oracle 12c
- SAP, the primary ERP system
- Exchange Online (via Office 365) and on-prem Microsoft Exchange servers
- PARS system for patent-related technical information
- APOLLO system for trade secrets, especially manufacturing processes

<b>3. Authentication and Access Control:</b>
- Single Sign-On (SSO) solution leveraging Microsoft Active Directory
- Assess the security of user authentication, authorization, and access control mechanisms

<b>4. Communication Systems:</b>
- Email systems including Exchange Online and on-premise Microsoft Exchange
- Evaluate security measures for email communications

<h2>II. PROJECT OBJECTIVES:</h2>

- Conduct a comprehensive penetration test to identify and assess vulnerabilities in the network infrastructure, servers, and applications at Artemis.
- Prioritize vulnerabilities based on their severity, potential impact, and exploitability.
- Provide detailed recommendations and remediation strategies to mitigate identified vulnerabilities effectively.

<h2>III. ASSUMPTIONS:</h2>

- The assessment will be conducted during specified maintenance windows to minimize impact on production environments.
- Non-Disclosure Agreement and rules of engagement has been signed
- Artemis understands that the vulnerability assessment is a controlled and authorized activity, and no retaliatory measures will be taken against the testing team.

<h2>IV. TIMELINE:</h2>

<body>
    <table border="1">
        <tr>
            <th>Vulnerability Assessment</th>
            <th>Start Date</th>
            <th>End Date</th>
        </tr>
        <tr>
            <td>Reconnaissance</td>
            <td>01/01/2024</td>
            <td>01/15/2024</td>
        </tr>
        <tr>
            <td>Vulnerability Scanning</td>
            <td>01/16/2024</td>
            <td>01/23/2024</td>
        </tr>
        <tr>
            <td>Reporting</td>
            <td>01/24/2024</td>
            <td>02/07/2024</td>
        </tr>
    </table>
<b>Table 1. Vulnerability Assessment Timeline</b>
</body>
</html>

<h2>V. SUMMARY OF FINDINGS</h2>

<p align="center">
<img src="https://i.imgur.com/itGIoZU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

After using Nmap as the main tool for network scanning and Nessus for vulnerability scanning, the results of 9 vulnerabilities in Artemis’s system are the following:

<b>1. Unpatched RDP Exposed to the Internet:</b>

- Exposure: RDP is accessible from the internet without the latest security patches.
- Potential Impact: Unauthorized access, data theft, or compromise of the system due to exploitation of known vulnerabilities in RDP.
- Threat Level: High

<b>2. Web Application Vulnerable to SQL Injection:</b>

- Exposure: Attackers can manipulate SQL queries through user inputs, potentially gaining unauthorized access to the database.
- Potential Impact: Data theft, unauthorized access to sensitive information, and potential manipulation of the application's database.
- Threat Level: Critical

<b>3. Default Password on Cisco Admin Portal:</b>

- Exposure: Default credentials pose a significant security risk as they are easily exploitable.
- Potential Impact: Unauthorized access to critical network infrastructure, potential for unauthorized configuration changes, and network compromise.
- Threat Level: Medium

<b>4. Apache Web Server Vulnerable to CVE-2019-0211:</b>

- Exposure: The server is susceptible to this specific security vulnerability, possibly allowing remote code execution.
- Potential Impact: Remote attackers could exploit this vulnerability to execute arbitrary code on the server, leading to potential system compromise.
- Threat Level: High

<b>5. Web Server Exposing Sensitive Data:</b>

- Exposure: Critical data is accessible without proper access controls, leading to potential data leaks.
- Potential Impact: Unauthorized access to sensitive information, potential compliance violations, and reputational damage.
- Threat Level: High

<b>6. Web Application with Broken Access Control:</b>

- Exposure: Users may have unauthorized access to resources or perform actions beyond their intended privileges.
- Potential Impact: Unauthorized data access, modification, or disruption of application functionality.
- Threat Level: High

<b>7. Oracle WebLogic Server Vulnerable to CVE-2020-14882:</b>

- Exposure: The server is susceptible to a specific security vulnerability that could allow unauthenticated remote code execution.
- Potential Impact: Remote attackers could exploit this vulnerability to execute arbitrary code on the server, leading to potential system compromise.
- Threat Level: High

<b>8. Misconfigured Cloud Storage (AWS):</b>

- Exposure: Cloud storage is not properly configured, potentially allowing unauthorized access.
- Potential Impact: Unauthorized access to sensitive data, potential data breaches, and compliance issues.
- Threat Level: High

<b>9. Microsoft Exchange Server Vulnerable to CVE-2021-26855:</b>

- Exposure: The server is susceptible to a specific security vulnerability, possibly leading to unauthorized access or data manipulation.
- Potential Impact: Remote attackers could exploit this vulnerability to compromise the Exchange Server, leading to potential data theft or disruption of email services
- Threat Level: Medium

<h2>VI. RECOMMENDATIONS:</h2>

<b>1. Unpatched RDP Exposed to the Internet:</b>

- Immediately apply the latest security patches for the RDP service.
- Restrict RDP access to only trusted IP addresses using firewalls or Network Security Groups.
- Implement strong, unique passwords for RDP accounts.

<b>2. Web Application Vulnerable to SQL Injection:</b>

- Implement input validation and parameterized queries to prevent SQL injection attacks.
- Regularly conduct code reviews and security assessments of the web application.
- Employ a web application firewall (WAF) to detect and mitigate SQL injection attempts.

<b>3. Default Password on Cisco Admin Portal:</b>

- Change default passwords immediately to strong, unique credentials.
- Implement multi-factor authentication (MFA) for the admin portal.
- Regularly update and patch network equipment firmware.

<b>4. Apache Web Server Vulnerable to CVE-2019-0211:</b>

- Apply the latest patches and updates for Apache to address the CVE-2019-0211 vulnerability.
- Continuously monitor for security advisories related to Apache.
- Consider configuring web application firewall (WAF) to detect and block potential exploits.

<b>5. Web Server Exposing Sensitive Data:</b>

- Review and update access controls on the web server to restrict access to sensitive data.
- Encrypt sensitive data both in transit and at rest.
- Regularly conduct security audits to identify and address data exposure risks.

<b>6. Web Application with Broken Access Control:</b>

- Implement proper access controls within the web application.
- Conduct regular security assessments to identify and remediate access control issues.
- Enforce the principle of least privilege for user accounts.

<b>7. Oracle WebLogic Server Vulnerable to CVE-2020-14882:</b>

- Apply the latest patches and updates for Oracle WebLogic Server to address CVE-2020-14882.
- Monitor for security advisories related to Oracle WebLogic Server.
- Configure firewalls to restrict access to the WebLogic Server.

<b>8. Misconfigured Cloud Storage (AWS):</b>

- Review and update AWS security group configurations to follow the principle of least privilege.
- Implement access controls, such as AWS Identity and Access Management (IAM), to restrict unauthorized access.
- Regularly audit and monitor AWS configurations for misconfigurations.

<b>9. Microsoft Exchange Server Vulnerable to CVE-2021-26855:</b>

- Apply the latest patches and updates for Microsoft Exchange Server to address CVE-2021-26855.
- Monitor for security advisories related to Microsoft Exchange Server.
- Conduct an immediate security audit of the Exchange Server.

<h2>VII. METHODOLOGY</h2>

<b>1. Reconnaissance Activities:</b>

- To gather information about Artemis and its technology stack, various reconnaissance activities were conducted. 
- A search on Google <i>(Figure 1)</i> and Bing was performed to identify a dedicated technology page on the company's website, where details about their technology stack might be listed. 
- Technology-related forums like Stack Overflow and Quora were reviewed for discussions about Artemis's technology choices. 
- Annual reports, if available, were sought on annualreports.com for insights into the company's infrastructure and technologies. 
- Website analysis tools like BuiltWith and Wappalyzer were employed to analyze Artemis's website for technology details. 
- Contact information from the company's website, including telephone numbers, was utilized for further inquiry. 
- Email addresses were searched using tools like Hunter.io and Thatsthem.com. Public repositories on GitHub <i>(Figure 2)</i> were checked for any open-source projects revealing the company's tech stack. 
- Social media profiles on LinkedIn <i>(Figure 3)</i>, Facebook, and Twitter, including those of current and former employees, were examined to understand the technologies they have experience with.
- IP location tools like IPlocation.net were consulted to determine the geographical location of Artemis. 
- Lastly, domain search on who.is was performed to gather additional information about the domain, including registration details. 
- Networking events and conferences listed on platforms like Eventbrite and Meetup <i>(Figure 4)</i> were considered for potential insights from industry professionals associated with Artemis. 
- These diverse reconnaissance activities aimed to provide a comprehensive understanding of Artemis's technology environment.

<p align="center">
<img src="https://i.imgur.com/KrMzSKh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/pm32o3d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b>2. Reporting</b>

Based on the results, each vulnerability was put into the CVSS Version 3.1 Calculator in order to calculate the threat level. Exploitability Metrics and Impact Metrics were taken into account to calculate the Base CVSS score, and the results are as follow:

<p align="center">
<img src="https://i.imgur.com/kTvEuRV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/ImTgate.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
