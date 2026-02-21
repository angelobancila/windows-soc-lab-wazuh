# Project 02 – Windows Authentication Attack Detection & SOC Alert Triage

## Objective

To simulate and investigate a brute force authentication attack scenario using Windows Security Event logs and perform Tier 1 SOC triage within Wazuh SIEM.

---

## Attack Simulation

Multiple failed authentication attempts were generated against a local Windows account to simulate a potential brute force attack.

The objective was to validate detection capability, analyse event patterns, and determine whether the activity indicated malicious intent or user error.

---

## Detection & Analysis

The following Windows Security Event IDs were analysed:

- 4625 – Failed logon attempts  
- 4740 – Account lockout  
- 4624 – Successful logon (post-failure verification)

Observed behaviour included:

- Repeated failed logon attempts within a short timeframe  
- Account lockout triggered after threshold exceeded  
- No successful authentication from the same source following the failures  

Analysis steps included:

- Reviewing source IP address (private lab range)  
- Identifying Logon Type  
- Checking failure reason codes  
- Correlating timestamps to assess attack velocity  

---

## Investigation Workflow

1. Identified repeated 4625 events in Wazuh.
2. Correlated timestamps to determine frequency and pattern.
3. Confirmed account lockout event (4740).
4. Checked for any subsequent successful 4624 logon from the same source.
5. Assessed severity based on potential credential compromise risk.

---

## Outcome

The activity was classified as a simulated brute force authentication attempt resulting in account lockout, with no evidence of successful credential compromise.

This investigation demonstrated structured Tier 1 SOC triage, authentication event correlation, and incident classification capability.
