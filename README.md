# Hello
<a href="https://www.bradfordresearch.nhs.uk/our-research-teams/connected-bradford/">
  <img align="left" alt="ConnectedBradford" width="55px" src="https://github.com/ShoreRob1/Images/blob/main/CB%20logo%201.png?raw=true" />
</a>


![](https://visitor-badge.glitch.me/badge?page_id=ConnectedBradford.FDMDepartmentForEducation)

This is the **Connected Bradford Department for Education (DfE)** GitHub page where you can find a summary of the dataset(s), data dictionaries and helpful code.


This dataset and page is maintained by [Robert Shore](https://actearly.org.uk/team_member/rob-shore/): 


:e-mail: [email](mailto:robert.shore@bthft.nhs.uk)

:speech_balloon: ask me about anything, I'm happy to help;


# DfE

📌 *The DfE FDM is made up of 26 source tables (data dictionaries linked) as well as additional standardised (read more on 'FDMs' below) tables created by the Connected Bradford team. This FDM holds routinely collected DfE data and educational records for 299,888 individuals, made up from primary and secondary care data for those who attended school after 1997.* *It is collected on either an annual or termly basis, depending on the table.*. 

*The source tables are largely populated by fields with the prefix 'src_'. When you see the 'src_' prefix, this means that field has not been reformatted by the Connected Bradford team and it is included in its raw form.*

📁 **What is an FDM?**

*Connected Bradford has adopted the OMOP Common Data Model (CDM) for the majority of its patient-centred healthcare data. Some datasets in Connected Bradford have features that do not sit well within either the OMOP conceptual vocabulary or the structure of the CDM. The aim of the Flexible Data Model (FDM) is to provide a set of design principles and a data model for non-OMOP datasets such that they can be structured and annotated in an OMOP-friendly way, and are therefore easy to combine with OMOP CDM data during analysis.*

*The Connected Bradford Flexible Data Model enables researchers to link standardised datasets and tables across different areas, e.g. primary care, social care and education. In order to be linked to a CDM or clinical dataset, FDMs are designed in the same way as a full CDM, to standardize the structure and content of observational data and to enable efficient analyses that can produce reliable evidence. This also helps any researcher familiar with CDM and OMOP vocabulary to replicate analysis on the Connected Bradford platform.*

[OMOP guidelines here](https://ohdsi.github.io/CommonDataModel/cdm60.html)


### Standard FDM tables included in this dataset


🧍 **person**

299,888 individuals 

*This table serves as the central identity management for all Persons in the database. It contains records that uniquely identify each person or patient, and some demographic information. All records in this table are independent Persons. All Persons in this database have one record in this table, unless they fail data quality requirements specified, e.g. an event from the source tables pre-dates their date of birth or exceeds any date of death by more than 42 days (42 days is the time period allowed due to processing of deaths).*

*The BIRTH_DATETIME field is standardised across all Connected Bradford FDMs and is equivalent to the content of BIRTH_DAY, BIRTH_MONTH and BIRTH_YEAR (DD-MM-YYYYT00:00:00). The person’s death date is also stored in this table in the same standardises format. The validated minimum and maximum of additional ‘event’ dates are stored in the observation_period table, while all validated 'events' are stored in the visit_occurence table.*

*The person table also includes demographics such as ethnicity and gender.*

*Use fields from the person table for all analysis related to birth, death and any demographics*




🔎 **observation_period**

299,888 individuals 


*The observation_period table contains records which define spans of time during which two conditions are expected to hold: (i) Clinical Events that happened to the Person are recorded in event fields in the source tables and visit_occurence and (ii) absence of records indicate such Events did not occur during this span of time.*

*The validated minimum and maximum of additional ‘event’ dates are stored in the observation_period table, while all validated 'events' are stored in the visit_occurence table. observation_period records can be as short as a single day.*


🏥 **visit_occurence**

5,955,732 records


*The visit_occurence table contains Events where Persons engage with adult social care for a duration of time. They are often also referred to by OMOP as 'Encounters'. Visits are defined by a configuration of circumstances under which they occur, such as whether the patient comes into contact  with social care, the other way around, or the interaction is remote. All validated 'events' are stored in the visit_occurence table.*

### Source tables in this dataset

*There are three source tables in this dataset. Source tables are those that have had little to no manipulation other than to validate any event dates. All source field are prefixed with 'src_'. The three source tables in the adult social care data set are:*

### src_EYFSP - 2002/03-

*Early Years Foundation Stage Profile data. This has information on the statutory assessment of children in the final year of the Foundation Stage (Reception year).*

### src_KS1 - 1997/98-

*Key stage 1 attainment data. This has information on the assessment of learners by the end of year 2 of schooling.*

### src_KS2_exam 2006/07-

*Key stage 2 attainment data. This has information on the assessment of learners by the end of year 6 of schooling.*

### src_KS2_pupil 1995/96-

*Key stage 2 attainment data. This has information on the assessment of learners by the end of year 6 of schooling.*

### src_KS3_exam - 2006/07-2007/08

*Key stage 3 attainment data.*

### src_KS3_pupil - 2001/2002-2007/08

*Key stage 3 attainment data.*

### src_KS3_TA - 2008/09/2012/13

### src_KS4_exam - 2001/02 - 

*Key stage 4 attainment data (all methodologies). This has information on the assessment of learners by the end of year 11 of schooling.*

### src_KS4_pupil - 2001/02 -

*Key stage 4 attainment data (all methodologies). This has information on the assessment of learners by the end of year 11 of schooling.*

### src_KS5_exam - 2004/05 

*Key stage 5 attainment data. This has information on the post-16 assessment of learners in school sixth forms and FE colleges.*

### src_KS5_student 2002/03

*Key stage 5 attainment data. This has information on the post-16 assessment of learners in school sixth forms and FE colleges.*

### src_absence 2001/02 - 2001/02

*This has information on pupil absences derived from the termly School Census.*

### src_census 2001/02

*School Census data. This has information on pupils attending maintained schools. From Spring 2013/14, this includes local authority (LA) maintained PRUs and alternative provision (AP) academies, including AP Free Schools.*

*Pupil Referral Unit census data. This has information on children attending local authority (LA) maintained PRUs and alternative provision (AP) academies, including AP Free Schools. From Spring 2013/14, this data is collected as part of the School Census.*

*Early years census data. This has information on children attending any private, voluntary and independent (PVI) sector nursery with one or more children receiving funding from the Department.*

*Alternative Provision census data. This has information on children in Alternative Provision i.e. a school not maintained by an LA but which the authority is paying full tuition fees for.*

### src_exclusions - 2001/02

*This has information on pupil exclusions as collected in the termly School Census.*

### src_post16 - 2007/08

*This has information on post-16 learning aims as collected in the School Census.*


## Useful links

📖 [Data dictionary](https://github.com/ConnectedBradford/CY_FDM_DepartmentForEducation/blob/main/Copy%20of%20DfE%20Data%20Dictionary.xlsx)  











