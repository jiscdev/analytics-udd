# event

* [EVENT_ID](#event_id) [1] **
* [EVENT_NAME](#event_name) [0..1]
* [EVENT_DATA_SOURCE](#event_data_source) [0..1]
* [EVENT_DESCRIPTION](#event_description) [0..1]
* [EVENT_START](#event_start) [0..1]
* [EVENT_END](#event_end) [0..1]
* [EVENT_LOCATION](#event_location) [0..1] 
* [ROOM_ID](#room_id) [0..1]
* [EVENT_TYPE](#event_type) [0..1]
* [EVENT_TYPE_RAW](#event_type_raw) [0..1]
* [MOD_INSTANCE_ID](module_instance.md#mod_instance_id) [0..1]
* [COURSE_INSTANCE_ID](course_instance.md#course_instance_id)  [0..1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **event**

## Description of event entity
The event entity records events that might be attended by a student in the future. These include events linked to modules or courses, such as lectures and seminars, as well as other more general events, such as induction meetings. Data about events will often, but not exclusively, be drawn from timetabling systems; the source is indicated in EVENT_DATA_SOURCE. The primary purpose of the event entity is to record the details of events that a student was registered to attend, or expected to attend. Subsequently, the xapi data may describe whether or not a student attended. In addition, the event record links to the [booking_event entity](https://github.com/Cetis/intelligent-campus/blob/master/udd/booking-event.md) in the Jisc Intelligent Campus specification.

## EVENT_ID
### Description
Primary key. The EVENT_ID is used to link the UDD data to xAPI attendance data in the [xAPI attendance statement](https://github.com/jiscdev/xapi/blob/1.0.3/recipes/attendance/attendance.md#object).

### Purpose
Enables easy reference to the event entity.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes
Where a provider supplies only part of the EVENT_ID and the corresponding object.id in xAPI data, these parts should be identical, so that any LDH generated primary key can be used to link UDD and xAPI data. These identifiers may also be used to link to the [booking_event entity](https://github.com/Cetis/intelligent-campus/blob/master/udd/booking-event.md) in the Jisc Intelligent Campus specification.

## EVENT_NAME
### Description
Descriptive label for the event, using local parlance

### Purpose
To provide a human-readable distinctive label for the event.

### Derivation
Provider

### Valid Values
Any

### Format
String (255)

### Notes

## EVENT_DATA_SOURCE
### Description
Provider's label showing the source of the data recorded in the event entity.

### Purpose
To identify the data source, particularly in cases where providers have multiple sources and need to view the source in LA services.

### Derivation
Provider

### Valid Values
Any  
Control of the values of this property rests with the provider and any vendor responsible for data imported into the Learning Data Hub. Consistent values for sources should be maintained.

### Format
String (255)

### Notes

## EVENT_DESCRIPTION
### Description
Short summary text about the event

### Purpose
Clarifies and expands on the EVENT_NAME

### Derivation
Provider

### Valid Values
Any

### Format
String (255)

### Notes

## EVENT_START

### Description
Planned start date and time of the event 

### Purpose
Specifies the planned start date and time of the event

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

## EVENT_END

### Description
Planned end date and time of the event 

### Purpose
Specifies the planned end date and time of the event

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

## EVENT_LOCATION
### Description
Description of where the event is to be held. This could be campus, country, or building depending on the needs of the provider's configuration. Allows events to have a different location from the one identified at the module (MOD_LOCATION) or course level detail (COURSE_LOCATION).

### Purpose
Locates the event

### Derivation
Provider

### Valid Values
Any

### Format
String (255)

### Notes

## ROOM_ID
### Description
Identifier for the room in which the event will take place

### Purpose
To link relational database tables; in particular to link to the [ROOM_ID](https://github.com/Cetis/intelligent-campus/blob/master/udd/booking-event.md#room_id) in the Jisc Intelligent Campus specification.

### Derivation
CELCAT/Scientia or other timetabling or booking system

### Valid Value
Any

### Format
String (255)

### Notes

## EVENT_TYPE
### Description
Categorises the event from a controlled list

### Purpose
Enables filtering and analysis

### Derivation
Jisc

### Valid values
<table>
	<tr><td>EVENT_TYPE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td></tr>
	<tr><td>10</td><td>Dissertation</td><td></td></tr>
	<tr><td>11</td><td>Field Trip</td><td></td></tr>
	<tr><td>12</td><td>Assessment</td><td></td></tr>
	<tr><td>13</td><td>Lecture</td><td></td></tr>
	<tr><td>14</td><td>Meeting</td><td></td></tr>
	<tr><td>15</td><td>Practical</td><td></td></tr>
	<tr><td>16</td><td>Laboratory</td><td></td></tr>
	<tr><td>17</td><td>Seminar</td><td></td></tr>
	<tr><td>18</td><td>Tutorial</td><td></td></tr>
	<tr><td>19</td><td>Workshop</td><td></td></tr>
	<tr><td>20</td><td>Study Skills</td><td></td></tr>
	<tr><td>21</td><td>Other</td><td></td></tr>
</table>

### Format
String (255)

### Notes
The list of event types represents common types seen in data. Where providers have different local types, these should be mapped to one of the event types in this list. The original value should be stored in EVENT_TYPE_RAW.  
If event type data is not supplied, this property should be omitted.

## EVENT_TYPE_RAW
### Description
The original category of the event type entered from the provider's own list of values. The value of this property should be aligned with the provider's xAPI subType vocabulary for the [attendance object.definition subType](https://github.com/jiscdev/xapi/blob/1.0.3/recipes/attendance/attendance.md#object).

### Purpose
To capture the provider's own event type name; also used in xAPI subType.

### Derivation
Provider

### Valid values
Any

### Format
String (255)

### Notes
If event type data is not supplied, this property should be omitted.
