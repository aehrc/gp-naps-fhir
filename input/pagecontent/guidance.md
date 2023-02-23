### GP NAPS Data Submission
Fields to be passed to NAPS from general practice patient record management software systems in use in Australia.

The table below identifies the element that is the primary semantic match for that field to support ingestion of the data submission into the NAPS system. A complete FHIR data submission will populate a clinical or administrative concept in each FHIR resource that concept is applicable, for example:
- each FHIR resource will declare it's context including the patient
- date of visit is primarily matched to MedicationRequest.authoredOn but may also be populated in a MedicationStatement, Encounter, and Specimen resource.

For guidance on a complete FHIR data submission see the section [Complete FHIR data submission](guidance.html#complete-fhir-data-submission).

|GP NAPs data field|GP NAPS Profile|FHIR element|
|---|----|---|---|
|State/Territory|[GP NAPS Organization](StructureDefinition-gp-naps-organization.html)|Organization.address.state|
|Postcode|[GP NAPS Organization](StructureDefinition-gp-naps-organization.html)|Organization.address.postalCode|
|Gender|[GP NAPS Patient](StructureDefinition-gp-naps-patient.html)|Patient.gender|
|Indigenous Status |[GP NAPS Patient](StructureDefinition-gp-naps-patient.html)|Patient.extension:indigenousStatus|
|Prescription type|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.extension:TBD|
|Date of visit|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.authoredOn|
|Date of prescription|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.validityPeriod.start|
|Antimicrobial|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.medicationCodeableConcept XOR Medication.code|
|Route|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.route|
|Dose|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.value|
|Dose unit|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.unit|
|Dose form|[GP NAPS Medication](StructureDefinition-gp-naps-medication.html)|Medication.form|
|Frequency|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.timing|
|Quantity|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.quantity|
|Repeats|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.numberOfRepeatsAllowed|
|Indication for Antimicrobial|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.reasonCode|
|Long_Term|[GP NAPS MedicationStatement](StructureDefinition-gp-naps-medicationstatement.html)|MedicationStatement.extension:longTerm|
|Allergies to Antimicrobial|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.code|
|Nature of Allergies|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.reaction.manifestation|
|Severity|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.reaction.severity|
|Specialty|[GP NAPS PractitionerRole](StructureDefinition-gp-naps-practitionerrole.html)|PractitionerRole.specialty|
|Age|[GP NAPS Age](StructureDefinition-gp-naps-age.html)|Observation.valueQuantity.value XOR Observation.valueRange.low.value and Observation.valueRange.high.value|
|AgeUnit|[GP NAPS Age](StructureDefinition-gp-naps-age.html)|Observation.valueQuantity.unit XOR Observation.valueRange.low.unit and Observation.valueRange.high.unit|
|Weight|[GP NAPS Body Weight](StructureDefinition-gp-naps-bodyweight.html)|Observation.valueQuantity|
|eGFR|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.valueQuantity|
|CrCl|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.valueQuantity|
|Microbiology collected|[GP NAPS Specimen](StructureDefinition-gp-naps-specimen.html)|Specimen.type|
|Microbiology date collected|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.effectiveDateTime XOR Observation.effectivePeriod|
|Microbiology collected test|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.code|
|Microbiology collected result|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.value[x]|
|smoking status |[GP NAPS Smoking Status](StructureDefinition-gp-naps-smokingstatus.html)|Observation.valueCodeableConcept|
|Indication Documented|N/A|Generated as part of ingestion of data by NAPS if indication is present.|
|Event_Id|N/A|Generated as part of ingestion of data by NAPS from either each MedicationRequest XOR each Encounter.|
|General Practice Name|Not in scope of IG|Part of data access, privacy, and security.|
|Patient Identifying No|Not in scope of IG|Part of data access, privacy, and security.|
|Prescriber Number|Not in scope of IG|Part of data access, privacy, and security.|
{:.grid}


### Complete FHIR data submission
The table below provides guidance to developers implementing data export from a general practice system in forming the GP NAPS data submission.

|GP NAPs data field|Primary FHIR element|Derived FHIR element|
|---|----|---|
|State/Territory|Organization.address.state|N/A|
|Postcode|Organization.address.postalCode|N/A|
|Gender|Patient.gender|N/A|
|Indigenous Status |Patient.extension:indigenousStatus|N/A|
|Prescription type|MedicationRequest.extension:TBD|N/A|
|Date of visit|MedicationRequest.authoredOn|Encounter.period.end and MedicationStatement.dateAsserted|
|Date of prescription|MedicationRequest.dispenseRequest.validityPeriod.start|N/A|
|Antimicrobial|MedicationRequest.medicationCodeableConcept XOR Medication.code|If use of MedicationRequest.medicationCodeableConcept then MedicationStatement.medicationCodeableConcept|
|Route|MedicationRequest.dosageInstruction.route|MedicationStatement.dosage.route|
|Dose|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.value|MedicationStatement.dosage.doseAndRate.doseQuantity.value|
|Dose unit|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.unit|MedicationStatement.dosage.doseAndRate.doseQuantity.unit|
|Dose form|Medication.form|N/A|
|Frequency|MedicationRequest.dosageInstruction.timing|MedicationStatement.dosage.timing|
|Quantity|MedicationRequest.dispenseRequest.quantity|N/A|
|Repeats|MedicationRequest.dispenseRequest.numberOfRepeatsAllowed|N/A|
|Indication for Antimicrobial|MedicationRequest.reasonCode|MedicationStatement.reasonCode|
|Long_Term|MedicationStatement.extension:longTerm|N/A|
|Allergies to Antimicrobial|AllergyIntolerance.code|AllergyIntolerance.reaction.substance|
|Nature of Allergies|AllergyIntolerance.reaction.manifestation|N/A|
|Severity|AllergyIntolerance.reaction.severity|N/A|
|Specialty|PractitionerRole.specialty|N/A|
|Age|Observation.valueQuantity.value XOR Observation.valueRange.low.value and Observation.valueRange.high.value|N/A|
|AgeUnit|Observation.valueQuantity.unit XOR Observation.valueRange.low.unit and Observation.valueRange.high.unit|N/A|
|Weight|Observation.valueQuantity|N/A|
|eGFR|Observation.valueQuantity|N/A|
|CrCl|Observation.valueQuantity|N/A|
|Microbiology collected|Specimen.type|N/A|
|Microbiology date collected|Observation.effectiveDateTime XOR Observation.effectivePeriod|Specimen.collection.collected[x]|
|Microbiology collected test|Observation.code|N/A|
|Microbiology collected result|Observation.value[x]|N/A|
|smoking status |Observation.valueCodeableConcept|N/A|
{:.grid}


### Pseudonym identifiers (de-identification and re-identification)
This implementation guide does not prescribe or recommend an approach to de-identification and re-identification of data for NAPS. 

Within defined data security and privacy controls, a GP NAPS implementation may support the collection of data and provision of feedback to practices and prescribers through de-identification and re-identification protocols implemented by GP NAPS system and a local practice system participating in GP NAPS.

De-identification and re-identification may make use of a practice-scoped set of identifiers in a number of different ways including making use of hashing, local maps, etc. FHIR, and use of Bulk Data Access, can support most (if not all) approaches.

In this implementation guide to support example resources demonstrating the clinical data set, this implementation guide mandates Organization.identifier, and includes two simple types of identifiers:
- a UUID with no information on assigner, e.g.
~~~
{
  "resourceType" : "Organization",
    ...
    "identifier" : [
      {
      "system" : "urn:ietf:rfc:3986",
      "value" : "urn:uuid:53fefa32-fcbb-4ff8-8a92-55ee120877b7"
    },
...
~~~
- an identifier within a NAPS naming system, e.g.
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

    with locally managed prescriber identifier the local system (but not NAPS) would use to re-identify

    ~~~
    ...
        "identifier" : [
          {
          "system" : "https://www.naps.org.au/id/practice-scoped/14124/prescriber",
          "value" : "3235209"
        },
    ...
    ~~~

These identifiers do not implement data security and privacy controls, the GP NAPS system may implement a different approach.