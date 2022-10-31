# 2022 AMIA Annual Conference 
### Tuesday, Nov 08, 2022 3:30 PM - 5:00 PM EST
### Session: S87: Oral Presentations - Sharing is Caring: Interoperability and Secondary Use of Data

## Developing support for interoperation of research in healthcare equity

### James R. Campbell MD<sup>1</sup>, James Svoboda MS<sup>1</sup>, A. Jerrod Anzalone MS<sup>1</sup> , Mary E. Campbell PhD<sup>2</sup>,  Johnelle Sparks PhD<sup>3</sup>, Carol R. Geary PhD, MBA, RN<sup>1</sup>

1) University of Nebraska Medical Center, Omaha, NE; 
2) Texas A&M University, College Station, TX;
3) The University of Texas at San Antonio, San Antonio, TX

## Attendee Handout
Please find the attendee handouts for this session [here](https://github.com/UNMC-CRANE/AMIA_November_2022/tree/main/Handouts). 

## Introduction

Social Determinants of Health (SDoH) are widely accepted as important to healthcare outcomes but have no agreed information model or code standards for recording in clinical electronic health records (EHR). Therefore, SDoH are found minimally in research data warehouses extracted from EHRs. However, data elements recording SDoH facts in US Electronic Health Records(EHRs) must comply with the USCDI<sup>1</sup> data standards to interoperate in the US.

Researchers have reviewed data quality issues in studies of data from EHRs<sup>2-3</sup> citing problems with completeness, conformance and plausibility. A recent systematic review of SDoH data quality<sup>4</sup> concluded that such issues are common across domains of SDoH, especially plausibility and completeness for race and ethnicity and conformance and plausibility for community-level data. The authors concluded: “Consistently applied standards for SDoH data collection in the EHR would result in improved data quality, which in turn would lead to more robust research, care coordination, and population health management.” Although one paper has proposed a roadmap for a project of data standardization <sup>5</sup> , no inventory or data dictionary has been published to our knowledge.

## Methods

Our team identified the Healthy People 2030 framework<sup>6</sup> in order to specify the scope and domains of SDoH data. We reviewed draft version 3 of the ONC USCDI publication<sup>1</sup> on healthcare data interoperability for applicable terminology standards and dialogued with terminology lead of the HL7 Gravity project<sup>7</sup> , the Health Disparities and Data Standards workgroups of the OHDSI<sup>8</sup> research network and colleagues at University of Southern California.

Our team had experience with using the American Community Survey(ACS) for extracting community-level SDoH facts<sup>9</sup>. We expanded our inventory of computed ACS data items reported in that work, extracting a fraction of the substantial breadth of data within the ACS. We surveyed public data sets of relevance and developed software to mine the community-level data elements accessible in those additional public domain resources listed in Table 1.
### Table 1. Public data resources offering community-level data by SDoH domain
| **Resource**                                                   | **SDOH Domains**                                                                                                                                                             |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| American Community Survey, Department of Census                | Economic Stability, Social and Community Context, Education Access and Quality, Neighborhood and Built Environment                                                           |
| Food Environment Atlas, USDA                                   | Economic Stability, Nutrition Security                                                                                                                                       |
|     Social Vulnerability Index, CDC                            | Economic Stability, Social and Community Context, Neighborhood and Built Environment                                                                                         |
| Rural Urban Commuting Area, Department of Agriculture          | Social and Community Context                                                                                                                                                 |
| Center for Air Climate and Energy Solutions, EPA               | Neighborhood and Built Environment                                                                                                                                           


For all facts that we identified, we researched the relevant USCDI terminologies for applicable code references and definition. For facts without a precoordinated – that is, published - code and definition, we developed a fully specified name, extension concept identifier and metadata computable definition following the SNOMED CT concept model <sup>11</sup> for Observable entities, a model developed in collaboration with LOINC<sup>12</sup>.

We are currently publishing as open source all reference data tables, an extended ontology of SNOMED CT-LOINC-RXNORM with mappings to USCDI codes, and terminology services for geocoded community-level SDoH data. These may be browsed on our Nebraska Terminology Development website<sup>11</sup>.

## Results
Although our inventory of public resources for community-level SDoH facts is not yet complete, we have been able to identify and define 65 community-level items taken from the public resources of Table 1 and 76 patient-level items suitable for EHR implementation. Our EPIC® EHR had data available for 40/76 patient-level facts of which 6 were computable phenotypes for the Healthcare Access domain and 2 were computable phenotypes for Social and Community Context. The remaining 34 patient-level data elements were patient reported outcomes recorded during healthcare events.

As summarized in Table 2, 56/141 concepts that we identified had pre-coordinated (published) standards codes specified within the USCDI framework, all LOINC or SNOMED CT observable entities. In order to develop an interoperable computable definition and metadata ontology for all SDoH concepts, we extended the SNOMED CT-LOINC conceptual model to fully define all concepts in a unified ontology for USCDI datasets. The complete unified ontology is being documented and made available as SNOMED CT RF2 and OWL datasets on our Terminology Development website^10. Also included will be an open source software supporting retrieval of community-level SDoH data retrievable by geocode for sites that wish to expand their own SDoH datasets.

###  Table 2. SDoH concept counts by domain with pre-coordinated concept code counts
| **SDoH Domain**  | **Patient-level Facts**  | **Community-level Facts**  | **2022 USCDI Coded Facts**  |
|---|---|---|---|
| Economic Stability  | 14  |  8 |  LOINC:8 |
| Healthcare Access  | 8  | 1  |  LOINC:5 |
|  Social & Community Context | 44  | 42  | LOINC:33 SNOMEDCT:2  |
|  Education Access & Quality |  2 | 5  | LOINC:2  |
|  Neighbor & Built Environment | 8  |  9 | LOINC:5 SNOMEDCT:1  |
| Total Items  | 76  | 65  | 141  |

## Discussion

We found that 2022 USCDI published standards were applicable to only a minority of SDoH data present in our EHR. There is a large spectrum of community-level SDoH that is available in public sources and relevant to research in SDoH but are laborious to identify, document and standardize. In this paper we present the documentation, tooling and ontologies that we propose to support the researcher in Healthcare Equities for developing their research datamart.

### References

1) US Core Data for Interoperability Version 3 Draft https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi
2) Berkman LF, Lochner KA. Social determinants of health: Meeting at the crossroads. Health Affairs. 2002 Mar;21(2):291-3.
3) Weiskopf NG, Weng C. Methods and dimensions of electronic health record data quality assessment: enabling reuse for clinical research. J Am Med Inform Assoc 2013; 20 (1): 144–51.
4) Cook LA, Sachs J, Weiskopf NG. The quality of social determinants data in the electronic health record: a systematic review. J Am Med Inform Assoc. 2021 Dec 28;29(1):187-196.
5) Watkins M, Viernes B et all. Translating social determinants of health into standardized clinical entities. Stud Health Technol Informatics. 2020 June 16; 270:474-478.
6) HL7 Gravity project. https://HL7.org/gravity/
7) Healthy People 2030, U.S. Department of Health and Human Services, Office of Disease Prevention and Health Promotion. https://health.gov/healthypeople/objectives-and-data/social-determinants-health. retrieved 10/1/2021
8) OHDSI research network: https://www.ohdsi.org/
9) Gardner BJ, Pedersen JG, Campbell ME, McClay JC. Incorporating a location-based socioeconomic index into a de-identified i2b2 clinical data warehouse. J Am Med Inform Assoc. 2019 Apr 1;26(4):286-293.
10) UNMC Terminology Development Center: https://www.unmc.edu/pathology-research/bioinformatics/campbell/tdc.html
11) SNOMED CT Editorial Guide. https://confluence.ihtsdotools.org/display/DOCEG
12) Regenstrief and SNOMED International joint work agreement. https://loinc.org/collaboration/snomed-international/


**For more information, please visit our previous AMIA Workshop from the 2022 AMIA Clinical Informatics Conference [here](https://github.com/UNMC-CRANE/AMIA_Workshop_May_2022). This workshop - "Introduction to semantic interoperability; Top-level ontologies for the US domain" - covered terminology management from across the medical spectrum, including SDoH data elements. Specific content relevant to attendees can be found [here](https://unmc-crane.github.io/AMIA_Workshop_May_2022/interoperable-use-cases-for-vitals-clinical-assessments-nursing-assessments-and-social-determinants-of-health.html#social-determinants-of-health-sdoh).**
