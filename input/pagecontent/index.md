### Introduction
This implementation guide is provided to support the use of HL7<sup>&reg;</sup> FHIR<sup>&reg;&copy;</sup> to submit data for the General Practitioner (GP) National Antimicrobial Prescribing Survey (NAPS).

The [NAPS](https://www.naps.org.au) is coordinated by a multi-disciplinary team at the [National Centre for Antimicrobial Stewardship](https://www.ncas-australia.org/), and is delivered by the [Guidance Group](https://www.ncas-australia.org/Guidance_Group). This survey has been in use since 2011 and has already helped hundreds of Australian Health Care Facilities to assess their antimicrobial prescribing practice. It provides valuable information on the utilisation of antimicrobials within Australia.

This is a working specification developed in conjunction with the ongoing design of the GP NAPS data set. The content published in this guide is intended to be a base set of requirements for FHIR implementation of the data set that should be refined as design of the GP NAPS data set is matured. 

This guide does not cover:
- data access and API
- data privacy and security controls

### How to Read this Guide

This guide is divided into several pages which are listed at the top of each page in the menu bar.

- [Home](index.html): This page provides the introduction and scope for this guide.
- [Guidance](guidance.html): This page provides guidance.
- [FHIR Artefacts](artifacts.html): These pages provide detailed descriptions and formal definitions for all the FHIR artefacts defined in this guide.
  - [Profiles and Extensions](profiles-and-extensions.html): This set of pages describes the profiles and extensions that are defined in this guide to represent Australian local concepts using FHIR. Each profile page includes a narrative description, guidance, and formal definition. Although the guidance typically focuses on the profiled elements and seeks to provide a ‘how-to’ guide when representing concepts, it may also may focus on un-profiled elements to aid with implementation.
  - [Terminology](terminology.html): This set of pages lists the value sets and code systems defined in this guide.
- [Examples](examples.html): This page lists all the examples used in this guide.
- [Downloads](downloads.html): This page provides links to downloadable artefacts including the FHIR NPM package.


### Collaboration
This guide is the product of collaborative work undertaken with participants from:

* CSIRO Australian e-Health Research Centre 
* National Centre for Antimicrobial Stewardship (NCAS)

