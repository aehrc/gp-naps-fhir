### Intent of this Implementation Guide
TBD

### Forming pseudonym identifiers in FHIR

In support of feedback to practices and prescribers, a General Practice (system) could register with the NAPS system and gain a unique identifier known only to the NAPS system and that practice system that is used as the key for their data set. This identifier would not be shared with other registered practice systems or be allowed to be used for other purposes than the provision of feedback under NAPS agreements and the implemented data privacy and security controls.

This identifier would be applied as part of data extraction and export from the general practice system to the NAPS system.

For example
~~~
{
  "resourceType" : "Organization",
    ...
    "identifier" : [
      {
      "system" : "https://www.naps.org.au/id/practice",
      "value" : "14124"
    },
...
~~~

A unique Prescriber ID for use in NAPS exports would be assigned by the General Practice system and be stored in a map in the local system. NAPS has the local system registered, and the local system maintains an internal mapping for re-identification. The local system does not share that map or used for other purposes than the provision of feedback under NAPS agreements and the implemented data privacy and security controls. 

The Prescriber ID is unique only within that General Practice and when forming the identifier in FHIR it is made globally unique by using the General Practice system 

~~~
...
    "identifier" : [
      {
      "system" : "https://www.naps.org.au/id/practice-scoped/14124/prescriber",
      "value" : "3235209"
    },
...

The same pattern could be undertaken for a patient, if needed, if appropriate and approved as part of the data privacy and security assessments. 
~~~
...
    "identifier" : [
      {
      "system" : "https://www.naps.org.au/id/practice-scoped/14124/patient",
      "value" : "209"
    },
...
~~~
