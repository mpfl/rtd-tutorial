HeSANDA metadata profile and technical implementation
=====================================================

**Document history**


<table>
  <tr>
   <td><strong>Version</strong>
   </td>
   <td><strong>Date</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>0.1
   </td>
   <td>28/09/2022
   </td>
   <td>Draft release for consultation
   </td>
  </tr>
  <tr>
   <td>1.0
   </td>
   <td>16/12/2022
   </td>
   <td>First major release
   </td>
  </tr>
</table>



## **Introduction**

This document outlines HeSANDA’s information requirements and metadata profile. These requirements have been designed such that they can be fulfilled using two pre-existing metadata sources: the Australian New Zealand Clinical Trials Registry (ANZCTR) and DataCite.  

The left-hand side of the table below lists the information categories and attributes required for data discovery and the functionality of HeSANDA’s Federation Service. The right-hand side of the table then indicates how each requirement can be fulfilled using metadata sourced from ANZCTR and DataCite. 

Please note: 



1. The metadata profile has been designed such that HeSANDA requires a minimum number of fields beyond what is required by ANZCTR and DataCite. These are: 
* DataCite 6 Subject (for HeSANDA information requirement 2.3.1) 
* DataCite 7 Contributor (for HeSANDA information requirement 4.4.2) 
* DataCite 12 Related Identifier (for HeSANDA information requirement 2.1) 
* DataCite 17 Description (for HeSANDA information requirement 1.10 and 3.2) 
2. Fields that are critical to the technical function of HeSANDA are highlighted in orange. 
3. The following HeSANDA information requirements can be fulfilled using both ANZCTR and DataCite metadata:
* 2.1 Study identifier
* 2.4 Funding sources
* 2.7 Study protocol
* 2.7a Data dictionary
* 4.1 Permitted uses

    ANZCTR metadata is required in all cases. With the exception of requirement 2.1 (Study identifier), DataCite metadata is optional. For further information, refer to the description section in the table below.

4. A DataCite field may have one or more subfields, which may or may not be required. The Occurrences column indicates whether a subfield is required, optional, and even repeatable.
* 0-1 - Optional but not repeatable
* 0-n - Optional and repeatable
* 1 - Required but not repeatable
* 1-n - Required and repeatable
5. This document refers to [Version 4.4 of the DataCite Schema](https://schema.datacite.org/meta/kernel-4.4/doc/DataCite-MetadataKernel_v4.4.pdf).
6. Each dataset will require a landing page. DataCite provides guidance on [best practices for landing pages](https://support.datacite.org/docs/landing-pages). Please contact ARDC if you need support implementing these requirements.

[Please contact ARDC](https://ardc.edu.au/contact-us/#:~:text=You%20can%20also%20call%20us,touch%20with%20the%20right%20person.) to discuss any issues fulfilling these requirements via ANZCTR and DataCite. 

Related information:



* The [DataCite support site](https://support.datacite.org/) is an excellent source of information on how to work with DataCite systems.




<table>
  <tr>
   <td colspan="6" ><strong>HeSANDA information requirements</strong>
   </td>
   <td colspan="6" ><strong>Metadata sources</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Category</strong>
   </td>
   <td><strong>ID</strong>
   </td>
   <td><strong>Name</strong>
   </td>
   <td><strong>Required/ Optional</strong>
   </td>
   <td><strong>Repeatable</strong>
   </td>
   <td><strong>Definition</strong>
   </td>
   <td><strong>Source metadata field</strong>
   </td>
   <td><strong>Occurrences</strong>
   </td>
   <td><strong>Input type</strong>
   </td>
   <td><strong>Example input</strong>
   </td>
   <td><strong>Controlled vocabulary source</strong>
   </td>
   <td><strong>Notes</strong>
   </td>
  </tr>
  <tr>
   <td rowspan="59" >
<h3>Reference</h3>

<em>Elements in this category contain essential reference information for the data asset</em>
   </td>
   <td rowspan="2" >1.1
   </td>
   <td rowspan="2" >Primary Identifier
   </td>
   <td rowspan="2" >Required
   </td>
   <td rowspan="2" >N
   </td>
   <td rowspan="2" >A DataCite DOI is required. This is a globally unique and resolvable persistent identifier assigned to the data asset. 
   </td>
   <td>DataCite 1 Identifier
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>10.1080/15588742.2015.1017687
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 1.a Identifier Type
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>MUST be “DOI”
   </td>
   <td>DataCite
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="12" >1.2
   </td>
   <td rowspan="12" >Creator
   </td>
   <td rowspan="12" >Required
   </td>
   <td rowspan="12" >Y
   </td>
   <td rowspan="12" >Names of the individual(s) or entity(ies) who created the data asset. 1 These could be the  main researchers involved in producing the data, or the authors of the publication, in priority order. To supply multiple creators, repeat this
<p>
Property. May be a corporate/institutional or personal name. May also include affiliation for personal names.
<p>
*The inclusion of ORCID for individuals and ROR identifiers for organisations is strongly recommended.
   </td>
   <td>DataCite 2 Creator 
   </td>
   <td>1-n
   </td>
   <td>n/a
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.1 creatorName
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>Jane Doe
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.1.a nameType 
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>Personal
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>Organizational

<li>Personal
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.2 givenName
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Jane
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.3 familyName
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Doe
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.4 nameIdentifier
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>https://orcid.org/0000-0000-0001-0003
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.4.a nameIdentifierScheme
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>ORCID
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>ORCID

<li>ISNI

<li>ROR
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.4.b schemeURI
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>https://orcid.org/
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>https://orcid.org/

<li>https://isni.org

<li>https://ror.org/
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.5 affiliation
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>Holt University
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.5.a affiliationIdentifier 
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>https://ror.org/02czsnj07
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.5.b affiliationIdentifierSche
<p>
me
   </td>
   <td>1
   </td>
   <td>Test from list
   </td>
   <td>ROR
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>ISNI

<li>ROR
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 2.5.c SchemeURI 
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>https://ror.org/
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>https://isni.org

<li>https://ror.org/
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="13" >1.2.1
   </td>
   <td rowspan="13" >Contributors
   </td>
   <td rowspan="13" >Optional
   </td>
   <td rowspan="13" >Y
   </td>
   <td rowspan="13" >These are contributors in addition to the creators, ie. the institution or person responsible for collecting, managing, distributing, or otherwise contributing to the development of the resource. To supply multiple contributors, repeat this property.
<p>
*The inclusion of ORCID for individuals and ROR identifiers for organisations is strongly recommended.
   </td>
   <td>DataCite 7 Contributor 
   </td>
   <td>
   </td>
   <td>n/a
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.a contributorType
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
<ul>

<li>ContactPerson

<li>DataCollector

<li>DataCurator

<li>DataManager

<li>Distributor

<li>Editor

<li>HostingInstitution

<li>Producer

<li>ProjectLeader

<li>ProjectManager

<li>ProjectMember

<li>RegistrationAgency

<li>RegistrationAuthority

<li>RelatedPerson

<li>Researcher

<li>ResearchGroup

<li>RightsHolder

<li>Sponsor

<li>Supervisor

<li>WorkPackageLeader

<li>Other
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.1 contributorName
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>Jane Doe
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.1.a nameType 
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>Personal
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>Organizational

<li>Personal
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.2 givenName
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Jane
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.3 familyName
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Doe
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.4 nameIdentifier
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>https://orcid.org/0000-0000-0001-0003
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.4.a nameIdentifierScheme
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>ORCID
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>ORCID

<li>ISNI

<li>ROR
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.4.b schemeURI
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>https://orcid.org/
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>https://orcid.org/

<li>https://isni.org

<li>https://ror.org/
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5 affiliation
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>Holt University
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5.a affiliationIdentifier 
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>https://ror.org/02czsnj07
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5.b affiliationIdentifierSche
<p>
me
   </td>
   <td>1
   </td>
   <td>Test from list
   </td>
   <td>ROR
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>ISNI

<li>ROR
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5.c SchemeURI 
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>https://ror.org/
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>https://isni.org

<li>https://ror.org/
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >1.3
   </td>
   <td rowspan="2" >Title
   </td>
   <td rowspan="2" >Required
   </td>
   <td rowspan="2" >Y
   </td>
   <td rowspan="2" >A name to identify the data asset.
<p>
The name might refer to the research activity/study that produced the asset and give an indication of its contents.
<p>
Repeat if there other titles such as translations
   </td>
   <td>DataCite 3 Title
   </td>
   <td>1-n
   </td>
   <td>Text
   </td>
   <td>
<ul>

<li>Data from Prediction of Incident Dementia: Impact of Impairment in Instrumental Activities of Daily Living and Mild Cognitive Impairment – Results from the German Study on Ageing, Cognition and Dementia in Primary Care Patients (AgeCoDe)

<li>National Social Life, Health, and Ageing Project (NSHAP): Round 3 and COVID-19 Study, [United States], 2015-2016, 2020-2021
</li>
</ul>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 3.a titleType
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>AlternativeTitle
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>AlternativeTitle

<li>Subtitle

<li>TranslatedTitle

<li>Other
</li>
</ul>
   </td>
   <td>Do not use this field for the main title
   </td>
  </tr>
  <tr>
   <td>1.4
   </td>
   <td>Publisher
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>The name of the entity who is making the data asset available. 
<p>
The inclusion of an identifier such as VIAF, ISNI, or ROR is strongly recommended.and will be available from version 4.5 of the DataCite metadata schema, scheduled to be released in early 2023.
   </td>
   <td>DataCite 4 Publisher
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>Australasian Leukaemia and Lymphoma Group (ALLG)
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="17" >1.4.1
   </td>
   <td rowspan="17" >Geolocation
   </td>
   <td rowspan="17" >Optional
   </td>
   <td rowspan="17" >Y
   </td>
   <td rowspan="17" >The spatial region where the data was collected or about which the data is focused. 
<p>
Repeat this property to indicate several different locations.
   </td>
   <td>DataCite 18 GeoLocation 
   </td>
   <td>
   </td>
   <td>Text
   </td>
   <td>
<ul>

<li>University Hospital Geelong, Bellerine St, Geelong VIC 3220

<li>Whadjuk Noongar country

<li>Australia

<li>Western Australia

<li>City of Stirling, Western Australia

<li><a href="https://www.abs.gov.au/AUSSTATS/abs@.nsf/Latestproducts/DEDA554E1B6BB78BCA25791F000EEA26">An ABS SLA</a>
</li>
</ul>
   </td>
   <td>
   </td>
   <td>DataCite 18 is human readable, and could use any number of sources. It is repeatable if you want to specify a number of Australian states without implying all states. That is to say, specify Western Australia, Tasmania, and South Australia rather than simply Australia.
<p>
Only one, if any, of 18.1, 18.2, 18.3, 18.4 should be filled in.
<p>
Refer to pages 29-32 of <a href="https://schema.datacite.org/meta/kernel-4.4/doc/DataCite-MetadataKernel_v4.4.pdf">DataCite Metadata Schema 4.4</a>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.1 geoLocationPoint
   </td>
   <td>
   </td>
   <td>One set of coordinates
   </td>
   <td>-30.675715,120.025587
   </td>
   <td>
   </td>
   <td>Decimal representation of longitude and latitude, negatives being south and west, positives being north and east.
   </td>
  </tr>
  <tr>
   <td>DataCite 18.1.1 pointLongitude 
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>120.025587
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.1.2 pointLatitude
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>-30.675715
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.2 geoLocationBox 
   </td>
   <td>
   </td>
   <td>Two sets of coordinates
   </td>
   <td>-46.255847,101.661014
<p>
-9.524914,153.468537
   </td>
   <td>
   </td>
   <td>A box is defined by two geographic points. Left low corner and right upper corner. Each point is defined by its longitude and latitude.
   </td>
  </tr>
  <tr>
   <td>DataCite 18.2.1 westBoundLongitude
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>101.661014
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.2.2 eastBoundLongitude 
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>153.468537
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.2.3 southBoundLatitude 
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>-46.255847
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.2.4 northBoundLatitude
   </td>
   <td>
   </td>
   <td>Number
   </td>
   <td>-9.524914
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.3 geoLocationPlace
   </td>
   <td>
   </td>
   <td>Text
   </td>
   <td>
<ul>

<li>Vast, hilltop building housing Australia's parliament, opened in 1988, topped by an 81m-high flagpole.

<li>Traditional lands of the Whadjuk Noongar people of Australia
</li>
</ul>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4 geoLocationPolygon
   </td>
   <td>
   </td>
   <td>List of coordinates (at least three to draw a triangle)
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.1 polygonPoint
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>A polygon is delimited by geographic points. Each point is defined by a longitude latitude pair. The last point should be the same as the first point.
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.1.1 pointLongitude
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.1.2 pointLatitude
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.2 inPolygonPoint
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>inPolygonPoint is only necessary to indicate the "inside" of the polygon if the polygon is larger than half the earth. Otherwise the smallest of the two areas bounded by the polygon will be used.
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.2.1 pointLongitude
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 18.4.2.2 pointLatitude 
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>1.5.1
   </td>
   <td>Dataset Publication Date
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>The year that the data asset was made available, in yyyy format.
   </td>
   <td>DataCite 5 PublicationYear
   </td>
   <td>1
   </td>
   <td>Number
   </td>
   <td>1999
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="3" >1.5.2
   </td>
   <td rowspan="3" >Collection Date
   </td>
   <td rowspan="3" >Optional
   </td>
   <td rowspan="3" >N
   </td>
   <td rowspan="3" >A significant date or date range  for the dataset, in yyyy-mm-dd format. See dateType for the significant dates desired.
<p>
This attribute can be used to indicate the date range of data collection.
   </td>
   <td>DataCite 8 Date
   </td>
   <td>0-n
   </td>
   <td>Date
   </td>
   <td>2015-07-01T9:00+10:00/2015-07-31T17:00+10:00
<p>
(Indicates a date range of 1 July 2015 at 9:00 AEST to 31 July 2015 at 17:00 AEST)
   </td>
   <td>Use <a href="http://www.ukoln.ac.uk/metadata/dcmi/collection-RKMS-ISO8601/">RKMS-ISO8601</a> format
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 8.a dateType 
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>Must be “Collected”
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 8.b dateInformation
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Covers time points 1 and 2
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>1.6.1
   </td>
   <td>Resource Type General
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>For IPD: always “Dataset”
<p>
This field clarifies what kind of resource is being provided to HeSANDA, in its most general terms. 
   </td>
   <td>DataCite 10.a resourceTypeGeneral
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>MUST be “Dataset”
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>1.6.2
   </td>
   <td>Resource Type
   </td>
   <td>Required
   </td>
   <td>Y
   </td>
   <td>“Individual Participant Data (IPD)” 
<p>
<em>Note: The use of a controlled terminology will be considered.</em>
   </td>
   <td>DataCite 10 ResourceType
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>MUST be “Individual Participant Data (IPD)”.
   </td>
   <td>HeSANDA
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>1.7
   </td>
   <td>Format
   </td>
   <td>Optional
   </td>
   <td><em>Y</em>
   </td>
   <td>A description of the technical format in which the data asset will be shared.
<p>
<em>Note: The convention is still to be confirmed, and the use of a controlled terminology will be considered.</em>
   </td>
   <td>DataCite 14 Format 
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>text/csv
   </td>
   <td>Refer to <a href="https://www.iana.org/assignments/media-types/media-types.xhtml">IANA’s Media Types list</a> for MIME types.
   </td>
   <td>Use file extension or MIME type where possible, e.g., PDF, XML, MPG or application/pdf, text/xml, video/mpeg.
<p>
A human-readable text description of the files in the dataset, such as “CT scans of vertebrae”, should go in 3.2 Dataset description (DataCite field 17)
   </td>
  </tr>
  <tr>
   <td>1.8
   </td>
   <td>Version
   </td>
   <td>Optional
   </td>
   <td>Y
   </td>
   <td>The version number of the resource.
   </td>
   <td>DataCite 15 Version 
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>1.0.0
   </td>
   <td>Link to definition of semantic versioning
   </td>
   <td>We recommend the use of <a href="https://semver.org/">semantic versioning</a>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >1.9
   </td>
   <td rowspan="2" >Alternate Identifier
   </td>
   <td rowspan="2" >Optional
   </td>
   <td rowspan="2" >Y
   </td>
   <td rowspan="2" >An identifier other than the primary Identifier applied to the resource being registered. This may be any Text of characters which is unique within its
<p>
domain of issue. May be used for local identifiers. The AlternateIdentifier should be an additional identifier for the same instance of the resource (i.e., same location, same file).
   </td>
   <td>DataCite 11 alternateIdentifier
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>E-GEOD-34814
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 11.a alternateIdentifierType 
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>Local accession number
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >1.10
   </td>
   <td rowspan="2" >HeSANDA Version
   </td>
   <td rowspan="2" >Required
   </td>
   <td rowspan="2" >N
   </td>
   <td rowspan="2" >The version number of the HeSANDA metadata profile used for this record. This must be in the format 1.0.0
   </td>
   <td>DataCite 17 Description
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>Must be “HeSANDA 1.0.0”
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 17.a descriptionType
   </td>
   <td>1
   </td>
   <td>Must be ‘TechnicalInfo’
   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>Abstract Methods

<li>SeriesInformation

<li>TableOfContents

<li>TechnicalInfo

<li>Other
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="66" >
<h3>Origin</h3>

Elements in this category describe the activity/study that produced the data asset
   </td>
   <td rowspan="4" >2.1
   </td>
   <td rowspan="4" >Study identifier
   </td>
   <td rowspan="4" >Required
   </td>
   <td rowspan="4" >N
   </td>
   <td rowspan="4" >The trial registration number provided by ANZCTR must be in the DataCite record to enable the HeSANDA portal to associate a DataCite metadata record with an ANZCTR metadata record.
<p>
<a href="https://www.anzctr.org.au/Default.aspx">ANZCTR trial registration number</a> 
   </td>
   <td>ANZCTR Trial registration number
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>ACTRN12622000922774
   </td>
   <td>ANZCTR
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 12 RelatedIdentifier
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>https://www.anzctr.org.au/Trial/Registration/TrialReview.aspx?ACTRN=12622000922774
   </td>
   <td>
   </td>
   <td>A related identifier cannot be just free text, it must be expressed in the form of one of the permissible identifiers for the relatedIdentifierType. URL is probably the most usable, and requires the ANZCTR trial registration number to be expressed as a URL.
   </td>
  </tr>
  <tr>
   <td>DataCite 12.a relatedIdentifierType
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>Must be “URL”
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 12.b relationType
   </td>
   <td>1
   </td>
   <td>Text from list
   </td>
   <td>Must be “References”
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.2.1
   </td>
   <td>Public study name
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>Name of the activity/study, or the ‘public’ title.  If there is no such title the full scientific or protocol title needs to be used.
   </td>
   <td>ANZCTR Step 1 Public title
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>A randomised controlled trial of low-dose aspirin for the prevention of fractures in healthy older people: the ASPREE-Fracture sub-study
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.2.2
   </td>
   <td>Scientific study name
   </td>
   <td>Optional
   </td>
   <td>N
   </td>
   <td>The full scientific name of the activity/study.
   </td>
   <td>ANZCTR Step 1 Scientific title
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>A double-blind, randomised, placebo-controlled trial to determine the effects of daily low-dose aspirin (100mg) versus placebo on the risk of fractures and fall-related hospital presentations in healthy older adults aged 70 years and over
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.2.3
   </td>
   <td>Acronym
   </td>
   <td>Optional
   </td>
   <td>N
   </td>
   <td>A concise way of referring to the trial.
   </td>
   <td>ANZCTR Step 1 Trial acronym
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>ASPREE
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="5" >2.3.1
   </td>
   <td rowspan="5" >Research area/ Discipline
   </td>
   <td rowspan="5" >Required
   </td>
   <td rowspan="5" >Y
   </td>
   <td rowspan="5" >Keywords describing the research area and/or discipline.
<p>
A subject is a term, keyword, classification code or phrase representing the primary topic or topics covered by a registry object. This information answers the questions: What subject terms describe the topic of the object? What is it about?
<p>
HeSANDA requires at least one ANZSRC FOR code specified to the six-digit level. 
   </td>
   <td>DataCite 6 Subject
   </td>
   <td>0-n
   </td>
   <td>Text
   </td>
   <td>Endocrinology
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.a subjectScheme 
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>ANZSRC Fields of Research
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.b schemeURI
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>https://www.abs.gov.au/statistics/classifications/australian-and-new-zealand-standard-research-classification-anzsrc/2020
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.c valueURI
   </td>
   <td>0-1
   </td>
   <td>Text
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.d classificationCode
   </td>
   <td>0-1
   </td>
   <td>Number
   </td>
   <td>320208
   </td>
   <td>This field is for subject schemes like FOR codes, which include numerical codes for each of the subjects.
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.3.2
   </td>
   <td>Activity/ Research study description
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>A description of the activity/study that produced the data asset. Easily read and understood information about the study; the purpose is to enable users to find, categorise and evaluate the fitness of a data asset to their needs based on the activities undertaken during the study. 
<p>
This field supplements the attribute <strong>Dataset</strong> <strong>Description [3.2]</strong>.
   </td>
   <td>ANZCTR Step 9 Brief summary
   </td>
   <td>1
   </td>
   <td>Text
   </td>
   <td>This study aims to investigate the effect of a combined exercise training program, compared to a sham-placebo control group on skeletal muscle microvascular blood flow and exercise intolerance in adults living with atrial fibrillation. Secondary to this, the study aims to determine the effect of combined exercise training on quality of life, symptom severity and traditional cardiovascular risk factors. \
 \
It is hypothesised that participants in the combined exercise training group will have an increase in skeletal muscle microvascular blood flow and exercise tolerance when compared to the sham-placebo control. Additionally, those randomised to the combined exercise training group will have an improvement in quality of life, lower symptom severity and improved cardiovascular risk factors.
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="9" >2.4
   </td>
   <td rowspan="9" >Funding sources
   </td>
   <td rowspan="9" >Required
   </td>
   <td rowspan="9" >Y
   </td>
   <td rowspan="9" >Funding source(s) for the activity/study.
<p>
ANZCTR Step 8 must be provided, as it is an outline of funding received.
<p>
Optionally, more granular funding information can be provided to DataCite to enable linking between data and projects from the same funder(s).
   </td>
   <td>ANZCTR Step 8 Funding & Sponsors
   </td>
   <td>1-n
   </td>
   <td>
   </td>
   <td>Eg. 
<p>
Government body
<p>
Name: NHMRC Investigator
<p>
Grant #1174523
<p>
Address: GPO Box 1421 CANBERRA ACT 2601
<p>
Country: Australia
<p>
Primary sponsor type: University
<p>
Name: Sydney School of Public Health, The University of Sydney
<p>
Address	Edward Ford Building A27
<p>
The University of Sydney
<p>
Camperdown NSW 2006 Australia
<p>
Country: Australia \
Secondary sponsor category: None
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19 FundingReference
   </td>
   <td>0-n
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.1 funderName 
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>Australian Research Council
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.2 funderIdentifier 
   </td>
   <td>0-1
   </td>
   <td>
   </td>
   <td>501100000923
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.2.a funderIdentifierType
   </td>
   <td>0-1
   </td>
   <td>Text from list
   </td>
   <td>Crossref Funder ID
   </td>
   <td>From the DataCite metadata schema
<ul>

<li>Crossref Funder ID

<li>GRID

<li>ISNI

<li>ROR

<li>Other
</li>
</ul>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.2.b SchemeURI 
   </td>
   <td>0-1
   </td>
   <td>
   </td>
   <td>https://www.crossref.org/ser
<p>
vices/funder-registry/
   </td>
   <td>Examples:
<p>
https://www.crossref.org/ser
<p>
vices/funder-registry/
<p>
https://ror.org/
   </td>
   <td>Not available in Fabrica interface
   </td>
  </tr>
  <tr>
   <td>DataCite 19.3 awardNumber
   </td>
   <td>0-1
   </td>
   <td>
   </td>
   <td>LP0220726
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.3.a awardURI
   </td>
   <td>0-1
   </td>
   <td>
   </td>
   <td>http://purl.org/au-research/grants/arc/LP0220726
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 19.4 awardTitle 
   </td>
   <td>0-1
   </td>
   <td>
   </td>
   <td>Development of novel omega-3 enriched poultry products
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.5
   </td>
   <td>Activity/ research study type
   </td>
   <td>Required
   </td>
   <td>N
   </td>
   <td>The type of activity/study that produced the data asset.
   </td>
   <td colspan="6" >HeSANDA will use the value in field 1.10 to indicate the study type
   </td>
  </tr>
  <tr>
   <td>2.6.1
   </td>
   <td>Population
   </td>
   <td>Required
   </td>
   <td>Y
   </td>
   <td>The health condition(s) or problem(s) that the activity/study aimed to assess.
   </td>
   <td>ANZCTR Step 2 - Health condition(s) or problem(s) studied
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>E.g. 
<ol>

<li>Depression

<li>Breast cancer

<li>Medication error
</li>
</ol>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.6.2
   </td>
   <td>Intervention/exposure
   </td>
   <td>Required 
   </td>
   <td>Y
   </td>
   <td>The specific intervention(s) that the activity/study aimed to assess. Please use ANZCTR conventions as per the following (NB. For observational studies, provide a brief description of the condition observed and/or the exposure. The duration of observation must also be described):

<table>
  <tr>
   <td>Brief name
   </td>
   <td>Provide the name or a phrase that describes the intervention. If there are multiple intervention arms, please label with subheadings (e.g. Arm 1, Arm 2, etc.). 
<p>
Note: Intervention names should be consistent throughout the form. Avoid using alternative intervention names for clarity.
   </td>
  </tr>
  <tr>
   <td>For drug trials
   </td>
   <td>Provide the International Nonproprietary Name (INN) of each drug (not brand/trade names). For an unregistered drug, the generic name, chemical name, or company serial number is acceptable.
<p>
For each intervention drug, please also specify:
<p>
- the dose administered, e.g. 5mg once daily;
<p>
- the duration of administration, e.g. 4 weeks;
<p>
- the mode of administration, e.g. oral tablet, intravenous infusion.
<p>
Drug intervention can be sourced from: <a href="https://mor.nlm.nih.gov/RxClass/">RxNorm</a> OR <a href="https://audigitalhealth.github.io/ecl-examples/AMT/#:~:text=The%20Australian%20Medicines%20Terminology%20is,of%20human%20patients%20in%20Australia."> AMT</a> codes; or proprietary codes e.g. MULTUM; or proxy codes like PBS; <a href="https://bioportal.bioontology.org/ontologies/ATC">WHO ATC</a> Anatomic Therapeutic Chemical.  Only one Defined Daily Dose (DDD) is assigned per ATC code and route of administration; WHO Drug
<p>
Non-Drug intervention may be sourced from: <a href="https://ontoserver.csiro.au/shrimp">SNOMED CT; ICPC2+</a> coded data; <a href="http://loinc.org/">LOINC</a>
   </td>
  </tr>
  <tr>
   <td>For non-drug trials
   </td>
   <td>For each intervention, briefly describe:
<p>
- any physical or informational materials that will be used in the intervention, including those provided to participants or used in intervention delivery or in training of intervention providers;
<p>
- each of the procedures, activities, and/or processes used, including any enabling or support activities;
<p>
- who will deliver the intervention and if relevant, their expertise, e.g. dietician with minimum 5 years’ experience;
   </td>
  </tr>
</table>


   </td>
   <td>ANZCTR Step 3 - Description of intervention(s) / exposure

   </td>
   <td>1

   </td>
   <td>Text

   </td>
   <td>“Dexamethasone (10 mg) or placebo was administered 15 to 20 minutes before or with the first dose of antibiotic in Arm 1. Studies in animals have shown that bacterial lysis, induced by treatment with antibiotics, leads to inflammation in the subarachnoid space, which may contribute to an unfavourable outcome [references]. These studies also show that adjuvant treatment with anti-inflammatory agents, such as dexamethasone, reduces both cerebrospinal fluid inflammation and neurologic sequelae [references].”

   </td>
   <td>?

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.6.3

   </td>
   <td>Comparison/ control

   </td>
   <td>Required 

(for interventional studies only)

   </td>
   <td>Y

   </td>
   <td>Details of the comparator treatment and control group type. 

   </td>
   <td>ANZCTR Step 3 - Comparator / control treatment.

   </td>
   <td>
   </td>
   <td>Text

   </td>
   <td>
   </td>
   <td>Participants in the control group will receive the standard care from a specialist gastroenterologist who has about 20 years of working experience as a medical practitioner and 10 years as a specialist in internal medicine and gastroenterology.

The standard care includes reassurance and medication targeting the most troublesome symptoms (including fibre supplementation, anti-depressants, antispasmodics and anti-diarrhoeal medications for symptom control). The gastroenterologist will justify the frequency and duration of consultation according to individual participant’s needs as routine clinical visits; therefore, the participant’s irritable bowel symptoms will be monitored throughout the 8-week treatment period (at least two visits at Week 1 and Week 8).

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>2.6.3a

   </td>
   <td>Control group

   </td>
   <td>Required

   </td>
   <td>
   </td>
   <td>The comparator/control(s) is/are the treatments against which the study intervention is being compared (e.g. placebo, no treatment, active control

   </td>
   <td>ANZCTR Step 3 - Control group

   </td>
   <td>
   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>


* Placebo: an inactive or sham treatment that has no treatment value is given to the control group, such as sugar pill or saline solution.
* Active: when the control treatment is active. This includes standard care, alternate forms of treatment, no treatment given, or if patients act as their own control (crossover study).
* Uncontrolled: when there is no control group, as in single group trials. The same intervention is applied to all subjects in the study.
* Historical: a group of people who received their care in the past, i.e. not at the same time as the people receiving the intervention. This selection is not applicable for randomised controlled trials. The source and time period that historical data was collected needs to be described in the ‘Comparator / control treatment’ field.
* Dose comparison: the comparator group receives the same treatment as the intervention group, but in a different dose.
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
2.6.4

   </td>
   <td>Outcome measures

   </td>
   <td>Required

   </td>
   <td>Y

   </td>
   <td>The outcome measures at each timepoint in the study. 

   </td>
   <td>ANZCTR - Step 4 Primary outcome(s) and timepoint(s)

   </td>
   <td>1

   </td>
   <td>Text

   </td>
   <td>Primary Outcome 1: all-cause mortality as assessed by data linkage to medical records

Timepoint: at one year after randomisation

Primary Outcome 2: mean Beck depression score

Timepoint: Baseline, 6 weeks (primary timepoint) and 12 weeks after intervention commencement

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="3" >2.7

   </td>
   <td rowspan="3" >Study protocol

   </td>
   <td rowspan="3" >Required

   </td>
   <td rowspan="3" >Y

   </td>
   <td rowspan="3" >A link to the study protocol (or primary publication if the protocol cannot be provided). A link in the form of a persistent identifier (such as a DOI) is strongly recommended. If a DOI is not available, a standard URL is acceptable.

ANZCTR Step 11 must be provided.

Optionally, richer metadata can be provided to DataCite to enable linking between multiple research outputs.

   </td>
   <td>ANZCTR Step 11 - What supporting documents are/will

be available?

   </td>
   <td>0-n

   </td>
   <td>Text from list

   </td>
   <td>From ANZCTR data field explanation:



* No other documents available
* Study protocol
* Statistical analysis plan
* Informed consent form
* Clinical study report
* Ethical approval
* Analytic code
* Other (please specify)
   </td>
   <td>
Study protocol

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>ANZCTR Step 11 - How or where can supporting

documents be obtained?

   </td>
   <td>1

   </td>
   <td>Free text

   </td>
   <td>https://doi.org/10.1080/15588742.2015.1017687

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>See also 2.8 Other research outputs and related publications for information on DataCite 20 Related item

   </td>
   <td>0-1

   </td>
   <td>Various

   </td>
   <td>See 2.8

   </td>
   <td>See 2.8

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="3" >2.7a

   </td>
   <td rowspan="3" >Data dictionary

   </td>
   <td rowspan="3" >Required

   </td>
   <td rowspan="3" >Y

   </td>
   <td rowspan="3" >A link to the data dictionary. A link in the form of a persistent identifier (such as a DOI) is strongly recommended. If a DOI is not available, a standard URL is acceptable.

ANZCTR Step 11 must be provided.

Optionally, richer metadata can be provided to DataCite to enable linking between multiple research outputs.

   </td>
   <td>ANZCTR Step 11 - What supporting documents are/will

be available?

   </td>
   <td>0-n

   </td>
   <td>Text from list

   </td>
   <td>From ANZCTR data field explanation:



* No other documents available
* Study protocol
* Statistical analysis plan
* Informed consent form
* Clinical study report
* Ethical approval
* Analytic code
* Other (please specify)
   </td>
   <td>
Other 

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>ANZCTR Step 11 - How or where can supporting

documents be obtained?

   </td>
   <td>1

   </td>
   <td>Free text

   </td>
   <td>https://doi.org/10.1080/15588742.2015.1017687

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>See also 2.8 Other research outputs and related publications for information on DataCite 20 Related item

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="32" >2.8

   </td>
   <td rowspan="32" >Other research outputs and related publications

   </td>
   <td rowspan="32" >Optional

   </td>
   <td rowspan="32" >Y

   </td>
   <td rowspan="32" >A link in the form of a persistent identifier (such as a DOI) is strongly recommended. If a DOI is not available, a standard URL is acceptable.

For biospecimens, please select RelatedItemType as PhysicalObject.



1. Data quality statement
2. Analytic code
3. [CONSORT](http://www.consort-statement.org/)[^1][ statement](http://www.consort-statement.org/)
4. Clinical practice guidelines/recommendations emerging from the trial
5. Data management plan
6. Unpublished reports 
7. Statistical analysis plan
8. Publications, preprints, journal articles and abstracts
9. Related datasets
10. Case Report Forms/ Data Collection Forms
11. Biospecimens

If requested, we can provide an example per research output and related publication type.

   </td>
   <td>ANZCTR Step 11 - What supporting documents are/will

be available?

   </td>
   <td>0-n

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From ANZCTR data field explanation:



* No other documents available
* Study protocol
* Statistical analysis plan
* Informed consent form
* Clinical study report
* Ethical approval
* Analytic code
* Other (please specify)
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
ANZCTR Step 11 - How or where can supporting

documents be obtained?

OR

ANZCTR Step 12 - Summary results (for publications, preprints, journal articles, and abstracts, unpublished reports and clinical practice guidelines)

   </td>
   <td>1

   </td>
   <td>Free text

   </td>
   <td>https://doi.org/10.1080/15588742.2015.1017687

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20 Related item

   </td>
   <td>0-n

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.a relatedItemType

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* Audiovisual
* Book
* BookChapter
* Collection
* ComputationalNotebook
* ConferencePaper
* ConferenceProceeding
* DataPaper
* Dataset
* Dissertation
* Event Image
* InteractiveResource Journal
* JournalArticle Model
* OutputManagementPlan
* PeerReview
* PhysicalObject
* Preprint Report
* Service
* Software
* Sound
* Standard Text
* Workflow
* Other 
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.b relationType 

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* IsCitedBy Cites
* IsSupplementTo
* IsSupplementedBy
* IsContinuedBy
* Continues
* IsDescribedBy
* Describes
* HasMetadata
* IsMetadataFor
* HasVersion
* IsVersionOf
* IsNewVersionOf
* IsPreviousVersionO
* IsPartOf
* HasPart
* IsPublishedIn
* IsReferencedBy
* References
* IsDocumentedBy
* Documents
* IsCompiledBy
* Compiles
* IsVariantFormOf
* IsOriginalFormOf 
* IsIdenticalTo
* IsReviewedBy
* Reviews
* IsDerivedFrom
* IsSourceOf
* IsRequiredBy
* Requires
* IsObsoletedBy
* Obsoletes
   </td>
   <td>
Is “IsDerivedFrom” for biospecimens

   </td>
  </tr>
  <tr>
   <td>DataCite 20.1 relatedItemIdentifier

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>If relatedItemIdentifier is provided, an identical 12. RelatedIdentifier is strongly recommended for indexing.

   </td>
  </tr>
  <tr>
   <td>DataCite 20.1.a relatedItemIdentifie

rType

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* ARK 
* arXiv 
* Bibcode
* DOI
* EAN13
* EISSN
* Handle
* IGSN
* ISBN
* ISSN
* ISTC
* LISSN
* LSID
* PMID
* PURL
* UPC
* URL
* URN
* w3id
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.1.b relatedMetadataSch

eme

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>Use only with this relation pair: (HasMetadata/IsMetadataFor)

   </td>
  </tr>
  <tr>
   <td>DataCite 20.1.c schemeURI

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>Use only with this relation pair: (HasMetadata/IsMetadataFor)

   </td>
  </tr>
  <tr>
   <td>DataCite 20.1.d schemeType

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>


* XSD
* DDT
* Turtle
   </td>
   <td>
   </td>
   <td>
Use only with this relation pair: (HasMetadata/IsMetadataFor)

   </td>
  </tr>
  <tr>
   <td>DataCite 20.2 Creator

   </td>
   <td>0-n

   </td>
   <td>
   </td>
   <td>


* Jane Smith
* HeSANDA University
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.2.1 creatorName

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>Jane Smith

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.2.1.a nameType

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>


* Organizational
* Personal (default)
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.2.2 givenName

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>Jane

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.2.3 familyName

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>Smith

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.3 Title

   </td>
   <td>1-n

   </td>
   <td>Text

   </td>
   <td>Journal of the

American Chemical Society

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.3.a titleType 

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* Alternative
* Title
* Subtitle
* Translated
* Title
* Other
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.4 PublicationYear

   </td>
   <td>0-1

   </td>
   <td>Year

   </td>
   <td>2020

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.5 volume

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>8 

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.6 issue

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>3

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.7 number 

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>12

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.7.a numberType

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* Article
* Chapter
* Report
* Other
   </td>
   <td>
Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.8 firstPage

   </td>
   <td>0-1

   </td>
   <td>Number

   </td>
   <td>3

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

First page of the resource within the related item e.g. chapter, article or conference paper

   </td>
  </tr>
  <tr>
   <td>DataCite 20.9 lastPage

   </td>
   <td>0-1

   </td>
   <td>Number

   </td>
   <td>99

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

Last page of the resource within the related item e.g. chapter, article or conference paper

   </td>
  </tr>
  <tr>
   <td>DataCite 20.10 Publisher 

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>Holt University

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.11 edition 

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>V 0.1

   </td>
   <td>
   </td>
   <td>Use only with relationType IsPublishedIn

   </td>
  </tr>
  <tr>
   <td>DataCite 20.12 Contributor 

   </td>
   <td>0-n

   </td>
   <td>
   </td>
   <td>


* Jane Smith
* Foo Data Centre
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.12.a contributorType

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* ContactPerson
* DataCollector
* DataCurator
* DataManager
* Distributor
* Editor
* HostingInstitution
* Producer
* ProjectLeader
* ProjectManager
* ProjectMember
* RegistrationAgency
* RegistrationAuthority
* RelatedPerson
* Researcher
* ResearchGroup
* RightsHolder
* Sponsor
* Supervisor
* WorkPackageLeader
* Other
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.12.1 contributorName

   </td>
   <td>1

   </td>
   <td>
   </td>
   <td>Jane Smith

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.12.1. a nameType 

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>From the DataCite metadata schema



* Organizational
* Personal (default)
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 20.12.2 givenName 

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>Jane

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 20.12.3 familyName 

   </td>
   <td>0-1

   </td>
   <td>
   </td>
   <td>Smith

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="15" >

### Content
_Elements in this section describe the contents of the data asset_

   </td>
   <td rowspan="5" >3.1

   </td>
   <td rowspan="5" >Keyword

   </td>
   <td rowspan="5" >Optional

   </td>
   <td rowspan="5" >Y

   </td>
   <td rowspan="5" >Qualifying words that help the reader understand more about the dataset, that can help differentiate this dataset from others. 

These Text keywords are not constrained by vocabularies, however the use of vocabularies (e.g. MeSH, SNOMED, etc) is strongly recommended.

   </td>
   <td>DataCite 6 Subject

   </td>
   <td>0-n

   </td>
   <td>
   </td>
   <td>Blood pressure

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.a subjectScheme 

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>MeSH

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.b schemeURI

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>http://id.nlm.nih.gov/mesh/

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.c valueURI

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>https://id.nlm.nih.gov/mesh/D001794

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 6.d classificationCode

   </td>
   <td>0-1

   </td>
   <td>Number

   </td>
   <td>D001794

(where D001794 is the classification code associated with the subject term “Blood pressure” in the MeSH scheme)

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >3.2

   </td>
   <td rowspan="2" >Dataset description

   </td>
   <td rowspan="2" >Required

   </td>
   <td rowspan="2" >N

   </td>
   <td rowspan="2" >A description containing easily read and understood information about the data asset. The purpose is to enable users not involved in the original study to find, categorise and evaluate the fitness of a data asset to their needs.

It is recommended that the dataset description include:



* the sample size (3.2)
* sample description (3.3.2)
* assessment stage/ timepoint (3.3.3)

 for that individual data asset.

   </td>
   <td>DataCite 17 Description

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>Haemoglobin levels observed in blood samples of 50 trial participants taken at timepoint 3.

Timepoint 3 - 1 hour, 3 hours (primary timepoint) and 6 hours post dose

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 17.a descriptionType 

   </td>
   <td>1

   </td>
   <td>Must be “Abstract” 

   </td>
   <td>
   </td>
   <td>


* Abstract
* Methods
* TableOfContents
* TechnicalInfo
* Other
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
3.3.1

   </td>
   <td>Sample Size

   </td>
   <td>Optional

   </td>
   <td>Y

   </td>
   <td>A positive integer representing the number of participant records available in the data asset. 

   </td>
   <td>ANZCTR Step 7 - Final sample size

   </td>
   <td>0-1

   </td>
   <td>Number

   </td>
   <td>35

   </td>
   <td>
   </td>
   <td>Please note that the ANZCTR metadata describes the sample for the whole trial; individual datasets produced by the trial may be derived from subsets of the whole sample. 

The sample size for individual datasets should appear in 3.2 Dataset description

   </td>
  </tr>
  <tr>
   <td rowspan="6" >3.3.2

   </td>
   <td rowspan="6" >Sample description

   </td>
   <td rowspan="6" >Required

   </td>
   <td rowspan="6" >Y

   </td>
   <td rowspan="6" >Descriptive statistics of age, sex, disease vs control, cultural background.

 

   </td>
   <td>ANZCTR Step 5 - Eligibility - Key inclusion criteria

   </td>
   <td>1

   </td>
   <td>Text

   </td>
   <td>


* Minimum Age : 12 years \
Maximum Age: 25 years \
Sex: F \

* Minimum Age : 0 years \
Maximum Age: 3 years \
Sex: M \

   </td>
   <td>
   </td>
   <td>
Please note that the ANZCTR metadata describes the sample for the whole trial; individual datasets produced by the trial may be derived from subsets of the whole sample. 

The sample description for individual datasets should appear in 3.2 Dataset description.

   </td>
  </tr>
  <tr>
   <td>ANZCTR Step 5 - Eligibility - Minimum age

   </td>
   <td>1

   </td>
   <td>Number and option from provided list

   </td>
   <td>
   </td>
   <td>


* Years
* Months
* Weeks
* Days
* Hours
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
ANZCTR Step 5 - Eligibility - Maximum age

   </td>
   <td>1

   </td>
   <td>Number and option from provided list

   </td>
   <td>
   </td>
   <td>


* Years
* Months
* Weeks
* Days
* Hours
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
ANZCTR Step 5 - Eligibility - Gender

   </td>
   <td>1-3

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>


* Males
* Females
* Both males and females
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
ANZCTR Step 5 - Eligibility - Can healthy volunteers participate?

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>
   </td>
   <td>


* Yes
* No
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
ANZCTR Step 5 - Eligibility - Key exclusion criteria

   </td>
   <td>
   </td>
   <td>Text

   </td>
   <td>


* Diagnosis of sleep apnea or any other chronic respiratory disease
* Any acute or chronic condition that would limit the ability of the patient to participate in the study
* Refusal to give informed consent
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
3.3.3

   </td>
   <td>Assessment stage/ timepoint

   </td>
   <td>Optional

   </td>
   <td>Y

   </td>
   <td>The assessment stage or timepoint at which the dataset was collected. This is a subset of the indicated timepoints in **2.6.4.**

   </td>
   <td>DataCite 17 Description (see 3.2 Dataset description)

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>The assessment state/timepoints for individual datasets should appear in 3.2 Dataset description.

   </td>
  </tr>
  <tr>
   <td rowspan="21" >

### Access
_Elements in this section contain information about accessing/use of the data asset_

   </td>
   <td rowspan="6" >4.1

   </td>
   <td rowspan="6" >Permitted uses

   </td>
   <td rowspan="6" >Required

   </td>
   <td rowspan="6" >Y

   </td>
   <td rowspan="6" >A brief general description of the kinds of permitted secondary uses of the dataset. These uses would generally be dictated by the terms of consent and/or HREC approval. A more detailed description of the terms of use would be provided via the **Data Sharing Policy [4.2] **and** Rights/Licence [4.3] **attribute.

It is assumed that requests to access data for secondary use may require review on a case by case basis. As such, this attribute is used to indicate the kinds of requests that align with existing consent/HREC approval.

ANZCTR Step 11 must be provided.

Optionally, more structured metadata can be provided to DataCite to enable machine-readability of permitted uses, which the HeSANDA portal can use to provide a better user experience.

If providing metadata to DataCite, DUO - the Data Use Ontology - is recommended here, if appropriate for the dataset. [Read an introduction](https://doi.org/10.1016/j.xgen.2021.100028) here.  \
Note: DUO terms can currently only be applied using the DataCite metadata schema.

   </td>
   <td>ANZCTR Step 11 -  ’Available for what types of analyses?’

   </td>
   <td>1

   </td>
   <td>Text

   </td>
   <td>Any purpose, only to achieve the

aims in the approved proposal, for IPD meta-analyses, etc.

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 16 Rights

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>population origins/ancestry research

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 16.a rightsURI

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>http://purl.obolibrary.org/obo/DUO_0000011

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 16.b rightsIdentifier

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>DUO_0000011

   </td>
   <td>
   </td>
   <td>Not available in Fabrica interface

   </td>
  </tr>
  <tr>
   <td>DataCite 16.c rightsIdentifierScheme

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>DUO

   </td>
   <td>
   </td>
   <td>Not available in Fabrica interface

   </td>
  </tr>
  <tr>
   <td>DataCite 16.d schemeURI 

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>http://purl.obolibrary.org/obo/duo.owl

   </td>
   <td>
   </td>
   <td>Not available in Fabrica interface

   </td>
  </tr>
  <tr>
   <td>4.2

   </td>
   <td>Data sharing policy

   </td>
   <td>Required

   </td>
   <td>Y

   </td>
   <td>A policy statement and/or set of procedures that addresses secondary use of the dataset. This would commonly be presented as a publicly accessible document or webpage that details items such as the following:



* Governance roles and responsibilities
* Regulatory requirements (e.g. legal, ethical, funding)
* Requirements for requesting data access (e.g. procedures, time frames, costs)
* Requirements for management and handling of shared data (e.g. storage and disposal, reporting)

Data sharing policies are broad in nature and represent the general position of the data custodian regarding sharing of the dataset. It is common for a specific data sharing agreement to be signed by the requestor and custodian prior to the release of data in response to a data request. Data sharing agreements are contracts between two or more parties that articulate the specific terms and conditions for the sharing of data for a specific purpose. The data sharing policy may be cited in the terms of the data sharing agreement if required.

See also **Permitted uses [4.1]** and **Rights/Licence [4.3]**.

   </td>
   <td>ANZCTR Step 11: Data sharing statement

   </td>
   <td>1

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>See 2.8 Other research outputs and related publications for a more detailed breakdown of DataCite 20 relatedItem. Use relatedItemType “Text” for a data sharing policy.

   </td>
  </tr>
  <tr>
   <td rowspan="2" >4.3

   </td>
   <td rowspan="2" >Rights/ Licence

   </td>
   <td rowspan="2" >Optional

   </td>
   <td rowspan="2" >Y

   </td>
   <td rowspan="2" >Any intellectual property rights and/or licensing information regarding sharing and/or secondary use of the data object. This may be expressed as:



* A textual statement of the rights management associated with the asset
* A legal document under which the asset is made available (e.g. a data sharing agreement template)

See also **Permitted uses [4.1] **and **Data sharing policy [4.2]**.

   </td>
   <td>DataCite 16 Rights

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>RESTRICTIVE LICENCE AGREEMENT for USE OF MATERIAL [insert description] between THE SUPPLIER [insert Supplier’s name] and THE CUSTOMER [insert Customer’s name]

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 16.a rightsURI

   </td>
   <td>0-1

   </td>
   <td>Text

   </td>
   <td>https://licenceagreementtemplate.uni.edu.au/

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>4.4.1

   </td>
   <td>Enquiries 

   </td>
   <td>Required

   </td>
   <td>Y

   </td>
   <td>The relevant point of contact for requesting additional information about the data asset. The point of contact should be enduring (e.g. role-based) as opposed to a specific individual (e.g. a chief investigator).

This may be different to the point of contact for requesting access to the data asset (see **Request POC** **[4.4.2]** below).

Email (or URL to web form) for the point of contact.

   </td>
   <td>ANZCTR Step 10 - Contact person for scientific queries

   </td>
   <td>1

   </td>
   <td>Text

   </td>
   <td>Medical Director for the Study, +61 2 9562 5333, Department of Clinical Trials, Holt University, enquiries@holt.edu.au

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td rowspan="11" >4.4.2

   </td>
   <td rowspan="11" >Request point of contact

   </td>
   <td rowspan="11" >Required

   </td>
   <td rowspan="11" >Y

   </td>
   <td rowspan="11" >The relevant point of contact for requesting access to the data asset (e.g. the data custodian). The point of contact should be enduring (e.g. role-based) as opposed to a specific individual (e.g. a chief investigator).

This may be a different point of contact than that used for enquiries about the data asset (see **Enquiries [4.4.1]** above).

This field will be used by the HeSANDA Federations Service to direct where data requests will be sent. 

The Request Point of Contact will need to be separately registered with ARDC to enable this functionality.

   </td>
   <td>DataCite 7 Contributor 

   </td>
   <td>
   </td>
   <td>n/a

   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.a contributorType

   </td>
   <td>1

   </td>
   <td>n/a

   </td>
   <td>Must be “Distributor”

   </td>
   <td>


* ContactPerson
* DataCollector
* DataCurator
* DataManager
* Distributor
* Editor
* HostingInstitution
* Producer
* ProjectLeader
* ProjectManager
* ProjectMember
* RegistrationAgency
* RegistrationAuthority
* RelatedPerson
* Researcher
* ResearchGroup
* RightsHolder
* Sponsor
* Supervisor
* WorkPackageLeader
* Other
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 7.1 contributorName

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>Australasian Leukaemia 

and Lymphoma Group (ALLG)

   </td>
   <td>List of all HeSANDA data providers

   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.1.a nameType 

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>Must be “Organizational”

   </td>
   <td>From the DataCite metadata schema



* Organizational
* Personal
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 7.4 nameIdentifier

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>https://ror.org/05t72y326

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.4.a nameIdentifierScheme

   </td>
   <td>1

   </td>
   <td>Text from list

   </td>
   <td>ROR

   </td>
   <td>From the DataCite metadata schema



* ISNI
* ROR
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 7.4.b schemeURI

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>https://ror.org/

   </td>
   <td>From the DataCite metadata schema



* https://isni.org
* https://ror.org/
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 7.5 affiliation

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>Holt University

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5.a affiliationIdentifier 

   </td>
   <td>0-n

   </td>
   <td>Text

   </td>
   <td>https://ror.org/02czsnj07

   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>DataCite 7.5.b affiliationIdentifierScheme

   </td>
   <td>1

   </td>
   <td>Test from list

   </td>
   <td>ROR

   </td>
   <td>From the DataCite metadata schema



* ISNI
* ROR
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
DataCite 7.5.c SchemeURI 

   </td>
   <td>0-1

   </td>
   <td>Text from list

   </td>
   <td>https://ror.org/

   </td>
   <td>From the DataCite metadata schema



* https://isni.org
* https://ror.org/
   </td>
   <td>
   </td>
  </tr>
</table>



<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
