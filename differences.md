# Differences between UDD 1.3.3 and 1.4.0

The following spreadsheet gives an overview of all the changes that were introduced with version 1.4 of the UDD. A blank cell indicates that a property is no longer used, green indicates a new property, and orange a changed property. 

[xls spreadsheet of 1.3.3 to 1.4.0 changes][differencesXLS]

[differencesXLS]: media/UDD1.3-1.4.xls "differencesXLS"

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
- Deprecated MOD_LOCATION deleted from module_instance
- Deprecated LEARN_DIF, DISABILITY1, DISABILITY2 and TERMTIME_ACCOM deleted from student
- Deprecated X_YEAR_AVERAGE_MARK deleted from student_on_course_instance
- Values for ADMISSIONS_ROUTE extended to include widening participation initiatives, UCAS Adjustment, UCAS Record of Prior Acceptance.
- Spreadsheet for entity and property changes v1.3.3 to v1.4 created
- COURSE_OUTCOME values 13 and 14 deleted; these were added to match values on FE ISR that are confusing in relation to the definition of COURSE_OUTCOME.
