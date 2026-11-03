--- 
title: Implementation Directory
post_excerpt: A directory of public APIs, terminology servers, and validation tools for UCUM.
---

> **Disclaimer & Notice:** The implementations, tools, and services listed below are provided solely for informational and community reference purposes. Regenstrief Institute, Inc. has not vetted, tested, audited, certified, or endorsed any third-party implementation, endpoint, or software listed in this directory. All information is provided **"AS IS"** without warranty of any kind, express or implied, including but not limited to implied warranties of merchantability, fitness for a particular purpose, operational availability, accuracy, or non-infringement. Inclusion in this directory does not constitute an endorsement, sponsorship, or recommendation by Regenstrief Institute. Users assume all risk, liability, and responsibility arising from the use of or reliance upon any third-party tool, service, or API referenced herein.

## FHIR Terminology Servers

The following FHIR servers host UCUM as a core code system and support programmatic validation (such as the `$validate-code` operation):

* **HL7 Global Terminology Server** (`tx.fhir.org`) — Reference FHIR R4 server with global UCUM validation support.
* **HL7 Europe Terminology Server** (`tx.hl7europe.eu/r4`) — Pan-European reference FHIR server supporting UCUM validation.
* **Australia (CSIRO Ontoserver Demo)** (`tx.ontoserver.csiro.au/fhir`) — Public FHIR R4 stack featuring the "Common UCUM Codes" value set.
* **Australia (National Clinical Terminology Service)** (`healthterminologies.gov.au/fhir`) — Production Ontoserver instance operated by the Australian Digital Health Agency.
* **Belgium (Health Apps Ontoserver)** (`apps.health.belgium.be/ontoserver/fhir`) — National FHIR terminology service providing UCUM.
* **Canada (Infoway Terminology Server)** (`terminology-server.infoway-inforoute.ca`) — FHIR service powered by Ontoserver with core UCUM code systems.
* **France (ANS / SMT Terminology Server)** (`smt.esante.gouv.fr/fhir`) — French e-Santé stack providing UCUM validation.
* **Germany (BfArM National Terminology Server)** (`terminologieserver.bfarm.de`) — National FHIR endpoints exposing UCUM.
* **Switzerland (HL7 CH Terminology Server)** (`tx.fhir.ch/r4`) — Terminology service supporting Swiss e-health profiles.
* **United Kingdom (NHS England Terminology Server)** (`digital.nhs.uk/services/terminology-server`) — National FHIR server with UCUM validation support.

## Interactive Web Tools & Dedicated APIs

Standalone web interfaces, specialized REST/SOAP endpoints, and conversion utilities:

* **NLM UCUM-LHC Tooling** — Interactive web form, REST/CSV API, and open-source code for validation and unit conversion ([ucum.nlm.nih.gov/ucum-lhc/](https://ucum.nlm.nih.gov/ucum-lhc/)).
* **NLM ClinicalTables UCUM API** — REST endpoints (`/validate`, `/convert`, `/commensurable`) widely integrated into EHRs and research pipelines ([clinicaltables.nlm.nih.gov/apidoc/ucum/v3/](https://clinicaltables.nlm.nih.gov/apidoc/ucum/v3/)).
* **XML4Pharma UCUM Web Services** — SOAP/REST web services maintained as a mirror of the NLM implementation ([xml4pharmaserver.com](https://xml4pharmaserver.com/.../UCUM_webservices.html)).
* **ucumate** is a developer-friendly Java library for working with units of measure based on the UCUM standard. At its core, it provides validation, canonicalization, conversion, and printing support with automatic caching. Optional features enable persistent database storage, mole-to-mass conversions, and high-precision calculation of conversion factors for special units. An [online demo](https://go.csiro.au/FwLink/ucumate-demo) is also available.
* **Anton V. UCUM Validator** — Lightweight, single-page web tool for validating and converting UCUM expressions ([antvaset.com/ucum-validator](https://www.antvaset.com/ucum-validator)).
* **University of Hawaiʻi ERDDAP Converter** — Specialized utility for converting between UDUNITS-1/-2 strings and UCUM expressions.
* **Data.gov UCUM Web API** — Federal catalog entry providing service metadata and SLA details for the NLM API endpoint.

## Implementation Notes

1. **Access Credentials:** While most public web interfaces permit ad-hoc validation without login, high-volume programmatic calls on national terminology servers often require a free API key or account registration.
2. **Underlying Libraries:** Most listed FHIR endpoints utilize the official UCUM Java library (embedded via Ontoserver or HAPI FHIR).
3. **Private Implementations:** Commercial EHR and LIS vendors frequently run private UCUM validators behind secure firewalls; these are omitted due to a lack of public endpoints.
4. **Maintenance:** Regional health IT initiatives launch new endpoints frequently, so periodic updates are recommended.
5. **Edits:** To provide updates or additions to this list, you can submit an issue or pull request on the [UCUM Documentation](https://github.com/ucum-org/ucum-docs) repository. You can also [contact us](https://ucum.org/contact).