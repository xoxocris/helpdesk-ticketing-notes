# Helpdesk Ticketing — Practice Notes & Playbooks 🎫

Documentation from hands-on helpdesk practice using Spiceworks and Service Desk Simulator. Built to develop real ticket lifecycle skills — intake, triage, escalation, resolution, and documentation — the way an actual IT support role operates.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Spiceworks | Ticket creation, assignment, tracking, and resolution logging |
| Service Desk Simulator | Scenario-based helpdesk practice (daily sessions) |

---

## Ticket Lifecycle

```
User Reports Issue
       ↓
Ticket Created — assign priority, category, affected user
       ↓
Triage — reproduce issue, gather info, check known issues
       ↓
Resolve or Escalate — fix if Tier 1 scope, escalate with full notes if not
       ↓
Document Resolution — steps taken, root cause, time to resolve
       ↓
Close & Follow Up
```

---

## Common Issue Playbooks

### 🔒 Account Locked Out
- Verify user identity
- Unlock account in Active Directory (ADUC)
- Check for repeated lockouts (possible credential stuffing or wrong saved password)
- Advise user to clear saved credentials
- Document: user, time, unlock method, advised action

### 🖨️ Printer Not Working
- Confirm printer is online and showing in device list
- Check print queue for stuck jobs — clear if needed
- Remove and re-add printer
- If network printer: ping IP, check port configuration
- Escalate if hardware fault suspected

### 🌐 No Internet / Network Connectivity
- Check physical cable / WiFi connection
- `ipconfig` — verify IP assignment (APIPA = DHCP issue)
- `ping 8.8.8.8` — test external connectivity
- `ping gateway` — isolate to LAN vs. WAN
- Flush DNS: `ipconfig /flushdns`
- Escalate to network team if gateway unreachable

### 💻 Slow Computer
- Check Task Manager — CPU, RAM, disk usage
- Look for runaway processes
- Check startup programs — disable unnecessary entries
- Run disk cleanup / check storage space
- If persistent: escalate for reimaging evaluation

### 📧 Can't Send / Receive Email
- Verify internet connectivity first
- Check Outlook profile is connected (bottom status bar)
- Test webmail access — isolates client vs. server issue
- Check mailbox size / quota
- Escalate to email admin if server-side

---

## Escalation Guidelines

| Situation | Action |
|---|---|
| Issue beyond Tier 1 scope | Escalate with full notes — steps taken, error messages, user impact |
| Security incident suspected | Escalate immediately to security team, do not attempt to resolve |
| Hardware failure confirmed | Ticket to hardware/procurement team |
| Repeated same issue for one user | Flag as pattern, escalate for deeper investigation |

---

## Documentation Standards

Every ticket I close includes:
- **Issue summary** — what the user reported
- **Steps taken** — what I tried and in what order
- **Root cause** — what actually caused it
- **Resolution** — what fixed it
- **Time to resolve** — for tracking SLA awareness

---

## Status

Ongoing — updated as I complete daily simulator sessions and encounter new scenarios.
