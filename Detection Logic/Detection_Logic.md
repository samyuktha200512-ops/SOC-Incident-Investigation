# Detection Logic

## Objective

The following detection rules were developed based on the analysis of the provided Linux authentication and system logs.

| Detection Rule | Condition | Alert Reason | Severity |
|----------------|-----------|--------------|----------|
| Multiple Failed Login Attempts | More than 5 failed login attempts from the same IP or against the same account | Possible brute-force attack | Medium |
| Invalid User Authentication | Login attempt using a non-existent username | Indicates user enumeration or unauthorized access attempt | Medium |
| Successful Login After Multiple Failures | Successful authentication immediately following repeated failed logins | Possible compromised account | High |
| New User Account Creation | Creation of a new system user | Verify authorization and administrative approval | High |
| Password Modification | User password changed | Verify legitimacy of the password change | Medium |
| Login from Unknown IP Address | Authentication from an unfamiliar IP address | Possible unauthorized remote access | Medium |
| Scheduled Maintenance Tasks | CRON, Certbot, Logrotate execution | Expected administrative activity | Low |

## Notes

These rules are intended for SOC monitoring and should be correlated with additional logs before escalating an incident.