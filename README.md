                                                        Basic Vulnerability Scan
The objective of this task was to use a free vulnerability scanning tool, 

Nessus Essentials, to identify common vulnerabilities on a local machine (PC).   

Implementation and Results


Tool Setup: Nessus Essentials was installed and configured, including the crucial step of downloading and initializing its plugins.   


Scan Configuration: A new scan was configured, named 'patch_finder'.   


Scan Target: The local machine's IP address (e.g., 172.16.xx.xxx) was set as the target.   



Policy: Basic Network Scan was selected for a general vulnerability assessment.   



Scan Execution: The scan ran for 17 minutes (from 7:25 PM to 7:42 PM) and was completed.   

Vulnerability Findings
The completed scan found a total of 

23 vulnerabilities.The severity was predominantly    

"Info", but the overall results included a group with a "Mixed" severity, which contained the most severe finding.   

Key Vulnerability Groups:

Netstat Portscanner (SSH): 30 counts.   

SMB (Multiple Issues): 6 counts.   

SSL (Multiple Issues): 4 counts, including the most severe issue found.   



Most Severe Finding: The most severe individual finding was a MEDIUM-rated issue within the SSL (Multiple Issues) group, titled "SSL Certificate Cannot Be Trusted".   



Risk Factor/Score: Medium, with a CVSS v3.0 Base Score of 6.5.   



Root Cause: The untrusted status can be caused by a broken certificate chain (e.g., self-signed or missing intermediate certificates), an invalid certificate date, or a bad/unverified signature.   


Solution: The recommended solution is to "Purchase or generate a proper SSL certificate for this service".
