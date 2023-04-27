This page compares the [GP NAPS data requirements](https://build.fhir.org/ig/aehrc/gp-naps-fhir/general-guidance.html#gp-naps-data-submission) to the data requirements of other national prescribing specifications in Australia.

The comparison table summarises which GP NAPS data requirements are also a requirement for a Real Time Prescription Monitoring (RTPM) system and an Electronic Prescribing (ETP)system.

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
                    Similar data requirement; minimal additional processing to add GP NAPS data export
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
                    Different but related data requirement; data may not match or significant additional processing to add GP NAPS data export
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
                    Data not required
                </p>
            </td>
        </tr>
    </tbody>
</table>


**Table: Comparison of GP NAPS Data Requirements to National Prescribing Specifications** 

<table border="1" cellspacing="0" cellpadding="0" width="609">
    <tbody>
        <tr>
            <td width="287" colspan="2" valign="top">
                <p>
                    <strong>GP NAPS requirement</strong>
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <strong>RTPM data requirement*</strong>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <strong>ETP data requirement*</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" rowspan="2" valign="top">
                <p>
                    Prescribing Organisation
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    State/Territory
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Postcode
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    Prescriber
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Specialty
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" rowspan="4" valign="top">
                <p>
                    Patient
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Indigenous status
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Biological sex**
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="tick-maybe.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Age**
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    AgeUnit**
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" rowspan="12" valign="top">
                <p>
                    Prescription
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Prescription type
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Date of visit
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Date of prescription
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Antimicrobial
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Route
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Dose
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Dose unit
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Frequency
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Quantity
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Repeats
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Indication for Antimicrobial
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/tick.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Long_Term
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" rowspan="3" valign="top">
                <p>
                    Allergies
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Allergies to Antimicrobial
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Nature of Allergies
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Severity
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    Trimester (pregnancy)
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Trimester (pregnancy)
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    Weight
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Weight
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    Smoking status
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Smoking status
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    eGFR
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    eGFR
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" valign="top">
                <p>
                    CrCl
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    CrCl
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="113" rowspan="4" valign="top">
                <p>
                    Microbiology
                </p>
            </td>
            <td width="174" valign="top">
                <p>
                    Microbiology collected
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Microbiology date collected
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Microbiology collected test
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
        <tr>
            <td width="174" valign="top">
                <p>
                    Microbiology collected result
                </p>
            </td>
            <td width="170" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
            <td width="151" valign="top">
                <p>
                    <img src="https://hl7.org/fhir/R4/assets/images/cross.png"/>
                </p>
            </td>
        </tr>
    </tbody>
</table>

\* _The data requirements for RTPM and ETP contain additional data elements that are not part of the GP NAPS data set._