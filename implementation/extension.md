# Extension
This section does not form a part of the formal UDD specification.

## Description
There is provision here for data extensions at the level of property (in other words, "field-level extensions"). The purpose of this is to enable institutions and vendors to experiment with new or proprietary properties in any UDD entity that may be relevant only to one or a few institutions, and may be specific to a vendor.  For example, an institution may wish to introduce a flag on student to indicate that a student was a member of an institution's sports team.

It is not envisaged that there will be a proliferation of extensions, but rather that these will be used sparingly and with good reason. In addition, the various values in this entity should be carefully managed by the body identified in CONTROLLER.

The CONTROLLER should record the details of the extension in the Field Guide spreadsheet that has been completed for the product or service. See the [Field Guide template](https://github.com/jiscdev/analytics-udd/blob/master/media/UDD_FieldGuide_template.xls) for details.

The records in the extension entity consist of 5 parts, described here. The purpose of the record is to identify the vendor or institution that is using this extension, the entity involved, the specific record that is extended, the name of the extension property and its value.

For example (using a TSV format):

```
Tribal	student	ST123456	SPORTS_TEAM_FLAG	Y
```

Extensions data can be provided in several ways. Please refer to the Technical Guides at https://docs.analytics.alpha.jisc.ac.uk/docs/learning-records-warehouse/Home.

* [CONTROLLER](#controller) [1] *
* [ENTITY](#entity) [1] *
* [REF_KEY](#ref_key) [1] *
* [PROPERTY_NAME](#property_name) [1] *
* [PROPERTY_VALUE](#property_value) [1]

\* indicates that the property is part of a composite primary key for this entity.

## CONTROLLER
### Description
Identifies the controlling agent for this extension. This will normally be a software vendor, institution or Jisc.

### Valid Values
String (255)

### Purpose
Enables identification of a group of extensions by the controlling agent.

### Format
String (255)

### Notes


## ENTITY
### Description
Names the UDD entity extended by this record.

### Purpose
Identifies the relevant entity using the UDD entity name from its MD file.

### Valid Values
<table>
	<tr>
		<td>ENTITY</td>
	</tr>
	<tr>
		<td>assessment_instance</td>
	</tr>
	<tr>
		<td>course</td>
	</tr>
	<tr>
		<td>course_instance</td>
	</tr>
	<tr>
		<td>institution</td>
	</tr>
	<tr>
		<td>module</td>
	</tr>
	<tr>
		<td>module_instance</td>
	</tr>
	<tr>
		<td>module_vle_map</td>
	</tr>
	<tr>
		<td>period</td>
	</tr>
	<tr>
		<td>staff</td>
	</tr>
	<tr>
		<td>staff_on_course_instance</td>
	</tr>
	<tr>
		<td>staff_on_mod_instance</td>
	</tr>
	<tr>
		<td>student</td>
	</tr>
	<tr>
		<td>student_course_membership</td>
	</tr>
	<tr>
		<td>student_on_a_module_instance</td>
	</tr>
	<tr>
		<td>student_on_assessment_instance</td>
	</tr>
	<tr>
		<td>student_on_course_instance</td>
	</tr>
</table>

### Format
String (255)

### Notes

## REF_KEY
### Description
Holds the unique single primary key identifying the record in the UDD entity to which the extension applies.

### Purpose
Identifies the relevant extended record in the ENTITY.

### Valid Values
Any

### Format
String (255)

### Notes
Must use the single primary key, not a composite key.


## PROPERTY_NAME
### Description
Label for the extension.

### Purpose
Identifies the extension used.

### Valid Values
Label drawn from a vocabulary of valid labels for extensions maintained by CONTROLLER.

### Format
String (255)

### Notes


## PROPERTY_VALUE
### Description
Data held against the extension for the specific record identified by the ENTITY and REF_KEY.

### Purpose
Holds the data for the extension.

### Valid Values
Any

### Format
String (255)

### Notes
The value of this property is held as a string.  However, it should be parsable into the appropriate format for use in the extension defined in PROPERTY_NAME by CONTROLLER.
