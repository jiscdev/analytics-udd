# Jisc Learning Analytics Unified Data Definitions v1.5.1

_Version 1.5.1 released on 29 October 2019._

## Introduction
The Unified Data Definitions (UDD) of the Jisc learning analytics project is a vocabulary of the chief data entities of interest to learning analytics: students, courses, modules, and so on, as well as their characteristics. The data coded with this vocabulary is typically extracted from the student record system of a college or university.

Along with xAPI recipes, the UDD makes up the core data specification of the Jisc learning analytics architecture.

The main folder (jiscdev/analytics-udd) contains:

- this ReadMe file that gives an overview of the UDD
- the details of the UDD licencing arrangements
- a UDD entity-relationship diagram
- a link to spreadsheets listing the differences between the previous version of the UDD and this version
- a consolidated list of the descriptions of each UDD entity. 

In addition to the main folder, there are 4 sub-folders. The udd sub-folder is the heart of the specification, with a file for each entity describing its properties in detail. Refer to these files to design data for import into the Learning Data Hub. The media sub-folder contains supporting files, including the E-R diagram source, the changes spreadsheet, Guides to the relative importance of UDD properties in respect of applications, products and services that use the UDD, and copies of the JACS3 and HECoS subject classification systems. The utilities sub-folder has code fragments and snippets to support the development and use of the UDD. The implementation sub-folder describes matters that are not part of the formal UDD specification, but are closely related to it, for example a description of the mechanism for handling unofficial extensions to properties in the UDD, and filename conventions for adding data into the Learning Data Hub.

For release schedule and version control, see [below](README.md#release-schedule-and-version-control).

## Differences between v1.4 and v1.5
The development of v1.5 has involved a number of additions and changes. [This overview page](differences.md) lists the changes in summary and provides a spreadsheet with the mapped listing of each entity and property change between v1.4.1 and v1.5.1.

## Data format
UDD data must be UTF-8 encoded. TSV is the preferred data format, but JSON and XML data are also supported. Other formats are not supported.

When providing UDD data, supply the data for different entities in separate files, 1 file per entity, using the [UDD filename conventions](implementation/filename_conventions.md).

## Diagram
2 entity-relationship diagrams provide an overview of the specification. There is a [brief E-R diagram](diagram.md) containing just the primary keys, constraints and foreign key properties, and a [full E_R diagram](diagramFull.md) with all the properties.

## Entities

### Primary keys
Some entities have uniqueness constraints across multiple properties; for example student_on_course_instance has STUDENT_COURSE_MEMBERSHIP_ID plus COURSE_INSTANCE_ID. The MD files for these entities contain a note to this effect. These entities have a single primary key for ease of processing and to enable field-level extensibility. The data supplier may choose to provide the single primary key, or may choose to leave it blank, in which case it will be generated by the Learning Data Hub loading mechanism.

### [assessment_instance](udd/assessment_instance.md)

### [course](udd/course.md)

### [course_instance](udd/course_instance.md)

### [course_subject](udd/course_subject.md)

### [event](udd/event.md)

### [institution](udd/institution.md)

### [module](udd/module.md)

### [module_instance](udd/module_instance.md)

### [module_map](udd/module_map.md)

### [module_subject](udd/module_subject.md)

### [module_vle_map](udd/module_vle_map.md) Deprecated

### [student](udd/student.md)

### [student_course_membership](udd/student_course_membership.md)

### [student_event](udd/student_event.md)

### [student_on_assessment_instance](udd/student_on_assessment_instance.md)

### [student_on_a_module_instance](udd/student_on_a_module_instance.md)

### [student_on_course_instance](udd/student_on_course_instance.md)

## Additional sections
### [period](udd/period.md)

### [staff](udd/staff.md)

### [staff_on_course_instance](udd/staff_on_course_instance.md) Deprecated

### [staff_on_mod_instance](udd/staff_on_mod_instance.md) Deprecated

### [staff_link](udd/staff_link.md)

### [student_id_map](udd/student_id_map.md)

### Table of entities and corresponding API endpoint names
See the [filename_conventions](implementation/filename_conventions.md) file for information about providing UDD data.

<table>
  <tr><td>ENTITY NAME</td><td>API ENDPOINT NAME</td></tr>
  <tr><td><a href="./udd/assessment_instance.md">assessment_instance</a></td><td>assessmentinstance</td></tr>
  <tr><td><a href="./udd/course.md">course</a></td><td>course</td></tr>
  <tr><td><a href="./udd/course_instance.md">course_instance</a></td><td>courseinstance</td></tr>
  <tr><td><a href="./udd/course_subject.md">course_subject</a></td><td>coursesubject</td></tr>
  <tr><td><a href="./udd/event.md">event</a></td><td>event</td></tr>
  <tr><td><a href="./udd/institution.md">institution</a></td><td>institution</td></tr>
  <tr><td><a href="./udd/module.md">module</a></td><td>module</td></tr>
  <tr><td><a href="./udd/module_instance.md">module_instance</a></td><td>moduleinstance</td></tr>
  <tr><td><a href="./udd/module_map.md">module_map</a></td><td>modulemap</td></tr>
  <tr><td><a href="./udd/module_subject.md">module_subject</a></td><td>modulesubject</td></tr>
  <tr><td><a href="./udd/module_vle_map.md">module_vle_map</a></td><td>modulevlemap</td></tr>
  <tr><td><a href="./udd/period.md">period</a></td><td>period</td></tr>
  <tr><td><a href="./udd/staff.md">staff</a></td><td>staff</td></tr> 
  <tr><td><a href="./udd/staff_link.md">staff_link</a></td><td>stafflink</td></tr> 
  <tr><td><a href="./udd/staff_on_course_instance.md">staff_on_course_instance</a></td><td>staffcourseinstance</td></tr>
  <tr><td><a href="./udd/staff_on_mod_instance.md">staff_on_mod_instance</a></td><td>staffmoduleinstance</td></tr>
  <tr><td><a href="./udd/student.md">student</a></td><td>student</td></tr>
  <tr><td><a href="./udd/student_course_membership.md">student_course_membership</a></td><td>studentcoursemembership</td></tr>
  <tr><td><a href="./udd/student_event.md">student_event</a></td><td>studentevent</td></tr>
  <tr><td><a href="./udd/student_id_map.md">student_id_map</a></td><td>studentidmap</td></tr>
  <tr><td><a href="./udd/student_on_assessment_instance.md">student_on_assessment_instance</a></td><td>studentassessmentinstance</td></tr>
  <tr><td><a href="./udd/student_on_a_module_instance.md">student_on_a_module_instance</a></td><td>studentmoduleinstance</td></tr>
  <tr><td><a href="./udd/student_on_course_instance.md">student_on_course_instance</a></td><td>studentcourseinstance</td></tr>
</table>

There are also files of code lists extracted from the MD files for machine processing.
### [UDD code lists in Welsh](udd/udd_codelists_cy.json)
### [UDD code lists in English](udd/udd_codelists_en.json)

## Mandatory and optional properties
The properties of the UDD are required in compliant datasets to different degrees, dependent on the products and services that use the outputs. There is a Field Guide spreadsheet that, for each product or service, indicates how important each property is for operation or use of the product. A [Field Guide](media/UDD_FieldGuide.xls) is included in this version of the UDD, so that vendors and service providers can supply their own entries for institutions to refer to as an aid to data preparation. The Field Guide enables the vendor or service provider to indicate data items that are MANDATORY, IMPORTANT, PREFERRED or NOT USED.

## Code lists
Some UDD properties consist of code lists. Some have values derived from HESA tables (for HE) or ILR tables (for FE). In general these code lists are mapped to generic UDD code lists, so that they are standardised across data from multiple institutions. To extract code lists from the UDD MD files, you may wish to use the Python utility provided [here](utilities/Extract%20Code%20Lists%20from%20MD.py).

Some code lists will be specific to one or a limited group of institutions. These lists are not included in the UDD and can be generated by the vendor. They can be loaded to the Learning Data Hub via a standard JSON format or can be handled via extensions (see below). An example of the JSON format is:

```
"MOD_LEVEL": {"A": null, "C": null, "B": null, "E": null, "D": null, "1": null, "0": null, "3": null, "2": null, "5": null, "7": null, "6": null, "9": null}}
```

## Extensions
There is provision for data extensions at the level of property (in other words, "field-level extensions"). Although not strictly part of the UDD, a separate entity is provided and described at [extension.md](implementation/extension.md).

## Specification development workflow
The simplest way of contributing to the UDD is as follows:

1. add an issue to the issue tracker to alert everyone to what you are working on and why.
2. tag the issue with the version milestone of which you'd like the patch to be a part.
3. make an edit or add a file in this repository, and save it to your own branch. If you prefer, you can fork the whole repository and work in your own repository.
4. send a pull request once you're done.
5. the pull request will be discussed at our regular meetings and either merged, or kept in the queue, depending on whether more work is required.

You can do all this through the Github GUI, but you're welcome to use any other git tool you prefer.

## Release schedule and version control

Particular release versions will get their own branches, but the master branch will always contain the latest agreed release. Releases will be made after the review group has come to an agreement.

Versioning is done broadly as follows: (majorVersion.minorVersion.patch) major versions indicate major data model changes. Minor versions denote changes that can break applications, such as the deletion of properties that were valid in earlier versions. Patches can include the addition of new properties.

There will usually be a new minor version with breaking changes available for use in June of each year, in time for the next academic year. For example, from version 1.5 to version 1.6 in the summer of 2020 for the 2020-21 academic year.

All version changes will be announced in advance on the repository issue tracker and in this README file.

Note that some properties will be marked as 'deprecated'. This means that the property is still valid, but will be removed by the next minor version update.

## Acknowledgements

Many thanks to all contributors who have raised issues, sent pull requests, commented and made suggestions. The UDD specification is the achievement of all of you.

- @alanepaull
- @andrewhickey
- @arc12
- @christoffballard
- @craig-petch
- @ds10
- @gmoger-jisc
- @gryglbrt
- @ht2 
- @huwrobertsjisc
- @Josh-Ring-jisc
- @jfmullaney
- @michaelwebjisc
- @MiroslavKratchounov
- @robwynj
- @ryansmith94
- @sandeepmjay
- @willblenkhorn
- @wilmTap


### License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
