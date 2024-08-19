# 0x19-postmortem task

![Technical Issue Resolution](./photo_2024-08-18_22-25-00.jpg)
# Issue Summary:
- **Duration**: The outage occurred on June 15, 2023, from 9:00 AM to 1:00 PM (PST).
- **Impact**: The customer login/authentication service was down, causing a 30% increase in overall customer support calls due to login failures.
- **Root Cause**: An unforeseen database connection limit was reached due to increased traffic and a lack of automatic scaling.

# Timeline:
- **Issue Detected**: June 15, 2023, 9:00 AM (PST).
- **Detection Method**: Detected through monitoring alerts on abnormal database response times.
- **Actions Taken**: Investigated database, network connections, and server logs. Initially assumed an issue with network instability.
- **Misleading Paths**: Assumed network issues, leading to unnecessary network diagnostics and configurations.
- **Escalated To**: Incident was escalated to the DevOps and Database Administration teams.
- **Resolution**: Database connection limits were increased, additional servers provisioned, and monitoring thresholds adjusted.

# Root Cause and Resolution:
- **Cause**: Database connection limit reached due to unexpected traffic surge.
- **Resolution**: Increased database connection limits, provisioned additional servers for automatic scaling during peak loads.

# Corrective and Preventative Measures:
- **Improvements**: Implement automatic scaling for critical services, enhance monitoring alerts for database thresholds.
- **Tasks**:
  1. Implement automatic scaling for customer authentication service.
  2. Review and optimize database connection limits based on projected growth.
  3. Enhance monitoring and alerts for critical database thresholds.
  4. Conduct a post-incident review with teams to discuss lessons learned.

**This outage postmortem analyzed a service disruption due to database connection limits, which was promptly resolved by scaling resources and adjusting monitoring thresholds. To prevent future occurrences, measures such as automated scaling and optimized database configurations will be implemented.**
