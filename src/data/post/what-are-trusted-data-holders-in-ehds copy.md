---
publishDate: 2025-05-11T00:00:00Z
author: Yves Thorrez
title: What is the Difference between Trusted Data Holders and Health Data Intermediation Entities?
excerpt: ...
image: https://images.unsplash.com/photo-1516996087931-5ae405802f9f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80
category: Tutorials
tags:
  - astro
  - tailwind css
metadata:
  canonical: https://astrowind.vercel.app/get-started-website-with-astro-tailwind-css
---

### EHDS labels in a nutshell

| Feature | **Trusted health data holder** | **Health-data intermediation entity** |
|---------|--------------------------------|--------------------------------------|
| **Legal basis** | Article 72 EHDS | Recital (59)–(60) + Art. 50 §3 (“duties fulfilled by intermediation entities”) |
| **Who designates it?** | Member-State authority, **per individual data-holder** | Member-State law may assign whole *categories* of data-holders to one intermediation entity |
| **Scope of data** | *Own* datasets only (one hospital, one registry, etc.) | May act for **many heterogeneous data-holders** (e.g. all public hospitals < 300 beds) |
| **May assess access requests?** | **Yes.** It reviews the application, then sends a recommendation to the HDAB; HDAB still grants/refuses the permit. citeturn7view0 | **No.** All requests are handled by the HDAB; the entity just prepares / transmits data. |
| **Secure Processing Environment (SPE)** | **Must run an SPE** that meets Art. 73 requirements. This is a *pre-condition* for designation. | **Does not host an SPE**. Access is delivered through the **HDAB’s** SPE (or, in a multi-country case, the Commission’s). |
| **Simplified workflow** | *Yes* – if the request involves only this holder, the HDAB can forward the file straight to it (no multi-holder consolidation). | *No* – standard Chapter IV timelines apply. |
| **Segregation of functions** | Same organisation both prepares data **and** hosts the SPE; still under HDAB permit. | Preparation and hosting are separated: the entity prepares and uploads, the HDAB hosts. |
| **Can it also be the other?** | A trusted holder cannot be an intermediation entity for others. | Intermediation entities **may not be designated** as trusted holders. |

---

### Why an intermediation entity does **not** run an SPE

Recital 77 makes clear that SPEs are provided **only by HDABs or trusted holders**. 
The policy idea is **segregation of powers**:

* the body that grants permits (HDAB) or the single trusted holder that owns the data environment controls live access;  
* any “proxy” that merely collects/cleans data for many hospitals should **not** also control the compute environment, to avoid conflicts of interest and consolidate security certification in one place.

---

## Positioning your platform

### Option A — support **trusted-holder** hospitals  
*Each hospital that onboards could pursue designation as a trusted health data holder.*  
Your platform would:

1. Provide and operate an Art. 73-compliant SPE for each hospital.  
2. Offer the case-management workflow & catalogue that prove “necessary expertise”.  
3. Expose the hospital’s datasets under its own entry in the national catalogue.  
4. Receive forwarded applications from the HDAB, assess them, upload prepared data into the local SPE, and let users in.

**Pros:**  
- Shorter turnaround for “single-holder” requests.  
- Full control of security stack remains with the hospital (good for sensitive cohorts).

**Cons:**  
- Each hospital must pass the designation audit individually; ongoing reviews apply.  
- You cannot merge datasets from several holders inside one SPE.

### Option B — act as a **health-data intermediation entity**  
Your company (or a consortium) is appointed in national law to perform Chapter IV duties *for a class of hospitals*.

Your platform would:

1. Harvest / harmonise data from member hospitals.  
2. Register the combined datasets in the EHDS catalogue *on the hospitals’ behalf*.  
3. Hand the prepared extracts to the **HDAB**, which then loads them into its own SPE for users.

**Pros:**  
- Hospitals off-load the Chapter IV admin burden to you (big selling point).  
- One designation covers many hospitals; easier onboarding.  
- No need to certify an SPE—lower up-front cost.

**Cons:**  
- No “simplified” permit pathway; HDAB timelines still apply.  
- Users work in the HDAB’s environment, so advanced tools must be whitelisted there.  
- Revenue comes from cost-recovery fees set by the HDAB, not from direct SPE services.

### Option C — **hybrid**

Operate as an intermediation entity **and** sell your SPE as a managed service to hospitals that want trusted-holder status.  Legally the SPE then belongs to *those* hospitals; you host it under a processor contract.  This keeps you within the letter of Recital 244 (the intermediation entity itself is not the trusted holder).

---

## Decision checklist

| Question | If answer is *Yes* → lean towards |
|----------|-----------------------------------|
| Do target hospitals insist on keeping data inside their perimeter? | **Trusted-holder** model |
| Is there political appetite to delegate HDAB-level admin work to a central service? | **Intermediation entity** |
| Will you invest in ISO 27001/27701 + future EHDS SPE certification? | Trusted-holder / hybrid |
| Is fast, single-holder turnaround a competitive edge for your research users? | Trusted-holder |
| Do you want one legal umbrella for many small hospitals? | Intermediation entity |

---

### Bottom line

*   A **trusted health data holder** is a single, expert data-holder that runs its **own SPE** and handles first-line permit assessment.  
*   A **health-data intermediation entity** is an outsourcing vehicle that can do the heavy lifting for many data-holders **but must let the HDAB host the SPE**.  
*   The SPE exclusion is not accidental; it enforces a clear separation between data preparation and controlled compute access.  
*   Your platform can fit either role: decide whether you want to manage the SPE yourself (trusted-holder path) or focus on aggregation and case management while the national HDAB provides the compute layer (intermediation path).