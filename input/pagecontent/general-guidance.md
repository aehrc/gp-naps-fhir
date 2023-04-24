### GP NAPS Data Submission
Fields to be passed to NAPS from general practice patient record management software systems in use in Australia.

The table below identifies the element that is the primary match for that field to support ingestion of the data submission into the NAPS system. 

A complete FHIR data submission will include the source system value in each element it applies to, for example:
- 'Date of visit' is primarily matched to MedicationRequest.authoredOn, but if the resources are included, it will also be included in Encounter.period.end, MedicationStatement.dateAsserted, Observation(Age).effectiveDateTime and Observation(Gestational Age Trimester).effectiveDateTime.

For guidance on constructing a complete FHIR data submission see the section [Complete FHIR data submission](general-guidance.html#complete-fhir-data-submission).

|GP NAPs data field|GP NAPS Profile|Primary FHIR element|
|---|----|---|---|
|State/Territory|[GP NAPS Organization](StructureDefinition-gp-naps-organization.html)|Organization.address.state|
|Postcode|[GP NAPS Organization](StructureDefinition-gp-naps-organization.html)|Organization.address.postalCode|
|Biological sex|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.extension:sexForClinicalUse|
|Trimester (pregnancy)|[GP NAPS Gestational Age Trimester](StructureDefinition-gp-naps-gestational-age-trimester.html)|Observation.valueCodeableConcept|
|Indigenous status |[GP NAPS Patient](StructureDefinition-gp-naps-patient.html)|Patient.extension:indigenousStatus|
|Prescription type|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.extension:scriptAuthorityType|
|Date of visit|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.authoredOn|
|Date of prescription|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.validityPeriod.start|
|Antimicrobial|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.medicationCodeableConcept|
|Route|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.route|
|Dose|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.value|
|Dose unit|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.doseAndRate.doseQuantity.unit|
|Frequency|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dosageInstruction.timing|
|Quantity|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.quantity|
|Repeats|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.dispenseRequest.numberOfRepeatsAllowed|
|Indication for Antimicrobial|[GP NAPS MedicationRequest](StructureDefinition-gp-naps-medicationrequest.html)|MedicationRequest.reasonCode|
|Long_Term|[GP NAPS MedicationStatement](StructureDefinition-gp-naps-medicationstatement.html)|MedicationStatement.extension:longTerm|
|Allergies to Antimicrobial|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.code|
|Nature of Allergies|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.reaction.manifestation|
|Severity|[GP NAPS AllergyIntolerance](StructureDefinition-gp-naps-allergyintolerance.html)|AllergyIntolerance.reaction.severity|
|Specialty|[GP NAPS PractitionerRole](StructureDefinition-gp-naps-practitionerrole.html)|PractitionerRole.code|
|Age|[GP NAPS Age](StructureDefinition-gp-naps-age.html)|Observation.valueQuantity.value|
|AgeUnit|[GP NAPS Age](StructureDefinition-gp-naps-age.html)|Observation.valueQuantity.unit|
|Weight|[GP NAPS Body Weight](StructureDefinition-gp-naps-bodyweight.html)|Observation.valueQuantity|
|eGFR|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.valueQuantity|
|CrCl|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.valueQuantity|
|Microbiology collected|[GP NAPS Specimen](StructureDefinition-gp-naps-specimen.html)|Specimen.type|
|Microbiology date collected|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.effectiveDateTime|
|Microbiology collected test|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.code|
|Microbiology collected result|[GP NAPS Pathology Result](StructureDefinition-gp-naps-pathologyresult.html)|Observation.value[x]|
|Smoking status |[GP NAPS Smoking Status](StructureDefinition-gp-naps-smokingstatus.html)|Observation.valueCodeableConcept|
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
|Biological sex|MedicationRequest.extension:sexForClinicalUse|N/A|
|Trimester (pregnancy)|Observation.valueCodeableConcept|N/A|
|Indigenous status |Patient.extension:indigenousStatus|N/A|
|Prescription type|MedicationRequest.extension:scriptAuthorityType|N/A|
|Date of visit|MedicationRequest.authoredOn|Encounter.period.end and MedicationStatement.dateAsserted and Observation(Age).effectiveDateTime and Observation(Gestational Age Trimester).effectiveDateTime|
|Date of prescription|MedicationRequest.dispenseRequest.validityPeriod.start|MedicationStatement.effectivePeriod.start|
|Antimicrobial|MedicationRequest.medicationCodeableConcept|MedicationStatement.medicationCodeableConcept. |
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
|Specialty|PractitionerRole.code|N/A|
|Age|Observation.valueQuantity.value|N/A|
|AgeUnit|Observation.valueQuantity.unit|N/A|
|Weight|Observation.valueQuantity|N/A|
|eGFR|Observation.valueQuantity|N/A|
|CrCl|Observation.valueQuantity|N/A|
|Microbiology collected|Specimen.type|N/A|
|Microbiology date collected|Observation.effectiveDateTime|Specimen.collection.collectedDateTime|
|Microbiology collected test|Observation.code|N/A|
|Microbiology collected result|Observation.value[x]|N/A|
|Smoking status |Observation.valueCodeableConcept|N/A|
{:.grid}

### Frequency (dose timing)
The core FHIR standard provides advice on how to structure common dose timings in FHIR for machine-readable use cases incl analytics with standard text converters available for the purposes of rendering for human-readability. That advice is excerpted below with examples provided.

GP NAPS data submission export is recommended to structure dose timing, and convert to text as needed.

This table summarises some common uses of the [Timing](http://hl7.org/fhir/R4/datatypes.html#timing) Data Type criteria.


<table class="grid">
 <tr><td><b>description</b></td> <td><b>duration</b></td> <td><b>durationUnit</b></td> <td><b>frequency</b></td> <td><b>frequencyMax</b></td> <td><b>period</b></td> <td><b>periodUnit</b></td> <td><b>periodMax</b></td> <td><b>Day of Week</b></td> <td><b>Time Of Day</b></td> <td><b>when</b></td> <td><b>offset</b></td>  <td><b>bounds[x]</b></td>  <td><b>count</b></td></tr>
 <tr><td>Every 8 hours</td>      <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>8</td>             <td>h</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>Every 7 days</td>       <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>7</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>3 times a day</td>      <td></td>                <td></td>                     <td>3</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>3-4 times a day</td>    <td></td>                <td></td>                     <td>3</td>                <td>4</td>                   <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>Every 4-6 hours</td>    <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>4</td>             <td>h</td>                  <td>6</td>              <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>Every 21 days for 1 hour</td> <td>1</td>         <td>hr</td>                   <td>1</td>                <td></td>                    <td>21</td>            <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>Three times a week for ½ hour</td> <td>0.5</td>  <td>hr</td>                   <td>3</td>                <td></td>                    <td>1</td>             <td>wk</td>                 <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>With breakfast</td>     <td></td>                <td></td>                     <td></td>                 <td></td>                    <td></td>              <td></td>                   <td></td>               <td></td>                   <td></td>                   <td>CM</td>        <td></td>               <td></td>               <td></td></tr>
 <tr><td>For 5 minutes, 10 minutes before meals</td> <td>5</td>     <td>min</td>        <td></td>                 <td></td>                    <td></td>              <td></td>                   <td></td>               <td></td>                   <td></td>                   <td>AC</td>        <td>10</td>             <td></td>               <td></td></tr>
 <tr><td>1 tablet 3 times daily, 30 minutes before meals</td> <td></td>  <td></td>      <td>3</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td>AC</td>        <td>30</td>             <td></td>               <td></td></tr>
 <tr><td>BID, 30 mins before meal, for next 10 days</td> <td></td>  <td></td>            <td>2</td>               <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td>AC</td>        <td>30</td>             <td>Duration = 10 days</td>               <td></td></tr>
 <tr><td>TID, for 14 days</td>   <td></td>                <td></td>                     <td>3</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td>Duration = 14 days</td>               <td></td></tr>
 <tr><td>BID, start on 7/1/2015 at 1:00 PM</td> <td></td> <td></td>                     <td>2</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td>Period.start = 2015-07-01T13:00:00</td>               <td></td></tr>
 <tr><td>Mon, Wed, Fri Morning</td> <td></td>             <td></td>                     <td>1</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td>mon | wed | fri</td>    <td></td>                   <td>MORN</td>      <td></td>               <td></td>               <td></td></tr>
 <tr><td>Every day at 10am</td>  <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>               <td></td>                   <td>10:00</td>              <td></td>          <td></td>               <td></td>               <td></td></tr>
 <tr><td>Take once, at any time</td>  <td></td>           <td></td>                     <td></td>                 <td></td>                    <td></td>              <td></td>                   <td></td>               <td></td>                   <td></td>                   <td></td>          <td></td>               <td></td>               <td>1</td></tr>
 <tr><td>Take every second day, in the morning, until 20 have been taken</td><td></td>  <td></td>  <td>1</td>     <td></td>                    <td>2</td>             <td>d</td>                  <td></td>               <td></td>                   <td></td>                   <td>MORN</td>      <td></td>               <td></td>               <td>20</td></tr>
</table>

~~~
  "timing": { //  Frequency 24 hourly, Once a day
    "repeat" : {
          "frequency" : 1,
          "period" : 24,
          "periodUnit" : "h"
    }    
  }
~~~

~~~
  "timing": { //  Frequency 6 hourly, Four times a day
    "repeat" : {
          "frequency" : 1,
          "period" : 6,
          "periodUnit" : "h"
    }    
  }
~~~

~~~
  "timing": { //  Frequency every 4-6 hours
    "repeat" : {
          "frequency" : 1,
          "period" : 4,
          "periodMax" : 6,
          "periodUnit" : "h"
    }    
  }
~~~

~~~
  "timing": { //  Frequency Two times a week
    "repeat" : {
          "frequency" : 2,
          "period" : 1,
          "periodUnit" : "wk"
    }    
  }
~~~


#### Timing as text only 
Systems may avoid the complexity of the Timing structure by using a text field for timing instructions. This maps to <code>Timing.code.text</code>, for example:

~~~
  "timing": {
    "code" : {
      "text" : "Take medication in the morning on weekends and days off work"
    }    
  }
~~~

Note, though, that some systems include timing details in something like 'Dosage instructions' which is wider than just Timing; those systems do not use the Timing data type. 

#### Timing as code 
Other systems use a set of 'common' codes - including, but usually not limited to, 
widely understood acronyms such as "BID". If a <code>Timing.code</code> is provided, the code is understood to be a complete statement of whatever is specified in the structured timing data (except for <code>Timing.repeat.bounds</code>, which applies to the code), and either the code or the data may be used to interpret the <code>Timing</code>. A structured timing specification SHOULD be provided whenever possible, unless the code is BID, TID, QID, AM or PM, which have a ubiquitous meaning.
</p>
<p>
This table shows the relationship between the codes provided as part of the core FHIR specification, and the structured data portions of the Timing type:
</p>
<table class="grid">
 <tr><td><b>description</b></td> <td><b>duration</b></td> <td><b>durationUnit</b></td> <td><b>frequency</b></td> <td><b>frequencyMax</b></td> <td><b>period</b></td> <td><b>periodUnit</b></td> <td><b>periodMax</b></td> <td><b>when</b></td> <td><b>bounds[x]</b></td></tr>
 <tr><td>QOD</td>                <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>2</td>             <td>d</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>QD</td>                 <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>BID</td>                <td></td>                <td></td>                     <td>2</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>TID</td>                <td></td>                <td></td>                     <td>3</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>QID</td>                <td></td>                <td></td>                     <td>4</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>Q4H</td>                <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>4</td>             <td>h</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>Q6H</td>                <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>6</td>             <td>h</td>                  <td></td>                 <td></td>            <td></td></tr>
 <tr><td>AM</td>                 <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td>MORN</td>        <td></td></tr>
 <tr><td>PM</td>                 <td></td>                <td></td>                     <td>1</td>                <td></td>                    <td>1</td>             <td>d</td>                  <td></td>                 <td>AFT or EVE</td>  <td></td></tr>
</table>

~~~
  "timing": {
    "code" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v3-GTSAbbreviation",
        "code" : "BID",
        "display" : "BID"
      }]
    }    
  }
~~~

<p>
These codes **SHALL** be understood as having the formal meanings documented in this table. Note that <code>BID</code>, etc. are defined as 'at institutionally specified times'.
For example, an institution may choose that <code>BID</code> is "always at 7am and 6pm".  If it is inappropriate for this choice to be made, the code <code>BID</code> should not be used. Instead, a distinct organisation-specific code is used in place of the HL7-defined <code>BID</code> code and/or a structured representation should be used (in this case, <code>timeOfDay</code>).
</p>

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

    - with locally managed prescriber identifier the local system (but not NAPS) would use to re-identify

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

### Conformance and Must Support

FHIR defines the notion of [Must Support](http://hl7.org/fhir/R4/conformance-rules.html#mustSupport) to help establish conformance expectations for systems. The specific meaning of "Must Support" is required to be defined in individual implementation guides. 

For the purposes of this implementation guide, "Must Support" is defined in principle against a data specification it does not define the obligations for operations. To implement GP NAPS the definition of must support **SHALL** be extended as part of specifying the API by either:
- extending this specification to include the API definition with CapabilityStatements and must support obligations, or
- defining a separate API specification that points to this GP NAPS FHIR implementation guide

In principle, the system actors are defined as:


<table class="list">
  <thead>
    <tr>
      <th>System actor</th>
      <th>Description</th>
      <th>Obligation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>GP data submission</td>
      <td>An application that submits a GP NAPS data submission set. This may be the application that generates the data submission set.</td>
      <td><b>SHALL</b> be capable of sending the data element.</td>
    </tr>
    <tr>
      <td>Data receipt</td>
      <td>An application that receives and processes a GP NAPS data submission set. This may be the application that persists data.</td>
      <td><b>SHALL</b> be capable of receiving and processing the data element for storage.</td>
    </tr>
  </tbody>
</table>


See recommended guidance on must support in [AU Core](https://build.fhir.org/ig/hl7au/au-fhir-core/must-support.html).

#### Generating the submission set of data

A GP NAPS data submission is composed of a set of resources. This set of resources may be submitted in Bulk Data Export format (ndjson), or Bundle, or some other format, as defined by the API for GP NAPS.

The GP NAPS data submission **SHALL** contain:
- one and only one Organization resource that represents the GP from which this data set is submitted
- a Patient resource for each patient in the data set
- a MedicationRequest for each prescription in the data set
- an Age Observation resource for each prescription in the data set
- a PractitionerRole for each prescriber in the data set (each prescription must have a prescriber)

The GP NAPS data submission **MAY** contain, if available:
- a MedicationStatement for each prescription, if and only if information on long term usage is available
- a Trimester Observation for each prescription
- an AllergyIntolerance for each statement of each patient's allergy
- a Body Weight resource for each patient that is the latest body weight at the time of data submission
- a Smoking Status resource for each patient that is the latest smoking status at the time of data submission
- an AllergyIntolerance for each statement of each patient's allergy
- a Pathology Result Observation for each ordered test or set of results for a patient at the time of data submission  
- a Specimen for each Pathology Result, if and only if specimen type information is available
