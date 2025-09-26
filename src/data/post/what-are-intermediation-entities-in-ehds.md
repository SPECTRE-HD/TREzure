---
publishDate: 2025-05-11T00:00:00Z
author: Yves Thorrez
title: What are Health Data Intermediation Entities?
excerpt: Health data intermediation entities are a tool to reduce the administrative burden on health data holders.
image: https://images.unsplash.com/photo-1516996087931-5ae405802f9f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80
category: Tutorials
tags:
  - astro
  - tailwind css
metadata:
  canonical: https://astrowind.vercel.app/get-started-website-with-astro-tailwind-css
---

Member States can designate such health data intermediation entities to take over specific responsibilities of health data holders, particularly in managing data access requests. 
This helps reduce the administrative burden on individual data holders by centralising the process through a single intermediary. 
For instance, a Member State might designate a public sector body managing a centralised electronic patient file as a health data intermediation entity. 
Member States can designate multiple health data intermediation entities. 
Such entities would then interface with the Health Data Access Body (HDAB) on behalf of various hospitals and other healthcare providers (or other health data holders, as the case may be), ensuring streamlined data access while maintaining compliance with all regulatory requirements.
Data made available via a health data intermediation entity is still considered as originating from several health data holders. 
This means that it is not possible for such entities to be designated as trusted health data holders. 
Data made available via health data intermediation entities will always go through the normal application process at the HDAB.
Note that while data intermediation services under Chapter III of the Data Governance Act have a similar name, their tasks are very different. Those services primarily serve to facilitate voluntary data sharing in a business-to-business context.

### “Health data intermediation entities” — at a glance  

A **health-data intermediation entity** is a legal person that a Member State may designate to **take over some or all of the statutory duties of numerous individual health-data holders for the _secondary_ use chapter of the European Health Data Space (EHDS).**  
Its creation is optional and aimed at cutting the red tape that would otherwise fall on every single hospital, registry, research institute or company. citeturn8view0

---

#### Key characteristics  

| Aspect | What the Regulation says |
|--------|-------------------------|
| **Legal form** | Must be a *legal person* (public, not-for-profit or private) able to “process, make available, register, provide, restrict access to and exchange electronic health data for secondary use”. citeturn8view0 |
| **Designation** | Done in national law; a Member State may appoint several such entities. citeturn10view0 |
| **Scope of tasks** | Can fulfil any duties that Chapter IV lays on the original data holders—for example: compiling dataset descriptions, answering Health Data Access Body (HDAB) queries, preparing or pseudonymising data, and operating (or arranging) the secure processing environment. |
| **Interface with HDAB** | Acts as the single counterpart for permit requests; still goes through the normal HDAB procedure (no fast track). citeturn10view0 |
| **Relationship to other EHDS actors** | • **Not** the data controller for GDPR purposes—the underlying hospitals, labs, etc. remain controllers.<br>• **Cannot** be declared a “trusted health data holder”; that status is reserved for expert organisations that keep full control of their own data only. citeturn8view0turn10view0 |
| **Different from DGA intermediation services** | The similarly named “data intermediation service” under the Data Governance Act is a voluntary B2B marketplace; the EHDS entity is a regulatory construct that carries statutory obligations. citeturn10view0 |

---

#### Why a Member State might create one

* **Administrative relief** Hospitals and small registries hand off paperwork and permit logistics to a central expert body.  
* **Consistency & quality** One team applies uniform pseudonymisation and FAIR-data standards.  
* **Economies of scale** Shared secure-processing infrastructure can be cheaper and more robust than dozens of separate setups.

---

#### Typical examples

- A national e-health agency that already hosts a central electronic patient file could be empowered to act for all public hospitals.  
- A university-led biobank consortium might be appointed to handle secondary-use requests for multiple regional biobanks.

---

**In short:** a health-data intermediation entity is a Member-State-appointed “one-stop shop” that performs the Chapter IV obligations of many data holders—making life easier for hospitals while keeping all the EHDS privacy, security and permit safeguards intact.