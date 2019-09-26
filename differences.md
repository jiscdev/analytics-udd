# Differences between UDD 1.4.1 and 1.5.0

The following spreadsheet gives an overview of all the changes that were introduced with version 1.5.0 of the UDD. A blank cell indicates that a property is no longer used, green indicates a new property, and orange a changed property. 

[xls spreadsheet of 1.4.1 to 1.5.0 changes][differencesXLS]

[differencesXLS]: media/UDD1.4.1-1.5.0.xls "differencesXLS"

## Summary of differences

In summary, v1.5.0 release of UDD implemented the following, compared to v1.4.1:

- staff_link: new entity created; TUTOR_STAFF_ID on student deprecated, staff_on_course_instance deprecated; staff_on_mod_instance deprecated
- filename_conventions.md: student_event corrected to studentevent
- ISO 8601 formats updated to YYYY-MM-DDThh:mm[:ss.mmm]Z
- student_on_course_instance.md: new property FTE added
- course_instance.md: new property COMMENCEMENT_PERIOD added; PERIOD_CODE on period updated to refer to COMMENCEMENT_PERIOD
- Field Guide: ‘Preferred’ removed from student.ETHNICITY, SEXID, DIFFLEARN1 and DIFFLEARN2 for Predictive Analytics
- student: Preference text removed from Notes in student.ETHNICITY, SEXID, DIFFLEARN1 and DIFFLEARN2 in line with Field Guide.
- module_map: new entity created; module_vle_map and MODULE_VLE_MAP_MODE deprecated
- entity_descriptions.md: updated for new entities
- event: extensively revised; Description clarified; EVENT_ID description clarified; EVENT_NAME changed to optional; new properties EVENT_DATA_SOURCE EVENT_TYPE_RAW added; ISO 8601 formats revised for EVENT_START and EVENT_END; EVENT_LOCATION Description and Purpose modified
- course.SUBJECT and module.SUBJECT: deleted (were deprecated in v1.4).
- assessment_instance: new property ASSESS_SUMMATIVE added; old ASSESS_TYPE_ID and ASSESS_TYPE_NAME deleted, and replaced by new ASSESS_TYPE for categorical list, ASSESS_TYPE_RAW and ASSESS_TYPE_RAW_NAME.
- student_course_membership: new property CARELEAVER added.
