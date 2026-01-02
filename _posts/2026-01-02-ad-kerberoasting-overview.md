---
layout: post
title: "Active Directory – Kerberoasting (Overview)"
date: 2026-01-02
tags: [ActiveDirectory, RedTeam, Pentest]
---

## Context

This post provides a **high-level overview** of a Kerberoasting attack path in an Active Directory environment, focusing on methodology rather than exploitation details.

---

## Attack overview

Kerberoasting targets service accounts with weak or reusable passwords by requesting Kerberos service tickets and performing offline password cracking.

**High-level steps**
1. Identify SPNs linked to service accounts
2. Request Kerberos service tickets
3. Offline analysis of encrypted tickets
4. Credential reuse opportunities

---

## Defensive considerations

- Use strong, long service account passwords
- Prefer Managed Service Accounts (MSA / gMSA)
- Monitor unusual TGS requests
