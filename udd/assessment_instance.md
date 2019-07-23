# assessment_instance
* [ASSESS_INSTANCE_ID](#assess_instance_id) [1] **
* [MOD_INSTANCE_ID](module_instance.md#mod_instance_id) [1] 
* [ASSESS_TYPE](#assess_type) [0..1]
* [ASSESS_TYPE_RAW](#assess_type_raw) [0..1]
* [ASSESS_TYPE_RAW_NAME](#assess_type_raw_name) [0..1]
* [ASSESS_DETAIL](#assess_detail) [0..1]
* [ASSESS_SUMMATIVE](#assess_summative) [1]
* [ASSESS_WEIGHT](#assess_weight) [0..1]
* [MAX_MARKS](#max_marks) [0..1]
* [MOD_ACADEMIC_YEAR](module_instance.md#mod_academic_year) [1]
* [PROVIDED_AT](#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **assessmentinstance**

## Description of assessment_instance entity
An assessment_instance is any learning activity in a module, for which a student receives a grade and/or mark. The assumption is that most grades or marks in assessment_instances are summative, but there is provision through the ASSESS_SUMMATIVE property to indicate that a grade or mark is not summative.

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

## ASSESS_TYPE
### Description
The standardised UDD classification for the type of assessment

### Purpose
To provide standardised information about the type of assessment for filtering and analysis.

### Derivation
Jisc

### Valid Values
<table>
<tr><td>ASSESS_TYPE</td><td>DESCRIPTION (ENGLISH)</td><td>DESCRIPTION (WELSH)</td><td>DEFINITION</td></tr>
<tr><td>1</td><td>assignment or coursework</td><td></td><td>Individually submitted work</td></tr>
<tr><td>2</td><td>exam</td><td></td><td>Individual written work under exam conditions</td></tr>
<tr><td>3</td><td>group work or group discussion</td><td></td><td>Assessment of a group or participation in a group activity</td></tr>
<tr><td>4</td><td>oral exam or viva voce</td><td></td><td>Oral assessment</td></tr>
<tr><td>5</td><td>practical or observation</td><td></td><td>Lab work, performance, demonstrated practical skill or competence</td></tr>
<tr><td>6</td><td>presentation</td><td></td><td>Presentation by an individual</td></tr>
<tr><td>7</td><td>project</td><td></td><td>Individual project work</td></tr>
<tr><td>98</td><td>other</td><td></td><td>Type that does not fit into the above categories</td></tr>
</table>

### Format
String (255)

### Notes
Omitting this property may hinder the development or use of an effective analytics model.

## ASSESS_TYPE_RAW
### Description
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

## ASSESS_TYPE_NAME_RAW
### Description
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
### Description
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

## ASSESS_SUMMATIVE
### Description
Indicates whether or not the assessment_instance is summative.

### Purpose
To provide information about the assessment.

### Derivation
Jisc

### Valid Values
<table>
<tr><td>ASSESS_SUMMATIVE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td></tr>
<tr><td>1</td><td>Yes; summative</td><td>Ie</td></tr>
<tr><td>2</td><td>No; not summative</td><td>Na</td></tr>
</table> 
Default value: 1

### Format
String (255)

### Notes
This property is mandatory, and the default value is 1.

## ASSESS_WEIGHT
### Description
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
### Description
The maximum numeric marks that an instructor can allocate to an assessment. Used to indicate the marking scale used for an assignment.

### Purpose
To enable student performance calculations.

### Derivation
Jisc

### Valid Values
Any decimal value

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
Date/time in ISO 8601 format - YYYY-MM-DDThh:mm[:ss.mmm]Z

Seconds and milliseconds [:ss.mmm] are optional and will be zero filled where not given. Examples:
```
2012-03-29T10:05Z
2012-03-29T10:05:00Z
2012-03-29T10:05:00.000Z
```
### Format
String in ISO 8601 date and time format - YYYY-MM-DDThh:mm[:ss.mmm]Z

### Notes
Preferred format is YYYY-MM-DDThh:mm[:ss.mmm]Z with the "Z" denoting local time zone. However, YYYY-MM-DDThh:mm[:ss.mmm] is acceptable if the supplier does not hold the "Z". Do not insert "Z" if not held.
