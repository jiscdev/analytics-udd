# course_instance
* [COURSE_INSTANCE_ID](#course_instance_id) [1] **
* [COURSE_ID](course.md#course_id) [1]
* [START_DATE](#start_date) [0..1]
* [END_DATE](#end_date) [0..1]
* [ACADEMIC_YEAR](#academic_year) [1]
* [COMMENCEMENT_PERIOD](#commencement_period) [0..1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **courseinstance**

## Description of course_instance entity
A course_instance is a stage of a course with a start date and an end date, often marked by a progression decision point at the end.  Example: a single academic year in a 3 year Honours degree course.

## Note on data output
In most cases, there should be only a small number of course_instance records per academic year for any 1 course. For example, if a course_instance equates to a single academic year of a full-time course, then there would normally be 1 course_instance record for each academic year. Some providers may split course_instance records by mode of study and / or by terms or semesters, in which case there will be multiple course_instance records for a course in a single academic year. However, if more than about 4 course_instance records are generated for 1 course for a single academic year, it is possible that there has been an error in the data output process, and providers are encouraged to check this prior to import into the Learning Data Hub. 

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

## COMMENCEMENT_PERIOD
### Description
Period in which the course_instance starts (e.g. semester 1)

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
Each different code value in COMMENCEMENT_PERIOD should have a matching code value in period.PERIOD_CODE.

### Format
String (255)

### Notes
It is expected that sites / organisations will have their own code lists for COMMENCEMENT_PERIOD values.
