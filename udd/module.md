# module
* [MOD_ID](#mod_id) [1] **
* [MOD_NAME](#mod_name) [0..1]
* [MOD_SUBJECT](#mod_subject) [0..1] deprecated
* [MOD_CREDITS](#mod_credits) [0..1]
* [MOD_LEVEL](#mod_level) [0..1]
* [CREDIT_BEARING](#credit_bearing) [0..1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **module**

## Description of module entity
A module is a self-contained, formally structured unit of study, with a coherent and explicit set of learning outcomes and assessment criteria.

## Notes
This description is the same as the description for the Module entity in the HEDIIP Data Language.

## MOD_ID
### Description
The unique identifier standard across SRS and LMS for the module.

### Purpose
For analytics and to link module to module_instance

Derivation
https://www.hesa.ac.uk/collection/c16051/a/module_modid/

### Valid Values
Any

### Format
String (255)

### Notes


## MOD_NAME
### Description
The actual name of the module

### Purpose
For display purposes.

### Derivation
https://www.hesa.ac.uk/collection/c16051/a/MTITLE

### Valid Values
Any

### Format
String (255)

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## MOD_SUBJECT
### Description
Module subject - coded using JACS3 subject codes
DEPRECATED in v1.4. Use module_subject entity for preference.

### Purpose
For display purposes and analytics.

### Derivation
https://www.hesa.ac.uk/collection/c16051/a/modsbj/

https://www.hesa.ac.uk/support/documentation/jacs

### Valid Values
[JACS3 CSV](../media/jacs3-valid-entries.csv)

### Format
String (255) - For JACS3: 4 characters, capital letter followed by three digits

### Notes
For FE purposes, it will need be adapted to work with institutions specific codeset for Learning Activities. Details to be confirmed.
Omitting this property may hinder the development or use of an effective analytics model.


## MOD_CREDITS
### Description
Number of credits awarded for the module

### Purpose
For analytics

### Derivation
https://www.hesa.ac.uk/collection/c16051/a/CRDTPTS

### Valid Values
Any

### Format
Int

### Notes
Omitting this property may hinder the development or use of an effective analytics model.

## MOD_LEVEL
### Description
Level of credit points - indicates the level of module the student is studying. This has been initially based on the HESA field LEVELPTS, however may be utilised and adapted to also cater for FE.

### Purpose
Analytics

### Derivation
Jisc

### Valid Values

<table>
<tr><td>MOD_LEVEL</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>0</td><td>Entry level</td><td>  </td></tr>
<tr><td>1</td><td>HE Certificate/NVQ Level 4 or equivalent</td><td> 	</td></tr>
<tr><td>2</td><td>HE Intermediate</td><td> 	</td></tr>
<tr><td>3</td><td>HE Honours</td><td> 	</td></tr>
<tr><td>5</td><td>Undergraduate unspecified</td><td> 	</td></tr>
<tr><td>6</td><td>HE Masters</td><td> 	</td></tr>
<tr><td>7</td><td>HE Doctorate</td><td> 	</td></tr>
<tr><td>9</td><td>Not applicable</td><td> 	</td></tr>
<tr><td>A</td><td>NVQ level 1 or equivalent</td><td> 	</td></tr>
<tr><td>B</td><td>NVQ level 2 or equivalent</td><td> 	</td></tr>
<tr><td>C</td><td>NVQ level 3 or equivalent</td><td> 	</td></tr>
<tr><td>D</td><td>HND/Diploma HE</td><td> 	</td></tr>
<tr><td>E</td><td>Ordinary degrees</td><td></td></tr>
</table> 	

### Format
String (1)

### Notes


## CREDIT_BEARING
### Description
States whether or not the module carries a credit value.

### Purpose
Analytics

### Valid Values
<table>
<tr><td>CREDIT_BEARING</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>0</td><td>Not for credit</td><td>  </td></tr>
<tr><td>1</td><td>For credit, see MOD_CREDITS and MOD_LEVEL for details.</td><td> 	</td></tr>
<tr><td>2</td><td>for credit, but credit value unknown.</td><td> 	</td></tr>
</table> 	

### Format
String (1)

### Notes
