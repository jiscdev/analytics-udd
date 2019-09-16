# Differences between UDD 1.4.1 and 1.5.0

The following spreadsheets give an overview of all the changes that were introduced with version 1.4 of the UDD. A blank cell indicates that a property is no longer used, green indicates a new property, and orange a changed property. 

[xls spreadsheet of 1.3.3 to 1.4.0 changes][differencesXLS]

[differencesXLS]: media/UDD1.3-1.4.xls "differencesXLS"

[xls spreadsheet of 1.4.0 to 1.4.1 changes][differences2XLS]

[differences2XLS]: media/UDD1.4.0-1.4.1.xls "differences2XLS"

[xls spreadsheet of 1.4.0 to 1.4.1 changes][differences2XLS]

[differences2XLS]: media/UDD1.4.1-1.5.0.xls "differences2XLS"

## Summary of differences


In summary, v1.4.0 release of UDD implemented the following, compared to v1.3.3:

- HECoS vocabulary added to /media.
- Draft course_subject and draft module_subject entities added. Note: course.SUBJECT and module.SUBJECT not deleted, but deprecated instead.
- Documentation updated to show that uniqueness constraint on VLE_MOD_ID in module_vle_map is controlled by institution.MODULE_VLE_MAP_MODE; default is that MOD_INSTANCE_ID and VLE_MOD_ID form a uniqueness constraint.
- TENANT_ID in course made mandatory.
- ENTRY_POINTS split into ENTRY_POINTS (normally Ucas tariff) and AVERAGE_GCSE_SCORE in student_course_membership. ENTRY_POINTS labelled "Omitting this property may hinder the development or use of an effective analytics model." To encourage supply.
- ACADEMIC_YEAR and MOD_ACADEMIC_YEAR made mandatory throughout.
- Format for YEAR_PRG and YEAR_STU in student_on_course_instance changed to INT.
- ACTIVE_MEMBERSHIP in student_course_membership made mandatory.
- New property ENTRY_POINTS_SCHEMA added to student_course_membership, specifying the UCAS Tariff points scheme used in ENTRY_POINTS.
- ENTRY_POINTS_SCHEMA mandatory if ENTRY_POINTS used; indicates particular scheme used for ENTRY_POINTS (normally Ucas tariff).
- Deprecated MAX_POINTS deleted from student_on_assessment_instance.
- Deprecated MOD_OPTIONAL deleted from module_instance
- Deprecated LEARN_DIF, DISABILITY1, DISABILITY2 and TERMTIME_ACCOM deleted from student
- Deprecated X_YEAR_AVERAGE_MARK deleted from student_on_course_instance
- Values for ADMISSIONS_ROUTE extended to include widening participation initiatives, UCAS Adjustment, UCAS Record of Prior Acceptance.
- Spreadsheet for entity and property changes v1.3.3 to v1.4 created
- COURSE_OUTCOME values 13 and 14 deleted; these were added to match values on FE ISR that are confusing in relation to the definition of COURSE_OUTCOME.

## Summary of differences between v1.4.0 and v1.4.1

- PROVIDED_AT: Added 'Z' clarification to date/time format: in ISO 8601 format - YYYY-MM-DDThh:mmZ or YYYY-MM-DDThh:mm is acceptable
- course: Added code I78 to COURSE_AIM
- student_course_membership: updated WITHDRAWAL_REASON codes and clarified ACTIVE_MEMBERSHIP Notes
- updated HESA links in many of the MD files to 2018-19 links
- New event and student_event entities added
- New UDD Field Guide introduced and old template removed
- New E-R diagrams and updated change spreadsheet created

## Summary of differences between v1.4.1 and v1.5.0

- staff_link: new entity created; TUTOR_STAFF_ID on student deprecated, staff_on_course_instance deprecated; staff_on_mod_instance deprecated
- filename_conventions.md: student_event corrected to studentevent
- ISO 8601 formats updated to YYYY-MM-DDThh:mm[:ss.mmm]Z
- student_on_course_instance.md: new property FTE added
- course_instance.md: new property COMMENCEMENT_PERIOD added; PERIOD_CODE on period updated to refer to COMMENCEMENT_PERIOD
- Field Guide: ‘Preferred’ removed from student.ETHNICITY, SEXID, DIFFLEARN1 and DIFFLEARN2 for Predictive Analytics
- module_map: new entity created; module_vle_map deprecated
- entity_descriptions.md: updated for new entities
- event: extensively revised; Description clarified; EVENT_ID description clarified; EVENT_NAME changed to optional; new properties 
- EVENT_DATA_SOURCE EVENT_TYPE_RAW added; ISO 8601 formats revised for EVENT_START and EVENT_END; EVENT_LOCATION Description and Purpose modified
