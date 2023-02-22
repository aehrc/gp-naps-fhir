### Intent of this Implementation Guide
TBD

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

These identifiers do not attempt to implement data security and privacy controls, the GP NAPS system may implement a different approach.