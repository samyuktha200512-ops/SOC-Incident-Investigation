# Incident Classification

| Incident | Severity | Potential Impact | Recommended Response |
|----------|----------|------------------|----------------------|
| Failed Login Attempts | Medium | Password guessing or brute-force activity | Monitor, investigate source IP, block if excessive |
| Invalid User Attempts | Medium | Username enumeration | Monitor and investigate repeated attempts |
| Successful Login After Failed Attempts | High | Possible account compromise | Reset password, verify user activity, escalate |
| New User Creation | High | Potential persistence mechanism | Verify authorization, remove unauthorized accounts |
| Password Change | Medium | Possible unauthorized credential modification | Confirm with account owner |
| CRON Jobs | Low | Normal system operation | No action required |
| Certbot Renewal | Low | Routine certificate maintenance | No action required |
| Logrotate Execution | Low | Routine log management | No action required |