### Introduction
This implementation guide is provided to support the use of HL7<sup>&reg;</sup> FHIR<sup>&reg;&copy;</sup> in an Australian context for TBD.

TBD Insert purpose and scope of the General Practitioner National Antimicrobial Prescribing Survey (NAPS) here.

### Questions
- Cardinality - any multiplicities?
- Data access mechanism - maybe Bulk Data Access IG - bulk export by system? by patient? qualified by time period?
- Encounter ID should not be needed - systems have date time to differentiate from source system; bundle should have generated technical ids for an entry. NAPS can assign the internal DB id on ingestion.
- Prescription ID not needed for a source system to differentiate - can be assigned on consumption by NAPs; otherwise needs to be some sort of generator within practices that should still be stripped on ingestion by and replaced by internal DB id on ingestion.
- General Practice name (i.e. ID) - not desired however - in support of feedback look
  - under assumption of feedback from a single practice installation then need is resolution between NAPS & local system
    - essentially need practice registration with identifier system that is made unique using NAPS domain
~~~
...
    "identifier" : [
      {
      "system" : "https://www.naps.org.au/id/practice",
      "value" : "14124"
    },
...
~~~
- Prescriber ID - not desired however - feedback cross-enterprise? cross-setting? geographical boundaries? local system?
  - under assumption of feedback from a single practice installation then only need is local resolution
    - i.e. same practitioner in acute session won't get feedback taking into account both settings
    - essentially need practice registration with identifier system that is made unique using the practice registration qualifier
    - NAPS system and local system interaction to resolve and re-identify to provide feedback...? Could have local system registration known to NAPS system, but not provider - local system knows how to assign and resolve providers.
~~~
...
    "identifier" : [
      {
      "system" : "https://www.naps.org.au/id/practice-scoped/14124/prescriber",
      "value" : "3235209"
    },
...
~~~
- Patient Identifying SYSTEM INTERACTION REQUIREMENTS
    - Is every upload considered a unique patient entry? If so no need for client-side or server-side resolution of Patient record only a unique bundle entry id to link content for an upload commit
    - or is every patient the scope implying the source GP system needs a way to resolve the GP NAPS system's resolveable id - implications across multiple systems for patient records, security, consent, privacy and greatly increased cross enterprise patient record matching costs and issues
      - this is a pathway to re-identified data
      - if requiring that each system can uniquely match their patient against NAPS patient, resolve, and update then solution architecture needs significant consideration
      - what is the feedback / research qs being addressed?

What are the interactions this data set & FHIR IG supports? is it soley reporting? 

### How to Read this Guide

This guide is divided into several pages which are listed at the top of each page in the menu bar.

- [Home](index.html): This page provides the introduction and scope for this guide.
- [Guidance](guidance.html): This page provides guidance on using the profiles defined in this guide.
- [FHIR Artefacts](artifacts.html): These pages provide detailed descriptions and formal definitions for all the FHIR artefacts defined in this guide.
  - [Profiles and Extensions](profiles-and-extensions.html): This set of pages describes the profiles and extensions that are defined in this guide to represent Australian local concepts using FHIR. Each profile page includes a narrative description, guidance, and formal definition. Although the guidance typically focuses on the profiled elements and seeks to provide a ‘how-to’ guide when representing concepts, it may also may focus on un-profiled elements to aid with implementation.
- [Examples](examples.html): This page lists all the examples used in this guide.
- [Downloads](downloads.html): This page provides links to downloadable artefacts including the FHIR NPM package.


### Collaboration
This guide is the product of collaborative work undertaken with participants from:

* CSIRO Australian e-Health Research Centre 
* National Centre for Antimicrobial Stewardship (NCAS)

