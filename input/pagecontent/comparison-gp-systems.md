This page provides a summary of an analysis performed that compared the GP NAPS data requirements with the possible support that GP clinical systems could provide. The overall tabular summary can be seen below.

Analysis was performed by assessing three leading GP systems using [Training simulators](https://www.digitalhealth.gov.au/healthcare-providers/initiatives-and-programs/my-health-record#training-simulators) provided by the [Australian Digital Health Agency](https://www.digitalhealth.gov.au/). The GP NAPS data requirements were compared against the user interface (UI), including data fields and other visual components, of the GP systems and observations were made as to the level of support that would be likley.

Consideration was given to the data field names, the context within the system workflow including surrounding fields, the perceived data types in the UI and the values that were possible to record against a particular field. For example, the specific values, the semantic type of possible values and the granularity of those values.

The analysis was limited to what could be observed from a UI perspective and the GP system environments being used. Those environments did not necessarily have all features accessible and had limited test data. This most impacted the assessment of pathology results information. Previous pathology results were not found and therefore, could not be assessed. Requested pathology was available but this did not correlate with the data requirement. An additional limitation noted is the fields and data types observed in the UI do not necessarily correlate with data stored by the system.

There was a strong level of support for many of the items, with ubiquitous support observed for key pieces of data such as "Antimicrobial", "Indication" for Antimicrobial and "Allergies to Antimicrobial". There were several data requirements where the level of possible support was difficult to assess given the variability in the way the data is recorded and aligned to the requirements as specified. For example, it was observed that dosage instructions data did not correlate with the discrete fields prescribed by the data requirements. Sometimes data was present as part of another data item (e.g. dose unit contained in medication) and others were concatenated together to form a string of instructions (e.g. dose + frequency + route). For these items, it may be possible to derive the discrete components but it is anticipated it would require significant additional processing. 

It appears as though a large proportion of the data requirements could be met, however, it would require varing levels of processing to meet each one. 

**Table 1: Key:** Describes how the symbols in Table 2 should be interpreted.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="94" valign="top">
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
            <td width="94" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    Either a field is present that directly correlates with the
                    requirement or it is anticipated the value might be derived
                    with minimal additional processing.
                </p>
            </td>
        </tr>
        <tr>
            <td width="94" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    There is similar data captured but either a direct correlation was difficult to determine or
                    it is anticipated significant additional processing may be required to meet
                    the requirement.
                </p>
            </td>
        </tr>
        <tr>
            <td width="94" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    There is no obvious support for this requirement.
                </p>
            </td>
        </tr>
        <tr>
            <td width="94" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="436" valign="top">
                <p>
                    The requirement was not assessable due to limitations in
                    the system simulator.
                </p>
            </td>
        </tr>
    </tbody>
</table>


**Table 2: GP NAPS Requirement Support in GP Systems:** Summarises the data requirements of GP NAPS and indicates the level of support observed in each GP system assessed.

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
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
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
                    <img src="tick-maybe.png"/>
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
                    <img src="tick-maybe.png"/>
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
                    <img src="tick-maybe.png"/>
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
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
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
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
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
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
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
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
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
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
                </p>
            </td>
            <td width="142" valign="top">
                <p>
                    <img src="question.png"/>
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
    </tbody>
</table>

