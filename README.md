# splunk-linux-authentication-investigation
SOC-style investigation of Linux SSH authentication logs using Splunk SPL transforming commands to analyze authentication activity, source IP addresses, and event trends.


Splunk Linux Authentication Investigation:

Overview
This project demonstrates a SOC-style investigation of Linux SSH authentication logs using Splunk Enterprise and Search Processing Language (SPL).

The objective was to analyze authentication activity, identify source IP addresses generating login attempts, and utilize transforming commands to convert thousands of raw events into actionable security insights.

Scenario
A SOC analyst was tasked with reviewing Linux authentication logs collected from a Linux server.

The goal of the investigation was to:

Review SSH authentication activity
Analyze login attempts within the dataset
Identify source IP addresses responsible for authentication events
Aggregate log data using SPL transforming commands
Develop familiarity with SIEM-based investigations
Environment
Component	Details
SIEM	Splunk Enterprise 10.6.0.5
Index	mydfir-lab1
Sourcetype	Linux:auth
Data Source	Linux Authentication Logs
Investigation Type	Authentication Analysis
Analyst	Adam Hunter
Skills Demonstrated
Splunk Enterprise
SPL (Search Processing Language)
SIEM Investigation
Log Analysis
Linux Authentication Analysis
Source IP Analysis
Security Monitoring
Cybersecurity Reporting
Investigation 1: Authentication Events by Host
Objective
Determine how authentication events can be summarized using transforming commands rather than manually reviewing individual log entries.

SPL Query
index=mydfir-lab1 sourcetype="Linux:auth"
| stats by host
Findings
Processed 3,676 Linux authentication events.
Utilized the stats transforming command to aggregate authentication activity.
Demonstrated how Splunk can summarize large datasets into analyst-friendly results.
Confirmed successful indexing of Linux authentication logs.
Screenshot
Authentication Events by Host

Investigation 2: Source IP Analysis
Objective
Identify source IP addresses responsible for authentication activity within the dataset.

SPL Query
index=mydfir-lab1 sourcetype="Linux:auth"
| top src_ip
Findings
Analyzed source IP addresses generating authentication activity.
Observed SSH login attempts involving the root account.
Identified authentication failure events within the log dataset.
Demonstrated how SPL can rapidly identify systems responsible for large volumes of authentication activity.
Screenshot
Top Source IP Analysis

Investigation Summary
This investigation focused on reviewing Linux SSH authentication events within Splunk Enterprise.

Using SPL transforming commands such as stats and top, thousands of raw events were transformed into meaningful information that could assist a security analyst during triage and investigation activities.

Key security analysis tasks included:

Reviewing authentication activity
Examining source IP addresses
Investigating login attempts
Analyzing authentication failures
Aggregating event data for faster analysis
Key Takeaways
✅ Worked with Linux authentication logs in Splunk Enterprise

✅ Used SPL transforming commands to analyze authentication activity

✅ Identified source IP addresses involved in SSH login attempts

✅ Reviewed authentication failures and root account activity

✅ Practiced SOC analyst investigation workflows

Conclusion
This project provided hands-on experience using Splunk Enterprise to investigate Linux SSH authentication logs.

The investigation demonstrated how SIEM platforms and SPL transforming commands can be used to efficiently summarize large datasets, identify authentication trends, and support day-to-day SOC operations.

Author:

Adam Hunter

Aspiring SOC Analyst

GitHub: https://github.com/adam-hunter-6703
