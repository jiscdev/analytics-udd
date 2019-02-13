# assessment_instance
* [ASSESS_INSTANCE_ID](#assess_instance_id) [1] **
* [MOD_INSTANCE_ID](module_instance.md#mod_instance_id) [1] 
* [ASSESS_TYPE_ID](#assess_type_id) [0..1]
* [ASSESS_TYPE_NAME](#assess_type_name) [0..1]
* [ASSESS_DETAIL](#assess_detail) [0..1]
* [ASSESS_WEIGHT](#assess_weight) [0..1]
* [MAX_MARKS](#max_marks) [0..1]
* [MOD_ACADEMIC_YEAR](module_instance.md#mod_academic_year) [1]
* [PROVIDED_AT](#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **assessmentinstance**

## Description of assessment_instance entity
An assessment_instance is any learning activity in a module, for which a student receives a grade and/or mark. The assumption is that grades and/or marks in assessment_instances are summative.

## ASSESS_INSTANCE_ID
### Description
An institution's unique identifier for an assessment_instance

### Purpose
To uniquely identify an assessment_instance, and to link it to other entities such as module instances.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes


## ASSESS_TYPE_ID
### Description.
An institution's unique identifier for the type of assessment as defined in their student record system (e.g. CW for Coursework)

### Purpose
To provide information about the type of assessment.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes
Omitting this property may hinder the development or use of an effective analytics model.

## ASSESS_TYPE_NAME
### Description.
An institution's description for the type of assessment as defined in their student record system (e.g. Coursework).

### Purpose
To provide information about the type of assessment.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## ASSESS_DETAIL
### Description.
A textual description of the assessment component and type. For example "Lab Report (1000 words)"

### Purpose
To provide information about the type of assessment.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## ASSESS_WEIGHT
### Description.
The weighting percentage that the assessment component counts towards the module mark.

### Purpose
To provide information about the type of assessment.

### Derivation
Jisc

### Valid Values
0-100

### Format
Decimal

### Notes
Omitting this property may hinder the development or use of an effective analytics model.

## MAX_MARKS
### Description.
The maximum numeric marks that an instructor can allocate to an assessment. Used to indicate the marking scale used for an assignment.

### Purpose
To enable student performance calculations.

### Derivation
Jisc

### Valid Values
Any

### Format
Decimal

### Notes

## PROVIDED_AT

### Description
Date and time stamp of the provision of the entity file to the Learning Data Hub. If not provided, the timestamp of the file itself will be used.

### Purpose
To provide a clear indication of the date and time of when the data was supplied. Cf. date/time of extraction or update. 

### Derivation
Provider

### Valid Values
Date/time in ISO 8601 format - YYYY-MM-DDThh:mmZ or YYYY-MM-DDThh:mm

### Format
String in ISO 8601 date and time format - YYYY-MM-DDThh:mmZ or YYYY-MM-DDThh:mm

### Notes
Preferred format is YYYY-MM-DDThh:mmZ with the "Z" denoting local time zone. However, YYYY-MM-DDThh:mm is acceptable if the supplier does not hold the "Z". Do not insert "Z" if not held.