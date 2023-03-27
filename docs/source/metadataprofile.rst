.. _4.1

4.1 Permitted uses
==============================

======== ==========
Required Repeatable
======== ==========
Yes      Yes
======== ==========

**Definition**
A brief general description of the kinds of permitted secondary uses of the dataset. These uses would generally be dictated by the terms of consent and/or HREC approval. A more detailed description of the terms of use would be provided via the Data Sharing Policy [4.2] and Rights/Licence [4.3] attribute.

It is assumed that requests to access data for secondary use may require review on a case by case basis. As such, this attribute is used to indicate the kinds of requests that align with existing consent/HREC approval.

ANZCTR Step 11 must be provided.

Optionally, more structured metadata can be provided to DataCite to enable machine-readability of permitted uses, which the HeSANDA portal can use to provide a better user experience.

If providing metadata to DataCite, DUO - the Data Use Ontology - is recommended here, if appropriate for the dataset. Read an introduction here. 
Note: DUO terms can currently only be applied using the DataCite metadata schema.


========================================================= =========== ============== =========================================================================================== ============================ =====
Source metadata field                                     Occurrences Input type     Example input                                                                               Controlled vocabulary source Notes
========================================================= =========== ============== =========================================================================================== ============================ =====
ANZCTR Step 11 -  ’Available for what types of analyses?’ 1           Text           Any purpose, only to achieve the aims in the approved proposal, for IPD meta-analyses, etc.
DataCite 16 Rights                                        0-n         Text           population origins/ancestry research
DataCite 16.a rightsURI                                   0-1         Text           http://purl.obolibrary.org/obo/DUO_0000011
DataCite 16.b rightsIdentifier                            0-1         Text           DUO_0000011
DataCite 16.c rightsIdentifierScheme                      0-1         Text from list DUO
DataCite 16.d schemeURI                                   0-1         Text           http://purl.obolibrary.org/obo/duo.owl
========================================================= =========== ============== =========================================================================================== ============================ =====

.. _4.2

4.2 Data sharing policy
==============================

======== ==========
Required Repeatable
======== ==========
Yes       Yes
======== ==========

**Definition**

A policy statement and/or set of procedures that addresses secondary use of the dataset. This would commonly be presented as a publicly accessible document or webpage that details items such as the following:

Governance roles and responsibilities
Regulatory requirements (e.g. legal, ethical, funding)
Requirements for requesting data access (e.g. procedures, time frames, costs)
Requirements for management and handling of shared data (e.g. storage and disposal, reporting)

Data sharing policies are broad in nature and represent the general position of the data custodian regarding sharing of the dataset. It is common for a specific data sharing agreement to be signed by the requestor and custodian prior to the release of data in response to a data request. Data sharing agreements are contracts between two or more parties that articulate the specific terms and conditions for the sharing of data for a specific purpose. The data sharing policy may be cited in the terms of the data sharing agreement if required.

See also Permitted uses [4.1] and Rights/Licence [4.3].

===================================== =========== ========== ============== ============================ ======================================================================================================================================================================
Source metadata field                 Occurrences Input type Example input  Controlled vocabulary source Notes
===================================== =========== ========== ============== ============================ ======================================================================================================================================================================
NZCTR Step 11: Data sharing statement 1                                                                  See 2.8 Other research outputs and related publications for a more detailed breakdown of DataCite 20 relatedItem. Use relatedItemType “Text” for a data sharing policy.
===================================== =========== ========== ============== ============================ ======================================================================================================================================================================

.. _4.3

4.3 Rights/ Licence
==============================

======== ==========
Required Repeatable
======== ==========
No       Yes
======== ==========

**Definition**

Any intellectual property rights and/or licensing information regarding sharing and/or secondary use of the data object. This may be expressed as:

A textual statement of the rights management associated with the asset
A legal document under which the asset is made available (e.g. a data sharing agreement template)

See also Permitted uses [4.1] and Data sharing policy [4.2].


======================= =========== ========== ============================================================================================================================================================== ============================ =====
Source metadata field   Occurrences Input type Example input                                                                                                                                                  Controlled vocabulary source Notes
======================= =========== ========== ============================================================================================================================================================== ============================ =====
DataCite 16 Rights      0-n         Text       RESTRICTIVE LICENCE AGREEMENT for USE OF MATERIAL [insert description] between THE SUPPLIER [insert Supplier’s name] and THE CUSTOMER [insert Customer’s name]
DataCite 16.a rightsURI 0-1         Text       https://licenceagreementtemplate.uni.edu.au/
======================= =========== ========== ============================================================================================================================================================== ============================ =====

.. _4.4.1:

4.4.1 Enquiries 
==============================

======== ==========
Required Repeatable
======== ==========
Yes      Yes
======== ==========

**Definition**

The relevant point of contact for requesting additional information about the data asset. The point of contact should be enduring (e.g. role-based) as opposed to a specific individual (e.g. a chief investigator).

This may be different to the point of contact for requesting access to the data asset (see Request POC [4.4.2] below).

Email (or URL to web form) for the point of contact.


====================================================== =========== ========== ====================================================================================================================== ============================ =====
Source metadata field                                  Occurrences Input type Example input                                                                                                          Controlled vocabulary source Notes
====================================================== =========== ========== ====================================================================================================================== ============================ =====
ANZCTR Step 10 - Contact person for scientific queries      1         Text    Medical Director for the Study, +61 2 9562 5333, Department of Clinical Trials, Holt University, enquiries@holt.edu.au
====================================================== =========== ========== ====================================================================================================================== ============================ =====


.. _4.4.2:

4.4.2 Request point of contact
==============================

======== ==========
Required Repeatable
======== ==========
Yes      Yes
======== ==========

**Definition**

The relevant point of contact for requesting access to the data asset (e.g. the data custodian). The point of contact should be enduring (e.g. role-based) as opposed to a specific individual (e.g. a chief investigator).

This may be a different point of contact than that used for enquiries about the data asset (see Enquiries (4.4.1)).

This field will be used by the HeSANDA Federations Service to direct where data requests will be sent. 

The Request Point of Contact will need to be separately registered with ARDC to enable this functionality.


============================ =========== ========== ============================= ============================ =====
Source metadata field        Occurrences Input type Example input                 Controlled vocabulary source Notes
============================ =========== ========== ============================= ============================ =====
DataCite 7 Contributor                   n/a                                    
DataCite 7.a contributorType 1           Text       Must be "Distributor"         DataCite                    
DataCite 7.1 contributorName
============================ =========== ========== ============================= ============================ =====


*Metadata fields:*

.. contents:: :local:

.. rubric:: Example XML

.. code:: xml

  <contributors>
      <contributor contributorType="Data Collector">
          <contributorName nameType="Personal">Garcia, Sofia</contributorName>
          <givenName>Sofia</givenName>
          <familyName>Garcia</familyName>
          <nameIdentifier schemeURI="https://orcid.org/" nameIdentifierScheme="ORCID">0000-0001-5727-2427</nameIdentifier>
          <affiliation affiliationIdentifier="https://ror.org/03efmqc40" affiiationIdentifierScheme="ROR" schemeURI="https://ror.org">Arizona State University</affiliation>
      </contributor>
      <contributor contributorType="HostingInstitution">
          <contributorName xml:lang="en" nameType="Organizational">California Digital Library</contributorName>
          <nameIdentifier schemeURI="https://ror.org/" nameIdentifierScheme="ROR">https://ror.org/03yrm5c26</nameIdentifier>
      </contributor>
  </contributors>

.. _7.a:

DataCite 7.a contributorType
~~~~~~~~~~~~~~~~~~~

**Occurrences:** 1

**Input type:** Text

**Example input:** Must be "Distributor"

**Controlled vocabulary source:**

**Notes:**

.. _7.1:

DataCite 7.1 contributorName
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Occurrences:** 1

**Input type:** Text from list

**Example input:** Australasian Leukaemia and Lymphoma Group (ALLG)

**Controlled vocabulary source:** List of all HeSANDA data providers

**Notes:**

.. _7.1.a:

DataCite 7.1.a nameType
^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 1

**Input type:** Text from list

**Example input:** Must be "Organizational"

**Controlled vocabulary source:**

**Notes:**

.. _7.4:

DataCite 7.4 nameIdentifier
~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Occurrences:** 0-n

**Input type:** Text

**Example input:** https://ror.org/05t72y326

**Controlled vocabulary source:**

**Notes:** Go to https://ror.org/ to look up the ROR ID for an organisation.

.. _7.4.a:

DataCite 7.4.a nameIdentifierScheme
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 1

**Definition:** The name of the name identifier scheme.

**Allowed values, examples, other constraints:**

If nameIdentifier is used, nameIdentifierScheme is mandatory.

Examples:

* ORCID
* ISNI
* ROR

.. _7.4.b:

DataCite 7.4.b schemeURI
^^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 0-1

**Definition:** The URI of the name identifier scheme.

**Allowed values, examples, other constraints:**

Examples:

* https://orcid.org/
* https://isni.org/
* https://ror.org/


.. _7.5:

DataCite 7.5 affiliation
~~~~~~~~~~~~~~~~~~~~~~~~

**Occurrences:** 0-n

**Definition:** The organizational or institutional affiliation of the contributor.

**Allowed values, examples, other constraints**

Free text.

The contributor's nameType may be *Organizational* or *Personal*. In the case of an organizational contributor, e.g., a research group,
this will often be the name of the institution to which that organization belongs.

Examples:

* German National Library of Science and Technology
* DataCite


.. _7.5.a:

DataCite 7.5.a affiliationIdentifier
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 0-1

**Definition:** Uniquely identifies the organizational affiliation of the contributor.

**Allowed values, examples, other constraints:**

The format is dependent upon scheme.

Examples:

* https://ror.org/04aj4c181
* https://isni.org/isni/0000000492299539

.. _7.5.b:

DataCite 7.5.b affiliationIdentifierScheme
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 1

**Definition:** The name of the affiliation identifier scheme.

**Allowed values, examples, other constraints:**

If affiliationIdentifier is used, affiliationIdentifierScheme is mandatory.

Examples:

* ROR
* ISNI


.. _7.5.c:

DataCite 7.5.c schemeURI
^^^^^^^^^^^^^^^^^^^^^^^^

**Occurrences:** 0-1

**Definition:** URI of the affiliation identifier scheme.

**Allowed values, examples, other constraints:**

Examples:

* https://ror.org/
* https://isni.org/