#Student on a module Instance
* [STUDENT_ID](student.md#student_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_ID](student_course_membership.md#student_course_membership_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_SEQ](student_course_membership.md#student_course_membership_seq) [1]
* [COURSE_INSTANCE_ID](course_instance.md#course_instance_id) [1]
* [MOD_INSTANCE_ID](module_instance.md#mod_instance_id) [1]
* [MOD_GRADE](#mod_grade) [1]
* [MOD_RESULT](#mod_result) [1]
* [MOD_RETAKE](#mod_retake) [0..1]
* [MOD_START_DATE](#mod_start_date) [1]
* [MOD_END_DATE](#mod_end_date) [1]
* [MOD_FIRST_MARK](#mod_first_mark) [0..1]
* [MOD_ACTUAL_MARK](#mod_actual_mark) [0..1]
* [MOD_AGREED_MARK](#mod_agreed_mark) [0..1]
* [MOD_FIRST_GRADE](#mod_first_grade) [0..1]
* [MOD_ACTUAL_GRADE](#mod_actual_grade) [0..1]
* [MOD_AGREED_GRADE](#mod_agreed_grade) [1]
* [MOD_CREDITS_ACHIEVED](#mod_credits_achieved) [1]
* [MOD_CURRENT_ATTEMPT](#mod_current_attempt) [1]
* [MOD_COMPLETED_ATTEMPT](#mod_completed_attempt) [1]
* [X_MOD_NAME](#x_mod_name) [0..1]

##MOD_GRADE
###Description.
Final grade student achieved on the module.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (256)

###Notes


##MOD_RESULT
###Description.
Indicates whether the student passed the module, didn't pass the module, deferred the module or whether this information is not known because the module hasn't been completed yet.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values

<table>
<tr><td>MOD_RESULT</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na  </td></tr>
<tr><td>3</td><td>Not completed yet</td><td>Dim wedi cwblhau</td></tr>
<tr><td>4</td><td>Deferred</td><td>Gohiriedig</td></tr>
</table>  

###Format
Int

###Notes
Code 3 is applied in all cases where the outcome is either not known (yet), or doesn't apply; because a student withdrew or deferred, for example.


##MOD_RETAKE
###Description.
Whether this is a retake of the module for that student.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values

<table>
<tr><td>MOD_RETAKE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na</td></tr>
</table>  

###Format
Int

###Notes


##MOD_START_DATE
###Description
Start date of this module instance

###Purpose
Analytics and display

###Derivation
Jisc

###Valid Values
ISO 8601 - YYYY-MM-DD

###Format
Date

###Notes
The start and end date of a module instance MUST align with the start and end date of a course instance.


##MOD_END_DATE
###Description
End date of this module instance

###Purpose
Analytics and display

###Derivation
Jisc

###Valid Values
ISO 8601 - YYYY-MM-DD

###Format
Date

###Notes
The start and end date of a module instance MUST align with the start and end date of a course instance.


##MOD_FIRST_MARK
###Description
The first or initial mark a student achieved on the module.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
0-100

###Format
Decimal

###Notes


##MOD_ACTUAL_MARK
###Description
The mark that was initially given prior to exam board ratification.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
0-100

###Format
Decimal

###Notes


##MOD_AGREED_MARK
###Description
The mark that was confirmed for a student following exam boards.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
0-100

###Format
Decimal

###Notes


##MOD_FIRST_GRADE
###Description
The first or initial grade a student achieved on the module.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes
The first grade a student receives on the module is used to help monitor what changes to marks are made during the re-assessment process.


##MOD_ACTUAL_GRADE
###Description
The grade that was initially given prior to exam board ratification.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes


##MOD_AGREED_GRADE
###Description
The grade that was confirmed for a student following exam boards.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
String (255)

###Notes


##MOD_CREDITS_ACHIEVED
###Description
The number of credits awarded for the module.

###Purpose
Analytics

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^CRDTPTS.html

###Valid Values
Any

###Format
Integer

###Notes


##MOD_CURRENT_ATTEMPT
###Description
Number of attempts taken by a student so far on a module instance.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
Integer

###Notes


##MOD_COMPLETED_ATTEMPT
###Description
Number of attempts taken by a student to complete a module instance.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Any

###Format
Integer

###Notes


##X_MOD_NAME
###Description
An extra implementation optimisation that isn't part of the UDD model. Its value is identical to that of the relevant module.MOD_NAME.

###Purpose
Implementation optimisation

###Derivation
Jisc; module.MOD_NAME

###Valid Values
Any

###Format
String (255)

###Notes
This data is generated internally from existing data, and does not need to be supplied by an institution.
