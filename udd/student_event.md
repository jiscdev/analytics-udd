# student_event

* [STUDENT_EVENT_ID](#student_event_id) [1] **
* [EVENT_ID](event.md#event_id) [1] *
* [STUDENT_ID](student.md#student_id) [1] *
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.  
\* indicates that the property is part of a uniqueness constraint for this entity.

API endpoint name: **studentevent**

## Description of student_event entity

The student_event entity records that a student is registered to attend, or expected to attend, an event. Subsequently, the xapi data may describe whether or not a student attended.

## STUDENT_EVENT_ID
### Description
Primary key. Where not supplied by data provider, the primary key will be generated by the Learning Data Hub loading mechanism.

### Purpose
Enables easy reference to the student_event entity.

### Derivation
Jisc

### Valid Values
Any

### Format
String (255)

### Notes
Where not supplied by data provider, the primary key will be generated by the Learning Data Hub loading mechanism.