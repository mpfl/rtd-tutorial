HeSANDA metadata profile and technical implementation
=====================================================

**Document history**

.. raw:: html

   <table>

.. raw:: html

   <tr>

.. raw:: html

   <td>

Version

.. raw:: html

   </td>

.. raw:: html

   <td>

Date

.. raw:: html

   </td>

.. raw:: html

   <td>

Description

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

0.1

.. raw:: html

   </td>

.. raw:: html

   <td>

28/09/2022

.. raw:: html

   </td>

.. raw:: html

   <td>

Draft release for consultation

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.0

.. raw:: html

   </td>

.. raw:: html

   <td>

16/12/2022

.. raw:: html

   </td>

.. raw:: html

   <td>

First major release

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   </table>

**Introduction**
----------------

This document outlines HeSANDA’s information requirements and metadata
profile. These requirements have been designed such that they can be
fulfilled using two pre-existing metadata sources: the Australian New
Zealand Clinical Trials Registry (ANZCTR) and DataCite.

The left-hand side of the table below lists the information categories
and attributes required for data discovery and the functionality of
HeSANDA’s Federation Service. The right-hand side of the table then
indicates how each requirement can be fulfilled using metadata sourced
from ANZCTR and DataCite.

Please note:

1. The metadata profile has been designed such that HeSANDA requires a
   minimum number of fields beyond what is required by ANZCTR and
   DataCite. These are:

-  DataCite 6 Subject (for HeSANDA information requirement 2.3.1)
-  DataCite 7 Contributor (for HeSANDA information requirement 4.4.2)
-  DataCite 12 Related Identifier (for HeSANDA information requirement
   2.1)
-  DataCite 17 Description (for HeSANDA information requirement 1.10 and
   3.2)

2. Fields that are critical to the technical function of HeSANDA are
   highlighted in orange.
3. The following HeSANDA information requirements can be fulfilled using
   both ANZCTR and DataCite metadata:

-  2.1 Study identifier
-  2.4 Funding sources
-  2.7 Study protocol
-  2.7a Data dictionary
-  4.1 Permitted uses

   ANZCTR metadata is required in all cases. With the exception of
   requirement 2.1 (Study identifier), DataCite metadata is optional.
   For further information, refer to the description section in the
   table below.

4. A DataCite field may have one or more subfields, which may or may not
   be required. The Occurrences column indicates whether a subfield is
   required, optional, and even repeatable.

-  0-1 - Optional but not repeatable
-  0-n - Optional and repeatable
-  1 - Required but not repeatable
-  1-n - Required and repeatable

5. This document refers to `Version 4.4 of the DataCite
   Schema <https://schema.datacite.org/meta/kernel-4.4/doc/DataCite-MetadataKernel_v4.4.pdf>`__.
6. Each dataset will require a landing page. DataCite provides guidance
   on `best practices for landing
   pages <https://support.datacite.org/docs/landing-pages>`__. Please
   contact ARDC if you need support implementing these requirements.

`Please contact
ARDC <https://ardc.edu.au/contact-us/#:~:text=You%20can%20also%20call%20us,touch%20with%20the%20right%20person.>`__
to discuss any issues fulfilling these requirements via ANZCTR and
DataCite.

Related information:

-  The `DataCite support site <https://support.datacite.org/>`__ is an
   excellent source of information on how to work with DataCite systems.

.. raw:: html

   <table>

.. raw:: html

   <tr>

.. raw:: html

   <td colspan="6">

HeSANDA information requirements

.. raw:: html

   </td>

.. raw:: html

   <td colspan="6">

Metadata sources

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

Category

.. raw:: html

   </td>

.. raw:: html

   <td>

ID

.. raw:: html

   </td>

.. raw:: html

   <td>

Name

.. raw:: html

   </td>

.. raw:: html

   <td>

Required/ Optional

.. raw:: html

   </td>

.. raw:: html

   <td>

Repeatable

.. raw:: html

   </td>

.. raw:: html

   <td>

Definition

.. raw:: html

   </td>

.. raw:: html

   <td>

Source metadata field

.. raw:: html

   </td>

.. raw:: html

   <td>

Occurrences

.. raw:: html

   </td>

.. raw:: html

   <td>

Input type

.. raw:: html

   </td>

.. raw:: html

   <td>

Example input

.. raw:: html

   </td>

.. raw:: html

   <td>

Controlled vocabulary source

.. raw:: html

   </td>

.. raw:: html

   <td>

Notes

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="59">

.. raw:: html

   <h3>

Reference

.. raw:: html

   </h3>

Elements in this category contain essential reference information for
the data asset

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

1.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Primary Identifier

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

N

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

A DataCite DOI is required. This is a globally unique and resolvable
persistent identifier assigned to the data asset.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 1 Identifier

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

10.1080/15588742.2015.1017687

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 1.a Identifier Type

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

MUST be “DOI”

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="12">

1.2

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="12">

Creator

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="12">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="12">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="12" >

Names of the individual(s) or entity(ies) who created the data asset. 1
These could be the main researchers involved in producing the data, or
the authors of the publication, in priority order. To supply multiple
creators, repeat this

.. raw:: html

   <p>

Property. May be a corporate/institutional or personal name. May also
include affiliation for personal names.

.. raw:: html

   <p>

\*The inclusion of ORCID for individuals and ROR identifiers for
organisations is strongly recommended.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 2 Creator

.. raw:: html

   </td>

.. raw:: html

   <td>

1-n

.. raw:: html

   </td>

.. raw:: html

   <td>

n/a

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.1 creatorName

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Jane Doe

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.1.a nameType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Personal

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

Organizational

.. raw:: html

   <li>

Personal

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.2 givenName

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Jane

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.3 familyName

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Doe

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.4 nameIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://orcid.org/0000-0000-0001-0003

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.4.a nameIdentifierScheme

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

ORCID

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

ORCID

.. raw:: html

   <li>

ISNI

.. raw:: html

   <li>

ROR

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.4.b schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

https://orcid.org/

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

https://orcid.org/

.. raw:: html

   <li>

https://isni.org

.. raw:: html

   <li>

https://ror.org/

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.5 affiliation

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Holt University

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.5.a affiliationIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://ror.org/02czsnj07

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.5.b affiliationIdentifierSche

.. raw:: html

   <p>

me

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Test from list

.. raw:: html

   </td>

.. raw:: html

   <td>

ROR

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

ISNI

.. raw:: html

   <li>

ROR

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 2.5.c SchemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

https://ror.org/

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

https://isni.org

.. raw:: html

   <li>

https://ror.org/

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="13">

1.2.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="13">

Contributors

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="13">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="13">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="13" >

These are contributors in addition to the creators, ie. the institution
or person responsible for collecting, managing, distributing, or
otherwise contributing to the development of the resource. To supply
multiple contributors, repeat this property.

.. raw:: html

   <p>

\*The inclusion of ORCID for individuals and ROR identifiers for
organisations is strongly recommended.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 7 Contributor

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

n/a

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.a contributorType

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   <ul>

.. raw:: html

   <li>

ContactPerson

.. raw:: html

   <li>

DataCollector

.. raw:: html

   <li>

DataCurator

.. raw:: html

   <li>

DataManager

.. raw:: html

   <li>

Distributor

.. raw:: html

   <li>

Editor

.. raw:: html

   <li>

HostingInstitution

.. raw:: html

   <li>

Producer

.. raw:: html

   <li>

ProjectLeader

.. raw:: html

   <li>

ProjectManager

.. raw:: html

   <li>

ProjectMember

.. raw:: html

   <li>

RegistrationAgency

.. raw:: html

   <li>

RegistrationAuthority

.. raw:: html

   <li>

RelatedPerson

.. raw:: html

   <li>

Researcher

.. raw:: html

   <li>

ResearchGroup

.. raw:: html

   <li>

RightsHolder

.. raw:: html

   <li>

Sponsor

.. raw:: html

   <li>

Supervisor

.. raw:: html

   <li>

WorkPackageLeader

.. raw:: html

   <li>

Other

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.1 contributorName

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Jane Doe

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.1.a nameType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Personal

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

Organizational

.. raw:: html

   <li>

Personal

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.2 givenName

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Jane

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.3 familyName

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Doe

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.4 nameIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://orcid.org/0000-0000-0001-0003

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.4.a nameIdentifierScheme

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

ORCID

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

ORCID

.. raw:: html

   <li>

ISNI

.. raw:: html

   <li>

ROR

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.4.b schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

https://orcid.org/

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

https://orcid.org/

.. raw:: html

   <li>

https://isni.org

.. raw:: html

   <li>

https://ror.org/

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.5 affiliation

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Holt University

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.5.a affiliationIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://ror.org/02czsnj07

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.5.b affiliationIdentifierSche

.. raw:: html

   <p>

me

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Test from list

.. raw:: html

   </td>

.. raw:: html

   <td>

ROR

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

ISNI

.. raw:: html

   <li>

ROR

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.5.c SchemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

https://ror.org/

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

https://isni.org

.. raw:: html

   <li>

https://ror.org/

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="2">

1.3

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Title

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2" >

A name to identify the data asset.

.. raw:: html

   <p>

The name might refer to the research activity/study that produced the
asset and give an indication of its contents.

.. raw:: html

   <p>

Repeat if there other titles such as translations

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 3 Title

.. raw:: html

   </td>

.. raw:: html

   <td>

1-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   <ul>

.. raw:: html

   <li>

Data from Prediction of Incident Dementia: Impact of Impairment in
Instrumental Activities of Daily Living and Mild Cognitive Impairment –
Results from the German Study on Ageing, Cognition and Dementia in
Primary Care Patients (AgeCoDe)

.. raw:: html

   <li>

National Social Life, Health, and Ageing Project (NSHAP): Round 3 and
COVID-19 Study, [United States], 2015-2016, 2020-2021

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 3.a titleType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

AlternativeTitle

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

AlternativeTitle

.. raw:: html

   <li>

Subtitle

.. raw:: html

   <li>

TranslatedTitle

.. raw:: html

   <li>

Other

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

Do not use this field for the main title

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.4

.. raw:: html

   </td>

.. raw:: html

   <td>

Publisher

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

The name of the entity who is making the data asset available.

.. raw:: html

   <p>

The inclusion of an identifier such as VIAF, ISNI, or ROR is strongly
recommended.and will be available from version 4.5 of the DataCite
metadata schema, scheduled to be released in early 2023.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 4 Publisher

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Australasian Leukaemia and Lymphoma Group (ALLG)

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="17">

1.4.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="17">

Geolocation

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="17">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="17">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="17" >

The spatial region where the data was collected or about which the data
is focused.

.. raw:: html

   <p>

Repeat this property to indicate several different locations.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 18 GeoLocation

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   <ul>

.. raw:: html

   <li>

University Hospital Geelong, Bellerine St, Geelong VIC 3220

.. raw:: html

   <li>

Whadjuk Noongar country

.. raw:: html

   <li>

Australia

.. raw:: html

   <li>

Western Australia

.. raw:: html

   <li>

City of Stirling, Western Australia

.. raw:: html

   <li>

An ABS SLA

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 18 is human readable, and could use any number of sources. It
is repeatable if you want to specify a number of Australian states
without implying all states. That is to say, specify Western Australia,
Tasmania, and South Australia rather than simply Australia.

.. raw:: html

   <p>

Only one, if any, of 18.1, 18.2, 18.3, 18.4 should be filled in.

.. raw:: html

   <p>

Refer to pages 29-32 of DataCite Metadata Schema 4.4

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.1 geoLocationPoint

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

One set of coordinates

.. raw:: html

   </td>

.. raw:: html

   <td>

-30.675715,120.025587

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Decimal representation of longitude and latitude, negatives being south
and west, positives being north and east.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.1.1 pointLongitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

120.025587

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.1.2 pointLatitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

-30.675715

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.2 geoLocationBox

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Two sets of coordinates

.. raw:: html

   </td>

.. raw:: html

   <td>

-46.255847,101.661014

.. raw:: html

   <p>

-9.524914,153.468537

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

A box is defined by two geographic points. Left low corner and right
upper corner. Each point is defined by its longitude and latitude.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.2.1 westBoundLongitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

101.661014

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.2.2 eastBoundLongitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

153.468537

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.2.3 southBoundLatitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

-46.255847

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.2.4 northBoundLatitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

-9.524914

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.3 geoLocationPlace

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   <ul>

.. raw:: html

   <li>

Vast, hilltop building housing Australia’s parliament, opened in 1988,
topped by an 81m-high flagpole.

.. raw:: html

   <li>

Traditional lands of the Whadjuk Noongar people of Australia

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4 geoLocationPolygon

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

List of coordinates (at least three to draw a triangle)

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.1 polygonPoint

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

A polygon is delimited by geographic points. Each point is defined by a
longitude latitude pair. The last point should be the same as the first
point.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.1.1 pointLongitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.1.2 pointLatitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.2 inPolygonPoint

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

inPolygonPoint is only necessary to indicate the “inside” of the polygon
if the polygon is larger than half the earth. Otherwise the smallest of
the two areas bounded by the polygon will be used.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.2.1 pointLongitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 18.4.2.2 pointLatitude

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.5.1

.. raw:: html

   </td>

.. raw:: html

   <td>

Dataset Publication Date

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

The year that the data asset was made available, in yyyy format.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 5 PublicationYear

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

1999

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="3">

1.5.2

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Collection Date

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

N

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3" >

A significant date or date range for the dataset, in yyyy-mm-dd format.
See dateType for the significant dates desired.

.. raw:: html

   <p>

This attribute can be used to indicate the date range of data
collection.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 8 Date

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Date

.. raw:: html

   </td>

.. raw:: html

   <td>

2015-07-01T9:00+10:00/2015-07-31T17:00+10:00

.. raw:: html

   <p>

(Indicates a date range of 1 July 2015 at 9:00 AEST to 31 July 2015 at
17:00 AEST)

.. raw:: html

   </td>

.. raw:: html

   <td>

Use RKMS-ISO8601 format

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 8.a dateType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “Collected”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 8.b dateInformation

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Covers time points 1 and 2

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.6.1

.. raw:: html

   </td>

.. raw:: html

   <td>

Resource Type General

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

For IPD: always “Dataset”

.. raw:: html

   <p>

This field clarifies what kind of resource is being provided to HeSANDA,
in its most general terms.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 10.a resourceTypeGeneral

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

MUST be “Dataset”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.6.2

.. raw:: html

   </td>

.. raw:: html

   <td>

Resource Type

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

“Individual Participant Data (IPD)”

.. raw:: html

   <p>

Note: The use of a controlled terminology will be considered.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 10 ResourceType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

MUST be “Individual Participant Data (IPD)”.

.. raw:: html

   </td>

.. raw:: html

   <td>

HeSANDA

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.7

.. raw:: html

   </td>

.. raw:: html

   <td>

Format

.. raw:: html

   </td>

.. raw:: html

   <td>

Optional

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

A description of the technical format in which the data asset will be
shared.

.. raw:: html

   <p>

Note: The convention is still to be confirmed, and the use of a
controlled terminology will be considered.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 14 Format

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

text/csv

.. raw:: html

   </td>

.. raw:: html

   <td>

Refer to IANA’s Media Types list for MIME types.

.. raw:: html

   </td>

.. raw:: html

   <td>

Use file extension or MIME type where possible, e.g., PDF, XML, MPG or
application/pdf, text/xml, video/mpeg.

.. raw:: html

   <p>

A human-readable text description of the files in the dataset, such as
“CT scans of vertebrae”, should go in 3.2 Dataset description (DataCite
field 17)

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

1.8

.. raw:: html

   </td>

.. raw:: html

   <td>

Version

.. raw:: html

   </td>

.. raw:: html

   <td>

Optional

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

The version number of the resource.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 15 Version

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

1.0.0

.. raw:: html

   </td>

.. raw:: html

   <td>

Link to definition of semantic versioning

.. raw:: html

   </td>

.. raw:: html

   <td>

We recommend the use of semantic versioning

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="2">

1.9

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Alternate Identifier

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2" >

An identifier other than the primary Identifier applied to the resource
being registered. This may be any Text of characters which is unique
within its

.. raw:: html

   <p>

domain of issue. May be used for local identifiers. The
AlternateIdentifier should be an additional identifier for the same
instance of the resource (i.e., same location, same file).

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 11 alternateIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

E-GEOD-34814

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 11.a alternateIdentifierType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Local accession number

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="2">

1.10

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

HeSANDA Version

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

N

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

The version number of the HeSANDA metadata profile used for this record.
This must be in the format 1.0.0

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 17 Description

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “HeSANDA 1.0.0”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 17.a descriptionType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be ‘TechnicalInfo’

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

Abstract Methods

.. raw:: html

   <li>

SeriesInformation

.. raw:: html

   <li>

TableOfContents

.. raw:: html

   <li>

TechnicalInfo

.. raw:: html

   <li>

Other

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="66">

.. raw:: html

   <h3>

Origin

.. raw:: html

   </h3>

Elements in this category describe the activity/study that produced the
data asset

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="4">

2.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="4">

Study identifier

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="4">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="4">

N

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="4" >

The trial registration number provided by ANZCTR must be in the DataCite
record to enable the HeSANDA portal to associate a DataCite metadata
record with an ANZCTR metadata record.

.. raw:: html

   <p>

ANZCTR trial registration number

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Trial registration number

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

ACTRN12622000922774

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 12 RelatedIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://www.anzctr.org.au/Trial/Registration/TrialReview.aspx?ACTRN=12622000922774

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

A related identifier cannot be just free text, it must be expressed in
the form of one of the permissible identifiers for the
relatedIdentifierType. URL is probably the most usable, and requires the
ANZCTR trial registration number to be expressed as a URL.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 12.a relatedIdentifierType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “URL”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 12.b relationType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “References”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.2.1

.. raw:: html

   </td>

.. raw:: html

   <td>

Public study name

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

Name of the activity/study, or the ‘public’ title. If there is no such
title the full scientific or protocol title needs to be used.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 1 Public title

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

A randomised controlled trial of low-dose aspirin for the prevention of
fractures in healthy older people: the ASPREE-Fracture sub-study

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.2.2

.. raw:: html

   </td>

.. raw:: html

   <td>

Scientific study name

.. raw:: html

   </td>

.. raw:: html

   <td>

Optional

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

The full scientific name of the activity/study.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 1 Scientific title

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

A double-blind, randomised, placebo-controlled trial to determine the
effects of daily low-dose aspirin (100mg) versus placebo on the risk of
fractures and fall-related hospital presentations in healthy older
adults aged 70 years and over

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.2.3

.. raw:: html

   </td>

.. raw:: html

   <td>

Acronym

.. raw:: html

   </td>

.. raw:: html

   <td>

Optional

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

A concise way of referring to the trial.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 1 Trial acronym

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

ASPREE

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="5">

2.3.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Research area/ Discipline

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5" >

Keywords describing the research area and/or discipline.

.. raw:: html

   <p>

A subject is a term, keyword, classification code or phrase representing
the primary topic or topics covered by a registry object. This
information answers the questions: What subject terms describe the topic
of the object? What is it about?

.. raw:: html

   <p>

HeSANDA requires at least one ANZSRC FOR code specified to the six-digit
level.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 6 Subject

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Endocrinology

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.a subjectScheme

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZSRC Fields of Research

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.b schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://www.abs.gov.au/statistics/classifications/australian-and-new-zealand-standard-research-classification-anzsrc/2020

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.c valueURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.d classificationCode

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

320208

.. raw:: html

   </td>

.. raw:: html

   <td>

This field is for subject schemes like FOR codes, which include
numerical codes for each of the subjects.

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.3.2

.. raw:: html

   </td>

.. raw:: html

   <td>

Activity/ Research study description

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

A description of the activity/study that produced the data asset. Easily
read and understood information about the study; the purpose is to
enable users to find, categorise and evaluate the fitness of a data
asset to their needs based on the activities undertaken during the
study.

.. raw:: html

   <p>

This field supplements the attribute Dataset Description [3.2].

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 9 Brief summary

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

This study aims to investigate the effect of a combined exercise
training program, compared to a sham-placebo control group on skeletal
muscle microvascular blood flow and exercise intolerance in adults
living with atrial fibrillation. Secondary to this, the study aims to
determine the effect of combined exercise training on quality of life,
symptom severity and traditional cardiovascular risk factors.
It is hypothesised that participants in the combined exercise training
group will have an increase in skeletal muscle microvascular blood flow
and exercise tolerance when compared to the sham-placebo control.
Additionally, those randomised to the combined exercise training group
will have an improvement in quality of life, lower symptom severity and
improved cardiovascular risk factors.

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="9">

2.4

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="9">

Funding sources

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="9">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="9">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="9" >

Funding source(s) for the activity/study.

.. raw:: html

   <p>

ANZCTR Step 8 must be provided, as it is an outline of funding received.

.. raw:: html

   <p>

Optionally, more granular funding information can be provided to
DataCite to enable linking between data and projects from the same
funder(s).

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 8 Funding & Sponsors

.. raw:: html

   </td>

.. raw:: html

   <td>

1-n

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Eg.

.. raw:: html

   <p>

Government body

.. raw:: html

   <p>

Name: NHMRC Investigator

.. raw:: html

   <p>

Grant #1174523

.. raw:: html

   <p>

Address: GPO Box 1421 CANBERRA ACT 2601

.. raw:: html

   <p>

Country: Australia

.. raw:: html

   <p>

Primary sponsor type: University

.. raw:: html

   <p>

Name: Sydney School of Public Health, The University of Sydney

.. raw:: html

   <p>

Address Edward Ford Building A27

.. raw:: html

   <p>

The University of Sydney

.. raw:: html

   <p>

Camperdown NSW 2006 Australia

.. raw:: html

   <p>

Country: Australia
Secondary sponsor category: None

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19 FundingReference

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.1 funderName

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Australian Research Council

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.2 funderIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

501100000923

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.2.a funderIdentifierType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Crossref Funder ID

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

.. raw:: html

   <ul>

.. raw:: html

   <li>

Crossref Funder ID

.. raw:: html

   <li>

GRID

.. raw:: html

   <li>

ISNI

.. raw:: html

   <li>

ROR

.. raw:: html

   <li>

Other

.. raw:: html

   </li>

.. raw:: html

   </ul>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.2.b SchemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

https://www.crossref.org/ser

.. raw:: html

   <p>

vices/funder-registry/

.. raw:: html

   </td>

.. raw:: html

   <td>

Examples:

.. raw:: html

   <p>

https://www.crossref.org/ser

.. raw:: html

   <p>

vices/funder-registry/

.. raw:: html

   <p>

https://ror.org/

.. raw:: html

   </td>

.. raw:: html

   <td>

Not available in Fabrica interface

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.3 awardNumber

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

LP0220726

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.3.a awardURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

http://purl.org/au-research/grants/arc/LP0220726

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 19.4 awardTitle

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Development of novel omega-3 enriched poultry products

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.5

.. raw:: html

   </td>

.. raw:: html

   <td>

Activity/ research study type

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

N

.. raw:: html

   </td>

.. raw:: html

   <td>

The type of activity/study that produced the data asset.

.. raw:: html

   </td>

.. raw:: html

   <td colspan="6">

HeSANDA will use the value in field 1.10 to indicate the study type

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.6.1

.. raw:: html

   </td>

.. raw:: html

   <td>

Population

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

The health condition(s) or problem(s) that the activity/study aimed to
assess.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 2 - Health condition(s) or problem(s) studied

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

E.g.

.. raw:: html

   <ol>

.. raw:: html

   <li>

Depression

.. raw:: html

   <li>

Breast cancer

.. raw:: html

   <li>

Medication error

.. raw:: html

   </li>

.. raw:: html

   </ol>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.6.2

.. raw:: html

   </td>

.. raw:: html

   <td>

Intervention/exposure

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

The specific intervention(s) that the activity/study aimed to assess.
Please use ANZCTR conventions as per the following (NB. For
observational studies, provide a brief description of the condition
observed and/or the exposure. The duration of observation must also be
described):

.. raw:: html

   <table>

.. raw:: html

   <tr>

.. raw:: html

   <td>

Brief name

.. raw:: html

   </td>

.. raw:: html

   <td>

Provide the name or a phrase that describes the intervention. If there
are multiple intervention arms, please label with subheadings (e.g. Arm
1, Arm 2, etc.).

.. raw:: html

   <p>

Note: Intervention names should be consistent throughout the form. Avoid
using alternative intervention names for clarity.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

For drug trials

.. raw:: html

   </td>

.. raw:: html

   <td>

Provide the International Nonproprietary Name (INN) of each drug (not
brand/trade names). For an unregistered drug, the generic name, chemical
name, or company serial number is acceptable.

.. raw:: html

   <p>

For each intervention drug, please also specify:

.. raw:: html

   <p>

-  the dose administered, e.g. 5mg once daily;

   .. raw:: html

      <p>

-  the duration of administration, e.g. 4 weeks;

   .. raw:: html

      <p>

-  the mode of administration, e.g. oral tablet, intravenous infusion.

   .. raw:: html

      <p>

   Drug intervention can be sourced from: RxNorm OR AMT codes; or
   proprietary codes e.g. MULTUM; or proxy codes like PBS; WHO ATC
   Anatomic Therapeutic Chemical. Only one Defined Daily Dose (DDD) is
   assigned per ATC code and route of administration; WHO Drug

   .. raw:: html

      <p>

   Non-Drug intervention may be sourced from: SNOMED CT; ICPC2+ coded
   data; LOINC

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   For non-drug trials

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   For each intervention, briefly describe:

   .. raw:: html

      <p>

-  any physical or informational materials that will be used in the
   intervention, including those provided to participants or used in
   intervention delivery or in training of intervention providers;

   .. raw:: html

      <p>

-  each of the procedures, activities, and/or processes used, including
   any enabling or support activities;

   .. raw:: html

      <p>

-  who will deliver the intervention and if relevant, their expertise,
   e.g. dietician with minimum 5 years’ experience;

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      </table>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ANZCTR Step 3 - Description of intervention(s) / exposure

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   “Dexamethasone (10 mg) or placebo was administered 15 to 20 minutes
   before or with the first dose of antibiotic in Arm 1. Studies in
   animals have shown that bacterial lysis, induced by treatment with
   antibiotics, leads to inflammation in the subarachnoid space, which
   may contribute to an unfavourable outcome [references]. These studies
   also show that adjuvant treatment with anti-inflammatory agents, such
   as dexamethasone, reduces both cerebrospinal fluid inflammation and
   neurologic sequelae [references].”

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ?

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   2.6.3

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Comparison/ control

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Required

(for interventional studies only)

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

Details of the comparator treatment and control group type.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 3 - Comparator / control treatment.

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Participants in the control group will receive the standard care from a
specialist gastroenterologist who has about 20 years of working
experience as a medical practitioner and 10 years as a specialist in
internal medicine and gastroenterology.

The standard care includes reassurance and medication targeting the most
troublesome symptoms (including fibre supplementation, anti-depressants,
antispasmodics and anti-diarrhoeal medications for symptom control). The
gastroenterologist will justify the frequency and duration of
consultation according to individual participant’s needs as routine
clinical visits; therefore, the participant’s irritable bowel symptoms
will be monitored throughout the 8-week treatment period (at least two
visits at Week 1 and Week 8).

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

2.6.3a

.. raw:: html

   </td>

.. raw:: html

   <td>

Control group

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

The comparator/control(s) is/are the treatments against which the study
intervention is being compared (e.g. placebo, no treatment, active
control

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 3 - Control group

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

-  Placebo: an inactive or sham treatment that has no treatment value is
   given to the control group, such as sugar pill or saline solution.
-  Active: when the control treatment is active. This includes standard
   care, alternate forms of treatment, no treatment given, or if
   patients act as their own control (crossover study).
-  Uncontrolled: when there is no control group, as in single group
   trials. The same intervention is applied to all subjects in the
   study.
-  Historical: a group of people who received their care in the past,
   i.e. not at the same time as the people receiving the intervention.
   This selection is not applicable for randomised controlled trials.
   The source and time period that historical data was collected needs
   to be described in the ‘Comparator / control treatment’ field.
-  Dose comparison: the comparator group receives the same treatment as
   the intervention group, but in a different dose.

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   2.6.4

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Outcome measures

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Required

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Y

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   The outcome measures at each timepoint in the study.

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ANZCTR - Step 4 Primary outcome(s) and timepoint(s)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Primary Outcome 1: all-cause mortality as assessed by data linkage to
   medical records

Timepoint: at one year after randomisation

Primary Outcome 2: mean Beck depression score

Timepoint: Baseline, 6 weeks (primary timepoint) and 12 weeks after
intervention commencement

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="3">

2.7

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Study protocol

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

A link to the study protocol (or primary publication if the protocol
cannot be provided). A link in the form of a persistent identifier (such
as a DOI) is strongly recommended. If a DOI is not available, a standard
URL is acceptable.

ANZCTR Step 11 must be provided.

Optionally, richer metadata can be provided to DataCite to enable
linking between multiple research outputs.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 11 - What supporting documents are/will

be available?

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

From ANZCTR data field explanation:

-  No other documents available
-  Study protocol
-  Statistical analysis plan
-  Informed consent form
-  Clinical study report
-  Ethical approval
-  Analytic code
-  Other (please specify)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Study protocol

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 11 - How or where can supporting

documents be obtained?

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Free text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://doi.org/10.1080/15588742.2015.1017687

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

See also 2.8 Other research outputs and related publications for
information on DataCite 20 Related item

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Various

.. raw:: html

   </td>

.. raw:: html

   <td>

See 2.8

.. raw:: html

   </td>

.. raw:: html

   <td>

See 2.8

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="3">

2.7a

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Data dictionary

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="3">

A link to the data dictionary. A link in the form of a persistent
identifier (such as a DOI) is strongly recommended. If a DOI is not
available, a standard URL is acceptable.

ANZCTR Step 11 must be provided.

Optionally, richer metadata can be provided to DataCite to enable
linking between multiple research outputs.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 11 - What supporting documents are/will

be available?

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

From ANZCTR data field explanation:

-  No other documents available
-  Study protocol
-  Statistical analysis plan
-  Informed consent form
-  Clinical study report
-  Ethical approval
-  Analytic code
-  Other (please specify)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 11 - How or where can supporting

documents be obtained?

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Free text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://doi.org/10.1080/15588742.2015.1017687

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

See also 2.8 Other research outputs and related publications for
information on DataCite 20 Related item

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="32">

2.8

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="32">

Other research outputs and related publications

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="32">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="32">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="32">

A link in the form of a persistent identifier (such as a DOI) is
strongly recommended. If a DOI is not available, a standard URL is
acceptable.

For biospecimens, please select RelatedItemType as PhysicalObject.

1.  Data quality statement
2.  Analytic code
3.  `CONSORT <http://www.consort-statement.org/>`__\  [1]_\ `statement <http://www.consort-statement.org/>`__
4.  Clinical practice guidelines/recommendations emerging from the trial
5.  Data management plan
6.  Unpublished reports
7.  Statistical analysis plan
8.  Publications, preprints, journal articles and abstracts
9.  Related datasets
10. Case Report Forms/ Data Collection Forms
11. Biospecimens

If requested, we can provide an example per research output and related
publication type.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 11 - What supporting documents are/will

be available?

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

From ANZCTR data field explanation:

-  No other documents available
-  Study protocol
-  Statistical analysis plan
-  Informed consent form
-  Clinical study report
-  Ethical approval
-  Analytic code
-  Other (please specify)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 11 - How or where can supporting

documents be obtained?

OR

ANZCTR Step 12 - Summary results (for publications, preprints, journal
articles, and abstracts, unpublished reports and clinical practice
guidelines)

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Free text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://doi.org/10.1080/15588742.2015.1017687

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20 Related item

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.a relatedItemType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

-  Audiovisual
-  Book
-  BookChapter
-  Collection
-  ComputationalNotebook
-  ConferencePaper
-  ConferenceProceeding
-  DataPaper
-  Dataset
-  Dissertation
-  Event Image
-  InteractiveResource Journal
-  JournalArticle Model
-  OutputManagementPlan
-  PeerReview
-  PhysicalObject
-  Preprint Report
-  Service
-  Software
-  Sound
-  Standard Text
-  Workflow
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.b relationType

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  IsCitedBy Cites
-  IsSupplementTo
-  IsSupplementedBy
-  IsContinuedBy
-  Continues
-  IsDescribedBy
-  Describes
-  HasMetadata
-  IsMetadataFor
-  HasVersion
-  IsVersionOf
-  IsNewVersionOf
-  IsPreviousVersionO
-  IsPartOf
-  HasPart
-  IsPublishedIn
-  IsReferencedBy
-  References
-  IsDocumentedBy
-  Documents
-  IsCompiledBy
-  Compiles
-  IsVariantFormOf
-  IsOriginalFormOf
-  IsIdenticalTo
-  IsReviewedBy
-  Reviews
-  IsDerivedFrom
-  IsSourceOf
-  IsRequiredBy
-  Requires
-  IsObsoletedBy
-  Obsoletes

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Is “IsDerivedFrom” for biospecimens

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.1 relatedItemIdentifier

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   If relatedItemIdentifier is provided, an identical 12.
   RelatedIdentifier is strongly recommended for indexing.

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.1.a relatedItemIdentifie

rType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

-  ARK
-  arXiv
-  Bibcode
-  DOI
-  EAN13
-  EISSN
-  Handle
-  IGSN
-  ISBN
-  ISSN
-  ISTC
-  LISSN
-  LSID
-  PMID
-  PURL
-  UPC
-  URL
-  URN
-  w3id

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.1.b relatedMetadataSch

eme

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Use only with this relation pair: (HasMetadata/IsMetadataFor)

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.1.c schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Use only with this relation pair: (HasMetadata/IsMetadataFor)

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.1.d schemeType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

-  XSD
-  DDT
-  Turtle

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with this relation pair: (HasMetadata/IsMetadataFor)

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.2 Creator

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-n

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Jane Smith
-  HeSANDA University

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.2.1 creatorName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Jane Smith

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.2.1.a nameType

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Organizational
-  Personal (default)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.2.2 givenName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Jane

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.2.3 familyName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Smith

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.3 Title

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1-n

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Journal of the

American Chemical Society

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.3.a titleType

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

-  Alternative
-  Title
-  Subtitle
-  Translated
-  Title
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.4 PublicationYear

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Year

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   2020

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.5 volume

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   8

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with relationType IsPublishedIn

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.6 issue

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   3

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with relationType IsPublishedIn

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.7 number

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   12

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with relationType IsPublishedIn

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.7.a numberType

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  Article
-  Chapter
-  Report
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with relationType IsPublishedIn

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.8 firstPage

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Number

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   3

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Use only with relationType IsPublishedIn

First page of the resource within the related item e.g. chapter, article
or conference paper

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.9 lastPage

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

99

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Use only with relationType IsPublishedIn

Last page of the resource within the related item e.g. chapter, article
or conference paper

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.10 Publisher

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Holt University

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Use only with relationType IsPublishedIn

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.11 edition

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

V 0.1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Use only with relationType IsPublishedIn

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 20.12 Contributor

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

-  Jane Smith
-  Foo Data Centre

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.12.a contributorType

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  ContactPerson
-  DataCollector
-  DataCurator
-  DataManager
-  Distributor
-  Editor
-  HostingInstitution
-  Producer
-  ProjectLeader
-  ProjectManager
-  ProjectMember
-  RegistrationAgency
-  RegistrationAuthority
-  RelatedPerson
-  Researcher
-  ResearchGroup
-  RightsHolder
-  Sponsor
-  Supervisor
-  WorkPackageLeader
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.12.1 contributorName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Jane Smith

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.12.1. a nameType

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  Organizational
-  Personal (default)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.12.2 givenName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Jane

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 20.12.3 familyName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Smith

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td rowspan="15" >

Content
~~~~~~~

*Elements in this section describe the contents of the data asset*

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

3.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Keyword

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="5">

Qualifying words that help the reader understand more about the dataset,
that can help differentiate this dataset from others.

These Text keywords are not constrained by vocabularies, however the use
of vocabularies (e.g. MeSH, SNOMED, etc) is strongly recommended.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 6 Subject

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Blood pressure

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.a subjectScheme

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

MeSH

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.b schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

http://id.nlm.nih.gov/mesh/

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.c valueURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://id.nlm.nih.gov/mesh/D001794

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 6.d classificationCode

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Number

.. raw:: html

   </td>

.. raw:: html

   <td>

D001794

(where D001794 is the classification code associated with the subject
term “Blood pressure” in the MeSH scheme)

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="2">

3.2

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Dataset description

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

N

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

A description containing easily read and understood information about
the data asset. The purpose is to enable users not involved in the
original study to find, categorise and evaluate the fitness of a data
asset to their needs.

It is recommended that the dataset description include:

-  the sample size (3.2)
-  sample description (3.3.2)
-  assessment stage/ timepoint (3.3.3)

for that individual data asset.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 17 Description

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Haemoglobin levels observed in blood samples of 50 trial participants
taken at timepoint 3.

Timepoint 3 - 1 hour, 3 hours (primary timepoint) and 6 hours post dose

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 17.a descriptionType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “Abstract”

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

-  Abstract
-  Methods
-  TableOfContents
-  TechnicalInfo
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   3.3.1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Sample Size

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Optional

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Y

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   A positive integer representing the number of participant records
   available in the data asset.

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ANZCTR Step 7 - Final sample size

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Number

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   35

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Please note that the ANZCTR metadata describes the sample for the
   whole trial; individual datasets produced by the trial may be derived
   from subsets of the whole sample.

The sample size for individual datasets should appear in 3.2 Dataset
description

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="6">

3.3.2

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Sample description

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Descriptive statistics of age, sex, disease vs control, cultural
background.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 5 - Eligibility - Key inclusion criteria

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

-  | Minimum Age : 12 years
   | Maximum Age: 25 years
   | Sex: F

-  | Minimum Age : 0 years
   | Maximum Age: 3 years
   | Sex: M

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Please note that the ANZCTR metadata describes the sample for the
   whole trial; individual datasets produced by the trial may be derived
   from subsets of the whole sample.

The sample description for individual datasets should appear in 3.2
Dataset description.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

ANZCTR Step 5 - Eligibility - Minimum age

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Number and option from provided list

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

-  Years
-  Months
-  Weeks
-  Days
-  Hours

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 5 - Eligibility - Maximum age

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Number and option from provided list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Years
-  Months
-  Weeks
-  Days
-  Hours

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 5 - Eligibility - Gender

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1-3

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Males
-  Females
-  Both males and females

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 5 - Eligibility - Can healthy volunteers participate?

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Yes
-  No

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   ANZCTR Step 5 - Eligibility - Key exclusion criteria

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

-  Diagnosis of sleep apnea or any other chronic respiratory disease
-  Any acute or chronic condition that would limit the ability of the
   patient to participate in the study
-  Refusal to give informed consent

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   3.3.3

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Assessment stage/ timepoint

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Optional

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Y

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   The assessment stage or timepoint at which the dataset was collected.
   This is a subset of the indicated timepoints in **2.6.4.**

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   DataCite 17 Description (see 3.2 Dataset description)

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   The assessment state/timepoints for individual datasets should appear
   in 3.2 Dataset description.

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td rowspan="21" >

Access
~~~~~~

*Elements in this section contain information about accessing/use of the
data asset*

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

4.1

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Permitted uses

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="6">

A brief general description of the kinds of permitted secondary uses of
the dataset. These uses would generally be dictated by the terms of
consent and/or HREC approval. A more detailed description of the terms
of use would be provided via the **Data Sharing Policy [4.2]**\ and*\*
Rights/Licence [4.3] \**attribute.

It is assumed that requests to access data for secondary use may require
review on a case by case basis. As such, this attribute is used to
indicate the kinds of requests that align with existing consent/HREC
approval.

ANZCTR Step 11 must be provided.

Optionally, more structured metadata can be provided to DataCite to
enable machine-readability of permitted uses, which the HeSANDA portal
can use to provide a better user experience.

| If providing metadata to DataCite, DUO - the Data Use Ontology - is
  recommended here, if appropriate for the dataset. `Read an
  introduction <https://doi.org/10.1016/j.xgen.2021.100028>`__ here.
| Note: DUO terms can currently only be applied using the DataCite
  metadata schema.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 11 - ’Available for what types of analyses?’

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Any purpose, only to achieve the

aims in the approved proposal, for IPD meta-analyses, etc.

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16 Rights

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

population origins/ancestry research

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16.a rightsURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

http://purl.obolibrary.org/obo/DUO_0000011

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16.b rightsIdentifier

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

DUO_0000011

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Not available in Fabrica interface

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16.c rightsIdentifierScheme

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

DUO

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Not available in Fabrica interface

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16.d schemeURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

http://purl.obolibrary.org/obo/duo.owl

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

Not available in Fabrica interface

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

4.2

.. raw:: html

   </td>

.. raw:: html

   <td>

Data sharing policy

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

A policy statement and/or set of procedures that addresses secondary use
of the dataset. This would commonly be presented as a publicly
accessible document or webpage that details items such as the following:

-  Governance roles and responsibilities
-  Regulatory requirements (e.g. legal, ethical, funding)
-  Requirements for requesting data access (e.g. procedures, time
   frames, costs)
-  Requirements for management and handling of shared data (e.g. storage
   and disposal, reporting)

Data sharing policies are broad in nature and represent the general
position of the data custodian regarding sharing of the dataset. It is
common for a specific data sharing agreement to be signed by the
requestor and custodian prior to the release of data in response to a
data request. Data sharing agreements are contracts between two or more
parties that articulate the specific terms and conditions for the
sharing of data for a specific purpose. The data sharing policy may be
cited in the terms of the data sharing agreement if required.

See also **Permitted uses [4.1]** and **Rights/Licence [4.3]**.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 11: Data sharing statement

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

See 2.8 Other research outputs and related publications for a more
detailed breakdown of DataCite 20 relatedItem. Use relatedItemType
“Text” for a data sharing policy.

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="2">

4.3

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Rights/ Licence

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Optional

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="2">

Any intellectual property rights and/or licensing information regarding
sharing and/or secondary use of the data object. This may be expressed
as:

-  A textual statement of the rights management associated with the
   asset
-  A legal document under which the asset is made available (e.g. a data
   sharing agreement template)

See also **Permitted uses [4.1]**\ and **Data sharing policy [4.2]**.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 16 Rights

.. raw:: html

   </td>

.. raw:: html

   <td>

0-n

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

RESTRICTIVE LICENCE AGREEMENT for USE OF MATERIAL [insert description]
between THE SUPPLIER [insert Supplier’s name] and THE CUSTOMER [insert
Customer’s name]

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 16.a rightsURI

.. raw:: html

   </td>

.. raw:: html

   <td>

0-1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

https://licenceagreementtemplate.uni.edu.au/

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

4.4.1

.. raw:: html

   </td>

.. raw:: html

   <td>

Enquiries

.. raw:: html

   </td>

.. raw:: html

   <td>

Required

.. raw:: html

   </td>

.. raw:: html

   <td>

Y

.. raw:: html

   </td>

.. raw:: html

   <td>

The relevant point of contact for requesting additional information
about the data asset. The point of contact should be enduring
(e.g. role-based) as opposed to a specific individual (e.g. a chief
investigator).

This may be different to the point of contact for requesting access to
the data asset (see **Request POC** **[4.4.2]** below).

Email (or URL to web form) for the point of contact.

.. raw:: html

   </td>

.. raw:: html

   <td>

ANZCTR Step 10 - Contact person for scientific queries

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text

.. raw:: html

   </td>

.. raw:: html

   <td>

Medical Director for the Study, +61 2 9562 5333, Department of Clinical
Trials, Holt University, enquiries@holt.edu.au

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td rowspan="11">

4.4.2

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="11">

Request point of contact

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="11">

Required

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="11">

Y

.. raw:: html

   </td>

.. raw:: html

   <td rowspan="11">

The relevant point of contact for requesting access to the data asset
(e.g. the data custodian). The point of contact should be enduring
(e.g. role-based) as opposed to a specific individual (e.g. a chief
investigator).

This may be a different point of contact than that used for enquiries
about the data asset (see **Enquiries [4.4.1]** above).

This field will be used by the HeSANDA Federations Service to direct
where data requests will be sent.

The Request Point of Contact will need to be separately registered with
ARDC to enable this functionality.

.. raw:: html

   </td>

.. raw:: html

   <td>

DataCite 7 Contributor

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

n/a

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.a contributorType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

n/a

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “Distributor”

.. raw:: html

   </td>

.. raw:: html

   <td>

-  ContactPerson
-  DataCollector
-  DataCurator
-  DataManager
-  Distributor
-  Editor
-  HostingInstitution
-  Producer
-  ProjectLeader
-  ProjectManager
-  ProjectMember
-  RegistrationAgency
-  RegistrationAuthority
-  RelatedPerson
-  Researcher
-  ResearchGroup
-  RightsHolder
-  Sponsor
-  Supervisor
-  WorkPackageLeader
-  Other

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.1 contributorName

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Australasian Leukaemia

and Lymphoma Group (ALLG)

.. raw:: html

   </td>

.. raw:: html

   <td>

List of all HeSANDA data providers

.. raw:: html

   </td>

.. raw:: html

   <td>

.. raw:: html

   </td>

.. raw:: html

   </tr>

.. raw:: html

   <tr>

.. raw:: html

   <td>

DataCite 7.1.a nameType

.. raw:: html

   </td>

.. raw:: html

   <td>

1

.. raw:: html

   </td>

.. raw:: html

   <td>

Text from list

.. raw:: html

   </td>

.. raw:: html

   <td>

Must be “Organizational”

.. raw:: html

   </td>

.. raw:: html

   <td>

From the DataCite metadata schema

-  Organizational
-  Personal

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.4 nameIdentifier

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-n

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   https://ror.org/05t72y326

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.4.a nameIdentifierScheme

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ROR

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  ISNI
-  ROR

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.4.b schemeURI

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   https://ror.org/

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  https://isni.org
-  https://ror.org/

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.5 affiliation

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-n

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Holt University

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.5.a affiliationIdentifier

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-n

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   https://ror.org/02czsnj07

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.5.b affiliationIdentifierScheme

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Test from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   ROR

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  ISNI
-  ROR

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      <tr>

   .. raw:: html

      <td>

   DataCite 7.5.c SchemeURI

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   0-1

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   Text from list

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   https://ror.org/

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   From the DataCite metadata schema

-  https://isni.org
-  https://ror.org/

   .. raw:: html

      </td>

   .. raw:: html

      <td>

   .. raw:: html

      </td>

   .. raw:: html

      </tr>

   .. raw:: html

      </table>

.. raw:: html

   <!-- Footnotes themselves at the bottom. -->

Notes
-----

.. [1]
