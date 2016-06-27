#Student course membership

* [STUDENT_ID](student.md#student_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_ID](#student_course_membership_id) [1]
* [STUDENT_COURSE_MEMBERSHIP_SEQ](#student_course_membership_seq) [1]
* [COURSE_ID](course.md#course_id) [1]
* [WITHDRAWAL_REASON](#withdrawal_reason) [0..1]
* [WITHDRAWAL_DATE](#withdrawal_date) [0..1]
* [ENTRY_QUALS](#entry_quals) [1]
* [ENTRY_POINTS](#entry_points) [0..1]
* [COURSE_OUTCOME](#course_outcome) [1]
* [COURSE_GRADE](#course_grade) [1]
* [COURSE_AIM_ATTAINED](#course_aim_attained) [0..1]
* [COURSE_MARK](#course_mark) [1]
* [COURSE_EXPECTED_END_DATE](#course_expected_end_date) [1]
* [COURSE_END_DATE](#course_end_date) [1]
* [COURSE_JOIN_DATE](#course_join_date) [0..1]
* [COURSE_JOIN_AGE](#course_join_age) [0..1]
* [COHORT_ID](#cohort_id) [0..1]


##STUDENT_COURSE_MEMBERSHIP_ID
###Description
The institution's own unique identifier for the combination of one student and one course they are enrolled on.

###Purpose
To provide a unique course code for a student, for use in correctly mapping to module and assessment records.

###Derivation
As defined by the Student Record System.

###References

###Format
String (255)

###Notes
The student course membership is designed to deal with the fact that some students are enrolled on more than one course in their time at a provider. Drawing together data on their student ID alone could therefore be misleading, or at least be significantly different from students who have only ever been registered on one course. STUDENT_COURSE_MEMBERSHIP_ID partitions the study careers of those who are on multiple courses, and makes them comparable to those who have only ever been enrolled on one course.

##STUDENT_COURSE_MEMBERSHIP_SEQ
###Description
The institution's own unique identifier for the student and the course instance they are assigned to.

###Purpose
To provide a unique course instance code for a student, for use in joining a student to course instance/enrolment records

###Derivation
As defined by the Student Record System.

###References

###Format
String (255)

###Notes
The student course membership sequence ID is designed to deal with the fact that some students drop out off or enroll on more than one instance of the same course.


##WITHDRAWAL_REASON
###Description
The reason a student has withdrawn from a course (if they have)

###Purpose
For analytics

###Derivation
Based on the ILR codeset used for 'WithdrawReason' - with HESA code '05' utilised. For further information visit:

https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/449779/ILRSpecification2015_16_v3_July2015.pdf
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^WITHDRAWREASON.html
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^RSNEND.html

###Valid Values & Mappings
<table>
<tr><td>WITHDRAWAL_REASON</td><td>DESCRIPTION (ENGLISH)</td><td>DESCRIPTION (WELSH)</td><td>HESA (WITHDRAWREASON)</td><td>HESA (RSNEND)</td><td>FEILR (WITHDRAWREASON)  </td></tr>
<tr><td>2</td><td>Learner has transferred to another provider</td><td></td><td>02</td><td>03</td><td>2  </td></tr>
<tr><td>3</td><td>Learner injury / illness</td><td></td><td>03</td><td>04</td><td>3   </td></tr>
<tr><td>5</td><td>Death</td><td></td><td>N/A</td><td>05</td><td>N/A  </td></tr>
<tr><td>7</td><td>Learner has transferred between providers due to intervention by the Skills Funding Agency</td><td></td><td>07</td><td>N/A</td><td>7  </td></tr>
<tr><td>10</td><td>Gone into employment</td><td></td><td>N/A</td><td>10</td><td>N/A  </td></tr>
<tr><td>28</td><td>OLASS learner withdrawn due to circumstances outside the providers’ control</td><td></td><td>N/A</td><td>N/A</td><td>28  </td></tr>
<tr><td>29</td><td>Learner has been made redundant</td><td></td><td>29</td><td>N/A</td><td>29  </td></tr>
<tr><td>40</td><td>Learner has transferred to a new learning aim with the same provider</td><td></td><td>40</td><td>N/A</td><td>40  </td></tr>
<tr><td>41</td><td>Learner has transferred to another provider to undertake learning that meets a specific government strategy</td><td></td><td>41</td><td>N/A</td><td>41  </td></tr>
<tr><td>42</td><td>Academic failure/left in bad standing/not permitted to progress – HE learning aims only</td><td></td><td>N/A</td><td>02</td><td>42  </td></tr>
<tr><td>43</td><td>Financial reasons</td><td></td><td>N/A</td><td>06</td><td>43  </td></tr>
<tr><td>44</td><td>Other personal reasons</td><td></td><td>N/A</td><td>07</td><td>44  </td></tr>
<tr><td>45</td><td>Written off after lapse of time (HE learning aims only)</td><td></td><td>N/A</td><td>08</td><td>45  </td></tr>
<tr><td>46</td><td>Exclusion</td><td></td><td>N/A</td><td>09</td><td>46  </td></tr>
<tr><td>97</td><td>Other</td><td></td><td>97</td><td>11</td><td>97  </td></tr>
<tr><td>98</td><td>Reason not known</td><td></td><td>98</td><td>99</td><td>98  </td></tr>
<tr><td>99</td><td>Completion of course - result unknown</td><td></td><td>N/A</td><td>98</td><td>N/A</td></tr>
<tr><td>NULL</td><td>No data</td><td></td><td>NULL</td><td>N/A</td><td>NULL  </td></tr>
</table>  

###Format
Int

###Notes

##WITHDRAWAL_DATE
###Description
The date a student has withdrawn from a course (if they have)

###Purpose
For analytics

###Derivation
https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/449779/ILRSpecification2015_16_v3_July2015.pdf
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^ENDDATE.html

###Valid Values
ISO Date - YYYY-MM-DD

###Format
Int

###Notes
Would normally utilise ENDDATE (HE/ HESA) or potentially LearnActEndDate (FE/ ILR - to be confirmed) when relevant fields denote that the learner/ student has withdrawn from the learning aim/ course.

##ENTRY_QUALS
###Description
The classification of entry qualifications, prior to entry to the institution

###Purpose
For display & analytics

###Derivation
Based on HESA codings for QUALENT3, but merged with specific element of the FE ILR field 'PriorAttain'
https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/449779/ILRSpecification2015_16_v3_July2015.pdf
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^QUALENT3.html

###Valid Values & Mappings
<table>
<tr><td>ENTRY_QUALS</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td><td>HESA(QUALENT3)</td><td>FEILR(PRIORATTAIN)   </td></tr>
<tr><td>DUK</td><td>UK doctorate degree</td><td></td><td>DUK</td><td> 	</td></tr>
<tr><td>DZZ</td><td>Non-UK doctorate degree</td><td></td><td>DZZ</td><td>  	</td></tr>
<tr><td>D80</td><td>Other qualification at level D</td><td></td><td>D80</td><td>  	</td></tr>
<tr><td>MUK</td><td>UK masters degree</td><td></td><td>MUK</td><td>  	</td></tr>
<tr><td>MZZ</td><td>Non-UK masters degree</td><td></td><td>MZZ</td><td>  	</td></tr>
<tr><td>M2X</td><td>Integrated undergraduate/postgraduate taught masters degree on the enhanced/extended pattern</td><td></td><td>M2X</td><td>  	</td></tr>
<tr><td>M41</td><td>Diploma at level M</td><td></td><td>M41</td><td>  	</td></tr>
<tr><td>M44</td><td>Certificate at level M</td><td></td><td>M44</td><td>  	</td></tr>
<tr><td>M71</td><td>Postgraduate Certificate in Education or Professional Graduate Diploma in Education</td><td></td><td>M71</td><td>  	</td></tr>
<tr><td>M80</td><td>Other taught qualification at level M</td><td></td><td>M80</td><td>  	</td></tr>
<tr><td>M90</td><td>Taught work at level M for provider credit</td><td></td><td>M90</td><td>  	</td></tr>
<tr><td>M91</td><td>(Other) Qualification at level 7 or above</td><td></td><td>N/A</td><td>13  </td></tr>
<tr><td>HUK</td><td>UK first degree with honours</td><td></td><td>HUK</td><td>  	</td></tr>
<tr><td>HZZ</td><td>Non-UK first degree</td><td></td><td>HZZ</td><td>  	</td></tr>
<tr><td>H11</td><td>First degree with honours leading to Qualified Teacher Status (QTS)/registration with a General Teaching Council (GTC)</td><td></td><td>H11</td><td>  	</td></tr>
<tr><td>H71</td><td>Professional Graduate Certificate in Education</td><td></td><td>H71</td><td>  	</td></tr>
<tr><td>H80</td><td>(Other) Qualification at level H or level 6</td><td></td><td>H80</td><td>12  </td></tr>
<tr><td>JUK</td><td>UK ordinary (non-honours) first degree</td><td></td><td>JUK</td><td>  	</td></tr>
<tr><td>J10</td><td>Foundation degree</td><td></td><td>J10</td><td>  </td></tr>
<tr><td>J20</td><td>Diploma of Higher Education (DipHE)</td><td></td><td>J20</td><td>  	</td></tr>
<tr><td>J30</td><td>Higher National Diploma (HND)</td><td></td><td>J30</td><td>  	</td></tr>
<tr><td>J31</td><td>(Other) Qualification at level 5 or above (DEPRECATED SINCE 01/08/2013)</td><td></td><td>J32</td><td>5  </td></tr>
<tr><td>J49</td><td>Foundation course at level J</td><td></td><td>J49</td><td>  	</td></tr>
<tr><td>J48</td><td>Certificate in Education (CertEd) or Diploma in Education (DipEd) (i.e. non-graduate initial teacher training qualification)</td><td></td><td>J48</td><td>  	</td></tr>
<tr><td>J80</td><td>Other qualification at level J</td><td></td><td>J80</td><td>  	</td></tr>
<tr><td>C20</td><td>Certificate of Higher Education (CertHE)</td><td></td><td>C20</td><td>  	</td></tr>
<tr><td>C30</td><td>Higher National Certificate (HNC)</td><td></td><td>C30</td><td> 	</td></tr>
<tr><td>C44</td><td>Higher Apprenticeship (level 4)</td><td></td><td>C44</td><td>  	</td></tr>
<tr><td>C80</td><td>(Other) Qualification at level C or level 4</td><td></td><td>C80</td><td>4, 10  </td></tr>
<tr><td>C90</td><td>Undergraduate credits</td><td></td><td>C90</td><td>  	</td></tr>
<tr><td>P41</td><td>Diploma at level 3</td><td></td><td>P41</td><td>  	</td></tr>
<tr><td>P42</td><td>Certificate at level 3</td><td></td><td>P42</td><td>  	</td></tr>
<tr><td>P46</td><td>Award at level 3</td><td></td><td>P46</td><td>  	</td></tr>
<tr><td>P47</td><td>AQA Baccalaureate (Bacc)</td><td></td><td>P47</td><td>  	</td></tr>
<tr><td>P50</td><td>A/AS level</td><td></td><td>P50</td><td>  	</td></tr>
<tr><td>P51</td><td>14-19 Advanced Diploma (level 3)</td><td></td><td>P51</td><td>  	</td></tr>
<tr><td>P53</td><td>Scottish Baccalaureate</td><td></td><td>P53</td><td>  	</td></tr>
<tr><td>P54</td><td>Scottish Highers/Advanced Highers</td><td></td><td>P54</td><td>  	</td></tr>
<tr><td>P62</td><td>International Baccalaureate (IB) Diploma</td><td></td><td>P62</td><td>  	</td></tr>
<tr><td>P63</td><td>International Baccalaureate (IB) Certificate</td><td></td><td>P63</td><td>  	</td></tr>
<tr><td>P64</td><td>Cambridge Pre-U Diploma</td><td></td><td>P64</td><td>  	</td></tr>
<tr><td>P65</td><td>Cambridge Pre-U Certificate</td><td></td><td>P65</td><td>  	</td></tr>
<tr><td>P68</td><td>Welsh Baccalaureate Advanced Diploma (level 3)</td><td></td><td>P68</td><td>  	</td></tr>
<tr><td>P80</td><td>(Other) Qualification at level 3</td><td></td><td>P80</td><td>3  </td></tr>
<tr><td>P91</td><td>Level 3 qualifications of which some or all are subject to UCAS Tariff</td><td></td><td>P91</td><td>  	</td></tr>
<tr><td>P92</td><td>Level 3 qualifications of which none are subject to UCAS Tariff</td><td></td><td>P92</td><td>  	</td></tr>
<tr><td>P93</td><td>Level 3 qualifications of which all are subject to UCAS Tariff</td><td></td><td>P93</td><td>  	</td></tr>
<tr><td>P94</td><td>Level 3 qualifications of which some are subject to UCAS Tariff</td><td></td><td>P94</td><td>  	</td></tr>
<tr><td>Q51</td><td>14-19 Higher Diploma (level 2)</td><td></td><td>Q51</td><td>  	</td></tr>
<tr><td>Q52</td><td>Welsh Baccalaureate Intermediate Diploma (level 2)</td><td></td><td>Q52</td><td>  	</td></tr>
<tr><td>Q80</td><td>(Other) Qualification at level 2</td><td></td><td>Q80</td><td>2  </td></tr>
<tr><td>R51</td><td>14-19 Foundation Diploma (level 1)</td><td></td><td>R51</td><td>  	</td></tr>
<tr><td>R52</td><td>Welsh Baccalaureate Foundation Diploma (level 1)</td><td></td><td>R52</td><td>  	</td></tr>
<tr><td>R80</td><td>Other qualification at level 1</td><td></td><td>R80</td><td>1  </td></tr>
<tr><td>X07</td><td>(Other) Qualification below level 1</td><td></td><td>NULL</td><td>7  </td></tr>
<tr><td>X00</td><td>Higher education (HE) access course Quality Assurance Agency (QAA) recognised</td><td></td><td>X00</td><td>  	</td></tr>
<tr><td>X01</td><td>Higher education (HE) access course not Quality Assurance Agency (QAA) recognised</td><td></td><td>X01</td><td>  	</td></tr>
<tr><td>X02</td><td>Mature student admitted on basis of previous experience and/or admissions test</td><td></td><td>X02</td><td>  	</td></tr>
<tr><td>X04</td><td>Other qualification level not known</td><td></td><td>X04</td><td>97  </td></tr>
<tr><td>X05</td><td>Student has no formal qualification</td><td></td><td>X05</td><td>99  </td></tr>
<tr><td>X06</td><td>Not known</td><td></td><td>X06</td><td>98  </td></tr>
<tr><td>NULL</td><td>No data</td><td></td><td>NULL</td><td>NULL </td></tr>
</table>

###Format
Alphanumeric

###Notes


##ENTRY_POINTS
###Description
This field indicates the entry points gained by the student/ learner prior to entry to the institution. This is currently based on the UCAS entry points system. This field must be adapted or used to represent those points for entry into FE eg. using a formula to combine & calculate points to represent Maths and English qualifications upon entry for example

###Purpose
For analytics

###Derivation
Jisc

###Valid Values
Any

###Format
Int

###Notes


##COURSE_OUTCOME
###Description
This field indicates the outcome/ status of the learner's current course or learning aim. This is based on the information provided by HESA via the RSNEND field, however this has been adapted with the addition of fields to cater for FE (via the ILR CompStatus field), and can be used to fully cater for the outcomes in granular detail

###Purpose
For analytics

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^RSNEND.html
https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/449779/ILRSpecification2015_16_v3_July2015.pdf

###Valid Values
Any integer

###Format
Int

###Notes


##COURSE_GRADE
###Description
Class of award achieved by the student on this course instance. Based on HESA codeset for CLASS (HE conformity to be confirmed)

###Purpose
For analytics

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^CLASS.html

###Valid Values

<table>
<tr><td>COURSE_GRADE</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>First class honours</td><td>  	</td></tr>
<tr><td>2</td><td>Upper second class honours</td><td>  	</td></tr>
<tr><td>3</td><td>Lower second class honours</td><td> 	</td></tr>
<tr><td>4</td><td>Undivided second class honours</td><td> 	</td></tr>
<tr><td>5</td><td>Third class honours</td><td> 	</td></tr>
<tr><td>6</td><td>Fourth class honours</td><td> 	</td></tr>
<tr><td>7</td><td>Unclassified honours</td><td> 	</td></tr>
<tr><td>8</td><td>Aegrotat (whether to honours or pass)</td><td> 	</td></tr>
<tr><td>9</td><td>Pass - degree awarded without honours following an honours course</td><td> 	</td></tr>
<tr><td>10</td><td>Ordinary (to include divisions of ordinary if any) - degree awarded after following a non-honours course</td><td> 	</td></tr>
<tr><td>11</td><td>General degree - degree awarded after following a non-honours course/degree that was not available to be classified</td><td> 	</td></tr>
<tr><td>12</td><td>Distinction</td><td> 	</td></tr>
<tr><td>13</td><td>Merit</td><td> 	</td></tr>
<tr><td>14</td><td>Pass</td><td> 	</td></tr>
<tr><td>51</td><td>A FE</td><td> 	</td></tr>
<tr><td>52</td><td>B FE</td><td> 	</td></tr>
<tr><td>53</td><td>C FE</td><td> 	</td></tr>
<tr><td>54</td><td>D FE</td><td> 	</td></tr>
<tr><td>55</td><td>E FE</td><td> 	</td></tr>
<tr><td>56</td><td>F FE</td><td> 	</td></tr>
<tr><td>57</td><td>G FE</td><td> 	</td></tr>
<tr><td>61</td><td>N FE</td><td> 	</td></tr>
<tr><td>62</td><td>U FE</td><td> 	</td></tr>
<tr><td>63</td><td>X FE</td><td> 	</td></tr>
<tr><td>64</td><td>A* FE</td><td> 	</td></tr>
<tr><td>65</td><td>Y FE</td><td> 	</td></tr>
<tr><td>71</td><td>Pass FE</td><td> 	</td></tr>
<tr><td>72</td><td>Merit FE</td><td> 	</td></tr>
<tr><td>73</td><td>Distinction FE</td><td> 	</td></tr>
<tr><td>74</td><td>Fail FE</td><td> 	</td></tr>
<tr><td>81</td><td>1 FE</td><td> 	</td></tr>
<tr><td>82</td><td>2 FE</td><td> 	</td></tr>
<tr><td>83</td><td>3 FE</td><td> 	</td></tr>
<tr><td>84</td><td>4 FE</td><td> 	</td></tr>
<tr><td>85</td><td>5 FE</td><td> 	</td></tr>
<tr><td>86</td><td>6 FE</td><td> 	</td></tr>
<tr><td>87</td><td>7 FE</td><td> 	</td></tr>
<tr><td>88</td><td>8 FE</td><td> 	</td></tr>
<tr><td>89</td><td>9 FE</td><td>  </td></tr>
<tr><td>90</td><td>10 FE</td><td>  </td></tr>
<tr><td>91</td><td>Not yet awarded</td><td>  </td></tr>
</table>

###Format
Int

###Notes


##COURSE_AIM_ATTAINED
###Description
The Course Aim the student attained on the course of which they are a member.

###Purpose
Allowing the analysis of whether a student achieved the award/aim associated with the course of which they are a member.

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^COURSEAIM.html

###Valid values
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^COURSEAIM.html

Plus additional codes X98 & X99 (see notes below)

###References

###Format
String(255)

###Notes
This field uses the HESA "COURSEAIM" codeset initially - with the addition of new code 'X98' to denote 'No formal qualification aim, below FE level' for FE equivalent denotation to HE code 'X99'. All course levels are denoted here (TBC with FE college, for final implementation). Specific use of the LARS codeset for FE (from ILR) may need to be considered, or a mapping/ amalgamation with the HESA codeset. This is to be discussed in consultation with the FE sector.


##COURSE_MARK
###Description
The overall mark a student attained on their course.

###Purpose
For display purposes and further analysis

###Derivation
SRS Systems

###Valid values
0-100

###References

###Format
Decimal (IEEE 754)

###Notes


##COURSE_EXPECTED_END_DATE
###Description
The end date the student was expected to complete a course when they enrolled. This will be used to identify students who extend beyond this date.

###Purpose
Analytics and display

###Derivation
Jisc

###Valid values
YYYY-MM-DD

###References

###Format
ISO 8601

###Notes


##COURSE_END_DATE
###Description
The date on which the student left their course.

###Purpose
Analytics and display

###Derivation
Jisc

###Valid values
YYYY-MM-DD

###References

###Format
ISO 8601

###Notes
Note that there may be many reasons why a student leaves a course. This is recorded in WITHDRAWAL_REASON.

##COURSE_JOIN_DATE
###Description
This field indicates the date of the student's initial commencement of studies for this student course membership and may relate to a date prior to the current academic/financial year. Exchange-in students should have the date they commenced their studies at the reporting provider.

###Purpose
Analytics

###Derivation
HESA COMDATE
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=15051&href=a^_^COMDATE.html

###Valid values
YYYY-MM-DD

###References

###Format
ISO 8601

###Notes


##COURSE_JOIN_AGE
###Description
The age of the student when they initially commenced their studies for this student course membership. Exchange-in students should have the age they commenced their studies at the reporting provider.

###Purpose
Analytics

###Derivation
Jisc

###Valid values
0-200

###References

###Format
Int

###Notes
This value is designed to be a secondary source to check COURSE_JOIN_DATE minus DOB. In cases where COURSE_JOIN_AGE is not stored separately, it should be calculated at the ETL stage.


##COHORT_ID
###Description
An identifier for a group of students in a year cohort.

###Purpose
Display and grouping purposes, and but analysis.

###Derivation
Jisc

###Valid values
Any

###References

###Format
String (255)

###Notes
