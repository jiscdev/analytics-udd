# module_instance
* [MOD_INSTANCE_ID](#mod_instance_id) [1] **
* [MOD_ID](module.md#mod_id) [1]
* [MOD_PERIOD](#mod_period) [0..1]
* [MOD_ONLINE](#mod_online) [0..1]
* [MOD_ACADEMIC_YEAR](#mod_academic_year) [1]
* [MOD_LOCATION](#mod_location) [0..1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **moduleinstance**

## Description of module_instance entity
A module_instance is the specific offer of a module to students. It therefore has a specific venue and defined assessments.

## MOD_INSTANCE_ID
### Description
Institution's unique identifier for this module_instance

### Purpose
To uniquely identify the module instance.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes


## MOD_PERIOD
### Description
Period to which module_instance relates (e.g. semester 1)

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
Each different code value in MOD_PERIOD should have a matching code value in period.PERIOD_CODE.

### Format
String (255)

### Notes
It is expected that sites / organisations will have their own code lists for MOD_PERIOD values.

## MOD_ONLINE
### Description
Whether or not this module_instance is delivered wholly online.

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
<table>
<tr><td>MOD_ONLINE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na</td></tr>
</table>  

### Format
String (255)

### Notes
Omitting this property may hinder the development or use of an effective analytics model.

## MOD_ACADEMIC_YEAR
### Description
Academic year that this module runs within - this must represent the start year of that specific academic year eg. for 2014-15 this would be 2014.

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
Year as four digits - year that the academic year starts in, with valid values being from 1900 onwards.

### Format
Int

### Notes
This is the starting year for the academic year.
This property is synonymous with ACADEMIC_YEAR.


## MOD_LOCATION
### Description
Identifies where a module is to be run. This could be campus, country, or building depending on the needs of the institutions config. Allows modules to be have a different location from the one identified at the course level detail (COURSE_LOCATION).

### Purpose
To provide details about a module and how it may differ from similar coded modules.

### Derivation
As defined by the institution and their SRS

### Valid Values
Any

### Format
String (255)

### Notes
