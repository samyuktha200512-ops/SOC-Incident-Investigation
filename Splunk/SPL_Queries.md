# Splunk Search Processing Language (SPL) Queries

The following SPL queries were used during the investigation to validate findings from the Linux authentication and system logs.

---

## 1. Display All Imported Events

```spl
index=main
```

Purpose:
Displays all events imported into Splunk.

---

## 2. Count Total Events

```spl
index=main | stats count
```

Purpose:
Verifies that all log events were successfully imported.

---

## 3. Failed Login Attempts

```spl
index=main "Failed password"
```

Purpose:
Detects failed authentication attempts.

---

## 4. Invalid User Login Attempts

```spl
index=main "Invalid user"
```

Purpose:
Identifies login attempts using non-existent usernames.

---

## 5. Successful Password Authentication

```spl
index=main "Accepted password"
```

Purpose:
Displays successful password-based logins.

---

## 6. Successful Public Key Authentication

```spl
index=main "Accepted publickey"
```

Purpose:
Shows successful SSH public key authentication.

---

## 7. CRON Activities

```spl
index=main CRON
```

Purpose:
Displays scheduled system tasks.

---

## 8. Logrotate Execution

```spl
index=main logrotate
```

Purpose:
Verifies routine log rotation activity.

---

## 9. Certbot Renewal

```spl
index=main certbot
```

Purpose:
Verifies scheduled SSL certificate renewal.

---

## 10. User Session Opened

```spl
index=main "session opened"
```

Purpose:
Shows successful user session creation.

---

## 11. User Session Closed

```spl
index=main "session closed"
```

Purpose:
Shows session termination events.

---

## Summary

These SPL queries were used to validate the findings documented in the Incident Response Report and demonstrate practical log analysis using Splunk Enterprise.