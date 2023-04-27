### Overview

This page compares the [GP NAPS data requirements](https://build.fhir.org/ig/aehrc/gp-naps-fhir/general-guidance.html#gp-naps-data-submission) with three leading Australian GP systems. The GP systems were assessed using [Training simulators](https://www.digitalhealth.gov.au/healthcare-providers/initiatives-and-programs/my-health-record#training-simulators) provided by the [Australian Digital Health Agency](https://www.digitalhealth.gov.au/).

The data requirements were compared against the systems' user interface (UI) with consideration given to data field names, context within the system workflow including surrounding fields, the perceived data types in the UI and the values that were possible to record against a particular field. Based on the information that could be input, an assessment was made as to the ease at which data could be exported to meet the requirements.

A summary of findings is presented in the tables below.

### Limitations

Limitations were noted due to the approach taken for this analysis. They are as follows:

* Not all features are accessible in the training simulators and may not reflect production environments.
* Data could be entered, but existing data is limited to the test data present in the training simulators. This most impacted the assessment of pathology results information. 
* Fields and data types observed in a UI do not necessarily correlate with data stored by a system. 

### Findings

There is uniform support for many of the data requirements, such as "Antimicrobial", "Indication for Antimicrobial" and "Allergies to Antimicrobial". For others, there is variability in the way data is recorded and therefore, variability is expected in the data that might be exported to meet the requirements. For example, it was observed that dosage instructions data does not always correlate with discrete fields. Sometimes information is present as part of another data item (e.g. dose unit contained in medication) and others were concatenated together to form a string of instructions (e.g. dose + frequency + route). For these items, it may be possible to derive the discrete components but it is anticipated it would require significant additional processing.

Overall, the systems assessed appeared to support the majority of data requirements. Support may be broadened through additional processing of data for export, however, it is noted that support may already exist with capability not assessable in a UI. There was only a single data point in one system that did not appear to be supported.


**Table: Key to symbols**

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="90" valign="top">
                <p>
                    <strong>Symbol</strong>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    <strong>Description</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="90" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    Minimal additional processing is expected to be needed to export the data specified
                </p>
            </td>
        </tr>
        <tr>
            <td width="90" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    Significant additional processing may be required to export the data specified
                </p>
            </td>
        </tr>
        <tr>
            <td width="90" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    No obvious support
                </p>
            </td>
        </tr>
    </tbody>
</table>


**Table: Level of support for GP NAPS Data Requirements in GP Systems Assessed** 

<table border="1" cellspacing="0" cellpadding="0" width="680">
    <tbody>
        <tr>
            <td width="293" colspan="2" valign="top">
                <p>
                    <strong>GP NAPS requirement</strong>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <strong>System 1 Support</strong>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <strong>System 2 Support</strong>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <strong>System 3 Support</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" rowspan="2" valign="top">
                <p>
                    Prescribing Organisation
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    State/Territory
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Postcode
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Prescriber
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Specialty
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Patient
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Indigenous status
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
            </td>
            <td width="161" valign="top">
                <p>
                    Biological sex
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
            </td>
            <td width="161" valign="top">
                <p>
                    Age
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
            </td>
            <td width="161" valign="top">
                <p>
                    AgeUnit
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" rowspan="12" valign="top">
                <p>
                    Prescription
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Prescription type
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Date of visit
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Date of prescription
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Antimicrobial
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Route
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Dose
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Dose unit
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Frequency
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Quantity
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Repeats
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Indication for Antimicrobial
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Long_Term
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Allergies
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Allergies to Antimicrobial
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
            </td>
            <td width="161" valign="top">
                <p>
                    Nature of Allergies
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
            </td>
            <td width="161" valign="top">
                <p>
                    Severity
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Trimester (pregnancy)
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Trimester (pregnancy)
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Weight
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Weight
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    Smoking status
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Smoking status
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    eGFR
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    eGFR
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" valign="top">
                <p>
                    CrCl
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    CrCl
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
        </tr>
        <tr>
            <td width="132" rowspan="4" valign="top">
                <p>
                    Microbiology
                </p>
            </td>
            <td width="161" valign="top">
                <p>
                    Microbiology collected
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Microbiology date collected
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Microbiology collected test
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
        </tr>
        <tr>
            <td width="161" valign="top">
                <p>
                    Microbiology collected result
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    *
                </p>
            </td>
        </tr>
    </tbody>
</table>

\* _Data requirement was not able to be assessed. Previous pathology results were not found in the test data and could not be created as this would typically come from a pathology provider. Requesting pathology was able to be entered but this does not correlate with the data requirement._