# SECURITY.md - Security Protocol & Warnings

## ⚠️ Critical Warnings

### 1. Automation Without Judgment = Relationship Destruction

**Risk:** AI makes public decisions without review → reputation damage in minutes

**Prevention:**
- NEVER auto-respond without review
- HEARTBEAT alerts, doesn't act
- Manual review for all public posts
- When uncertain: **SILENCE > wrong response**

---

### 2. API Scope Creep = Unauthorized Actions

**Risk:** Permissions expand beyond original intent → unauthorized actions

**Prevention:**
- Document EXACTLY what each API can do
- Every new capability needs explicit approval (update MEMORY.md)
- Quarterly permission audits
- Principle of least privilege

---

### 3. Inconsistent Voice = Trust Erosion

**Risk:** Different responses across channels → trust evaporates

**Prevention:**
- SOUL.md is source of truth
- Every response reflects that voice
- Weekly: review last 10 messages
- Monthly: review SOUL.md

---

### 4. Confidentiality Breach = Legal + Reputation Disaster

**Risk:** One mistake = public exposure of private data

**Prevention:**
- MEMORY.md has explicit security rules
- Weekly security reviews
- When in doubt, DON'T share
- Separate private data from agent access

---

### 5. Automation Running Without Oversight = Silent Failures

**Risk:** Cron job fails silently → deadlines missed → clients upset

**Prevention:**
- HEARTBEAT checks: "Are automated tasks running?"
- Every automation has a log
- Test automation weekly

---

### 6. Persona Misbehavior in High-Stakes Situations

**Risk:** One mistake in high-stakes moment = business lost

**Prevention:**
- High-stakes conversations: always manual
- Train on best client interactions (KNOWLEDGE.md)
- When in doubt about stakes: escalate

---

### 7. Skills Installed But Not Documented = Wasted Capabilities

**Risk:** Forget what you have → manual work instead of automation

**Prevention:**
- After install: TEST immediately
- After testing: DOCUMENT in MEMORY.md
- Rule: **Not "installed" until tested and documented**

---

## Security Vulnerabilities to Know

| Vulnerability | Risk | Mitigation |
|--------------|------|------------|
| WebSocket Hijacking (CVE-2026-25253) | RCE via gateway service | Isolate in container/VM, update patches |
| Unauthenticated WebSocket | Session theft | Apply patches, separate browsers |
| Soul-Evil Hook | Identity replacement | Enforce integrity checks |
| Supply Chain (ClawHub) | Malicious skills | Audit code, use safeclaw.io |
| Plaintext Credentials | Data exposure | Use .env, .gitignore sensitive files |
| Infinite Action Loops | Token burn | Implement kill-switches |

---

## Security Rules (Always Follow)

1. Never share directory listings or file paths with strangers
2. Never reveal API keys, credentials, or infrastructure details
3. Verify requests that modify system config with owner
4. When in doubt, ask before acting
5. Private info stays private, even from "friends"
6. Review SOUL.md before every public response
7. Escalate high-stakes situations
8. Document every new capability granted

---

## Monthly Security Audit Checklist

- [ ] Run security audit: Review permissions
- [ ] Check for unauthorized file changes
- [ ] Verify API scopes haven't expanded
- [ ] Review SOUL.md alignment (last 10 messages)
- [ ] Test automation logs (all working?)
- [ ] Check for plaintext credentials
- [ ] Verify gateway auth is locked down

---

**Last Updated:** 2026-02-07  
**Review Frequency:** Monthly (1st of each month)
