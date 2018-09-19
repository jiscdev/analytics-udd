# course_instance
* [COURSE_INSTANCE_ID](#course_instance_id) [1] **
* [COURSE_ID](course.md#course_id) [1]
* [START_DATE](#start_date) [0..1]
* [END_DATE](#end_date) [0..1]
* [ACADEMIC_YEAR](#academic_year) [1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **courseinstance**

## Description of course_instance entity
A course_instance is a stage of a course with a start date and an end date, often marked by a progression decision point at the end.  Example: a single academic year in a 3 year Honours degree course.

## COURSE_INSTANCE_ID
### Description
Institution's identifier for this course_instance

### Purpose
To link student to course, and course to course_instance

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes

## START_DATE
### Description
Start date for this course_instance

### Purpose
For analytics

### Derivation
Jisc

### Valid Values
Date in ISO 8601 format - YYYY-MM-DD

### Format
String in ISO 8601 Date extended format - YYYY-MM-DD

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## END_DATE
### Description
End date for this course_instance

## Purpose
For analytics

### Derivation
Jisc

### Valid Values
Date in ISO 8601 format - YYYY-MM-DD

### Format
String in ISO 8601 Date extended format - YYYY-MM-DD

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## ACADEMIC_YEAR
### Description
Academic year to which the course_instance relates. 

### Purpose
For display and analysis purposes

### Derivation
Jisc

### Valid Values
Year as four digits - year that the academic year starts in, with valid values being from 1900 onwards.

### Format
Int

### Notes
Could be derived, but academic year calendars may be different between institutions. This field could also be sourced directly from the SRS.
This property is synonymous with MOD_ACADEMIC_YEAR.
