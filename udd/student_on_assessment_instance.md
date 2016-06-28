#Student on assessment instance
* [STUDENT_ID](student.md#student_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_ID](student_course_membership.md#student_course_membership_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_SEQ](student_course_membership.md#student_course_membership_seq) [1]
* [MOD_INSTANCE_ID](module_instance.md#mod_instance_id) [1]
* [ASSESS_INSTANCE_ID](assessment_instance.md#assess_instance_id) [1]
* [ASSESS_SEQ_ID](#assess_seq_id) [1]
* [ASSESS_DUE_DATE](#assess_due_date) [0..1]
* [ASSESS_RETAKE](#assess_retake) [0..1]
* [ASSESS_AGREED_MARK](#assess_agreed_mark) [0..1]
* [ASSESS_ACTUAL_MARK](#assess_actual_mark) [0..1]
* [ASSESS_AGREED_GRADE](#assess_agreed_grade) [1]
* [ASSESS_ACTUAL_GRADE](#assess_actual_grade) [1]
* [ASSESSMENT_CURRENT_ATTEMPT](#assessment_current_attempt) [1]
* [ASSESSMENT_RESULT](#assessment_result) [1]
* [GRADE_DATE](#grade_date) [0..1]
* [MAX_POINTS](#max_points) [0..1]
* [X_ASSESS_DETAIL](#x_assess_detail) [0..1]
* [X_MOD_NAME](student_on_a_module_instance.md#x_mod_name) [0..1]
* [X_MOD_ID](#X_MOD_ID) [0..1]

##ASSESS_SEQ_ID
###Description.
A unique ID to indicate the order of assessments taken by a student on the assessment instance.

###Purpose
To help identify the latest assessment and the order of assessments for a student, especially for those in reassessment.
This could differ from the ASSESS_CURRENT_ATTEMPT/ASSESS_COMPLETED_ATTEMPT attributes when a student has mitigating circumstances.

###Derivation
Jisc

###Valid Values
Any

###Format
Integer

###Notes


##ASSESS_DUE_DATE
###Description.
The date an assessment instance for a student was due for submission.

###Purpose
Analytics and display

###Derivation
Jisc

###Valid Values
YYYY-MM-DD

###Format
ISO 8601

###Notes


##ASSESS_RETAKE
###Description.
Whether this is a retake of the asessment for that student.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
<table>
<tr><td>ASSESS_RETAKE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na</td></tr>
</table>  

###Format
Integer

###Notes


##ASSESS_ACTUAL_MARK
###Description.
The initial mark given for the assessment attempt.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
0-100

###Format
Decimal

###Notes


##ASSESS_AGREED_MARK
###Description.
The agreed mark for the assessment attempt.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
0-100

###Format
Decimal

###Notes


##ASSESS_ACTUAL_GRADE
###Description.
The actual grade for the assessment attempt.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes


##ASSESS_AGREED_GRADE
###Description.
The agreed grade for the assessment attempt.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes


##ASSESSMENT_CURRENT_ATTEMPT
###Description.
Number of attempts taken by a student so far on an assessment instance.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
Integer

###Notes


##ASSESSMENT_RESULT
###Description.
Indicates whether the student passed the assessment, didn't pass the assessment, deferred the assessment or whether this information is not known because the assessment hasn't been due yet.

###Purpose
Analytics

###Derivation
Jisc; student_on_a_module_instance.MOD_RESULT

###Valid Values
<table>
<tr><td>ASSESSMENT_RESULT</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na  </td></tr>
<tr><td>3</td><td>Not completed yet</td><td>Dim wedi cwblhau</td></tr>
<tr><td>4</td><td>Deferred</td><td>Gohiriedig</td></tr>
</table>  

###Format
Integer

###Notes
Code 3 is applied in all cases where the outcome is either not known (yet), or doesn't apply; because a student withdrew or deferred, for example.


##GRADE_DATE
###Description.
The date at which the grade result has been confirmed and awarded.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Not specified

###Format
Date (ISO format) - YYYY-MM-DD

###Notes
This is the date when a grade has been moderated and agreed, but before exam board confirmation. It is typically the date at which the grade is entered in a SRS.


##MAX_POINTS
###Description.
The maximum points that an instructor can allocate to an assessment. Used to indicate the marking scale used for an assignment.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Not specified

###Format
String (256)

###Notes
The value can be any alphanumeric used by any type of marking scale. E.g. 80%, B11 or 'excellent'.


##X_ASSESS_DETAIL
###Description.
An extra implementation optimisation that isn't part of the UDD model. It's value is identical to that of the relevant assessment_instance.ASSESS_DETAIL.

###Purpose
Implementation optimisation

###Derivation
Jisc; assessment_instance.ASSESS_DETAIL

###Valid Values
Any

###Format
String (255)

###Notes
This data is generated internally from existing data, and does not need to be supplied by an institution.


##X_MOD_ID
###Description.
An extra implementation optimisation that isn't part of the UDD model. Its value is identical to that of the relevant module.MOD_ID.

###Purpose
Implementation optimisation

###Derivation
Jisc; module.MOD_ID

###Valid Values
Any

###Format
String (255)

###Notes
This data is generated internally from existing data, and does not need to be supplied by an institution.
