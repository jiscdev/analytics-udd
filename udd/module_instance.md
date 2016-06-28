#Module instance
* [MOD_ID](module.md#mod_id) [1]
* [MOD_INSTANCE_ID](#mod_instance_id) [1]
* [MOD_PERIOD](#mod_period) [0..1]
* [MOD_ONLINE](#mod_online) [1]
* [MOD_ACADEMIC_YEAR](#mod_academic_year) [1]
* [MOD_OPTIONAL](#mod_optional) [0..1]
* [MOD_LOCATION](#mod_location) [0..1]

##MOD_INSTANCE_ID
###Description
Institutions unique identifier for this module instance

###Purpose
For link a module instance to a student

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes


##MOD_PERIOD
###Description
Period to which module instance relates (e.g. semester 1)

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (256)

###Notes
It is expected that sites / organisations will have their own code lists for MOD_PERIOD values.

##MOD_ONLINE
###Description
Whether this module instance is delivered wholly online

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
<table>
<tr><td>MOD_ONLINE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na</td></tr>
</table>  

###Format
Int

###Notes

##MOD_ACADEMIC_YEAR
###Description
Academic year that this module runs within - this must represent the start year of that specific academic year eg. for 2014-15 this would be 2014

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Int

###Format
4 digit year

###Notes
This is the starting year for the academic year.

##MOD_OPTIONAL
###Description
Whether this instance relates to an optional module or not.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values

<table>
<tr><td>MOD_OPTIONAL</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na</td></tr>
</table>  

###Format
Int

###Notes


##MOD_LOCATION
###Description
Identifies where a module is to be run. This could be campus, country, or building depending on the needs of the institutions config. Allows modules to be have a different location from the one identified at the course level detail (COURSE_LOCATION).

###Purpose
To provide details about a module and how it may differ from similar coded modules.

###Derivation
As defined by the institution and their SRS

###Valid Values
Any

###Format
String (255)

###Notes
