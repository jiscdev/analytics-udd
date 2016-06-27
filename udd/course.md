#Course
* [COURSE_ID](#course_id) [1]
* [SUBJECT](#subject) [1]
* [TITLE](#title) [1]
* [COURSE_AIM](#course_aim) [1]
* [INST_TIER_1](#inst_tier_1) [0..1]
* [INST_TIER_2](#inst_tier_2) [0..1]
* [INST_TIER_3](#inst_tier_3) [0..1]
* [TENANT_ID](institution.md#tenant_id) [0..1]

##COURSE_ID
###Description
The providers own ID for the course

###Purpose
To link relational database tables

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^OWNCOURSEID.html
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^Course_COURSEID.html

###Valid Values
Any

###Format
String (255)

###Notes
HE guidance - this field could relate to actual HESA COURSEID field or the HR institution's OWNCOURSEID field for cross-referencing purposes.

##SUBJECT
###Description
Subject coding - using JACS3

###Purpose
For display purposes

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^SBJCA.html

###Valid Values
Valid JACS3 Code. See:
https://www.hesa.ac.uk/jacs3

###Format
String (10) - Usually 4 characters, number followed by three digits

###Notes
The JACS3 coding will be used here initially, from the HE (HESA) model. Further discussion will be required around this, to discuss subject classifications for FE/ ILR.y

##TITLE
###Description
Course Name or Title

###Purpose
For display purposes

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^CTITLE.html

###Valid Value
Any

###Format
String (255)

###Notes

##COURSE_AIM
###Description
The qualification which the learner/ student is aiming for at the provider

###Purpose
For display purposes and further analysis

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^COURSEAIM.html

###Valid Values
<table>
 <tr>
  <td>COURSE_AIM</td>
  <td>DESCRIPTION (ENGLISH)</td>
  <td>DESCRIPTION (WELSH)</td>
  <td>HESA</td>
  <td>FEILR</td>
 </tr>
 <tr>
  <td>D00</td>
  <td>Doctorate degree that meets the criteria for a research-based higher degree</td>
  <td></td>
  <td>D00</td>
  <td></td>
 </tr>
 <tr>
  <td>D01</td>
  <td>New Route PhD that meets the criteria for a research-based higher degree</td>
  <td></td>
  <td>D01</td>
  <td></td>
 </tr>
 <tr>
  <td>D90</td>
  <td>Provider credit at level D that can count towards a research-based higher degree</td>
  <td></td>
  <td>D90</td>
  <td></td>
 </tr>
 <tr>
  <td>E00</td>
  <td>Doctorate degree that does not meet the criteria for a research-based higher degree</td>
  <td></td>
  <td>E00</td>
  <td></td>
 </tr>
 <tr>
  <td>E40</td>
  <td>National Vocational Qualification (NVQ) at level E</td>
  <td></td>
  <td>E40</td>
  <td></td>
 </tr>
 <tr>
  <td>E43</td>
  <td>Highly specialist diploma from a professional body</td>
  <td></td>
  <td>E43</td>
  <td></td>
 </tr>
 <tr>
  <td>E90</td>
  <td>Advanced taught study at level E for provider credit</td>
  <td></td>
  <td>E90</td>
  <td></td>
 </tr>
 <tr>
  <td>L00</td>
  <td>Masters degree that meets the criteria for a research-based higher degree</td>
  <td></td>
  <td>L00</td>
  <td></td>
 </tr>
 <tr>
  <td>L80</td>
  <td>Other postgraduate qualification at level L that meets the criteria for a research-based higher degree</td>
  <td></td>
  <td>L80</td>
  <td></td>
 </tr>
 <tr>
  <td>L90</td>
  <td>Provider credit at level L that can count towards a research-based higher degree</td>
  <td></td>
  <td>L90</td>
  <td></td>
 </tr>
 <tr>
  <td>L91</td>
  <td>Visiting research students at levels D or L, with formal or informal credit</td>
  <td></td>
  <td>L91</td>
  <td></td>
 </tr>
 <tr>
  <td>L99</td>
  <td>Research-based higher degree where the student may ultimately study at levels D or L</td>
  <td></td>
  <td>L99</td>
  <td></td>
 </tr>
 <tr>
  <td>M00</td>
  <td>Masters degree obtained typically by a combination of coursework and thesis/dissertation, that does not meet the criteria for a research-based higher degree</td>
  <td></td>
  <td>M00</td>
  <td></td>
 </tr>
 <tr>
  <td>M01</td>
  <td>Taught masters degree designed specifically as a training in research methods and intended as a preparation for a research-based higher degree</td>
  <td></td>
  <td>M01</td>
  <td></td>
 </tr>
 <tr>
  <td>M02</td>
  <td>Masters in Teaching and Learning</td>
  <td></td>
  <td>M02</td>
  <td></td>
 </tr>
 <tr>
  <td>M10</td>
  <td>Post-experience taught masters degree</td>
  <td></td>
  <td>M10</td>
  <td></td>
 </tr>
 <tr>
  <td>M11</td>
  <td>Master of Business Administration (MBA)</td>
  <td></td>
  <td>M11</td>
  <td></td>
 </tr>
 <tr>
  <td>M16</td>
  <td>Pre-registration masters degree leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>M16</td>
  <td></td>
 </tr>
 <tr>
  <td>M22</td>
  <td>Integrated undergraduate/postgraduate taught masters degree on the enhanced/extended pattern</td>
  <td></td>
  <td>M22</td>
  <td></td>
 </tr>
 <tr>
  <td>M26</td>
  <td>Integrated undergraduate/postgraduate taught masters degree on the enhanced/extended pattern leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>M26</td>
  <td></td>
 </tr>
 <tr>
  <td>M28</td>
  <td>Integrated undergraduate/postgraduate taught masters degree on the enhanced/extended pattern leading towards registration with the Architects Registration Board (Part 1 and Part 2 qualification)</td>
  <td></td>
  <td>M28</td>
  <td></td>
 </tr>
 <tr>
  <td>M40</td>
  <td>Fellowship at level M</td>
  <td></td>
  <td>M40</td>
  <td></td>
 </tr>
 <tr>
  <td>M41</td>
  <td>Diploma at level M</td>
  <td></td>
  <td>M41</td>
  <td></td>
 </tr>
 <tr>
  <td>M42</td>
  <td>Advanced professional certificate at level M</td>
  <td></td>
  <td>M42</td>
  <td></td>
 </tr>
 <tr>
  <td>M43</td>
  <td>National Vocational Qualification (NVQ) at level M</td>
  <td></td>
  <td>M43</td>
  <td></td>
 </tr>
 <tr>
  <td>M44</td>
  <td>Certificate at level M</td>
  <td></td>
  <td>M44</td>
  <td></td>
 </tr>
 <tr>
  <td>M45</td>
  <td>Scottish Vocational Qualification (SVQ) 5</td>
  <td></td>
  <td>M45</td>
  <td></td>
 </tr>
 <tr>
  <td>M50</td>
  <td>Postgraduate bachelors degree at level M obtained typically by a combination of coursework and thesis/dissertation, that does not meet the criteria for a research-based higher degree</td>
  <td></td>
  <td>M50</td>
  <td></td>
 </tr>
 <tr>
  <td>M70</td>
  <td>Professional taught qualification at level M other than a masters degree</td>
  <td></td>
  <td>M70</td>
  <td></td>
 </tr>
 <tr>
  <td>M71</td>
  <td>Postgraduate Certificate in Education or Professional Graduate Diploma in Education</td>
  <td></td>
  <td>M71</td>
  <td></td>
 </tr>
 <tr>
  <td>M72</td>
  <td>Post-registration education qualification at level M other than a masters degree for serving schoolteachers</td>
  <td></td>
  <td>M72</td>
  <td></td>
 </tr>
 <tr>
  <td>M76</td>
  <td>Post-registration health and social care qualification at level M</td>
  <td></td>
  <td>M76</td>
  <td></td>
 </tr>
 <tr>
  <td>M78</td>
  <td>Taught qualification at level M (where qualification at level H and/or level M is a pre-requisite for course entry) leading towards registration with the Architects Registration Board (Part 3 qualification)</td>
  <td></td>
  <td>M78</td>
  <td></td>
 </tr>
 <tr>
  <td>M79</td>
  <td>Level 7 Diploma in Teaching in the Lifelong Learning Sector</td>
  <td></td>
  <td>M79</td>
  <td></td>
 </tr>
 <tr>
  <td>M80</td>
  <td>Other taught qualification at level M</td>
  <td></td>
  <td>M80</td>
  <td></td>
 </tr>
 <tr>
  <td>M86</td>
  <td>Taught qualification at level M leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>M86</td>
  <td></td>
 </tr>
 <tr>
  <td>M88</td>
  <td>Taught qualification at level M (where a qualification at level H is a pre-requisite for course entry) leading towards registration with the Architects Registration Board (Part 2 qualification)</td>
  <td></td>
  <td>M88</td>
  <td></td>
 </tr>
 <tr>
  <td>M90</td>
  <td>Taught work at level M for provider credit</td>
  <td></td>
  <td>M90</td>
  <td></td>
 </tr>
 <tr>
  <td>M91</td>
  <td>Visiting taught students at levels E or M, with formal or informal credit</td>
  <td></td>
  <td>M91</td>
  <td></td>
 </tr>
 <tr>
  <td>M99</td>
  <td>Taught work at levels E or M with an unspecified qualification aim</td>
  <td></td>
  <td>M99</td>
  <td></td>
 </tr>
 <tr>
  <td>H00</td>
  <td>First degree with honours</td>
  <td></td>
  <td>H00</td>
  <td></td>
 </tr>
 <tr>
  <td>H11</td>
  <td>First degree with honours leading to Qualified Teacher Status (QTS)/registration with a General Teaching Council (GTC)</td>
  <td></td>
  <td>H11</td>
  <td></td>
 </tr>
 <tr>
  <td>H12</td>
  <td>First degree with honours leading to Early Years Teacher Status (EYTS)</td>
  <td></td>
  <td>H12</td>
  <td></td>
 </tr>
 <tr>
  <td>H16</td>
  <td>Pre-registration first degree with honours leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>H16</td>
  <td></td>
 </tr>
 <tr>
  <td>H18</td>
  <td>First degree with honours leading towards registration with the Architects Registration Board (Part 1 qualification)</td>
  <td></td>
  <td>H18</td>
  <td></td>
 </tr>
 <tr>
  <td>H22</td>
  <td>First degree with honours on the enhanced/extended pattern but at level H</td>
  <td></td>
  <td>H22</td>
  <td></td>
 </tr>
 <tr>
  <td>H23</td>
  <td>First degree with honours and diploma</td>
  <td></td>
  <td>H23</td>
  <td></td>
 </tr>
 <tr>
  <td>H41</td>
  <td>Diploma at level H</td>
  <td></td>
  <td>H41</td>
  <td></td>
 </tr>
 <tr>
  <td>H42</td>
  <td>Certificate at level H</td>
  <td></td>
  <td>H42</td>
  <td></td>
 </tr>
 <tr>
  <td>H43</td>
  <td>National Vocational Qualification (NVQ) at level H</td>
  <td></td>
  <td>H43</td>
  <td></td>
 </tr>
 <tr>
  <td>H50</td>
  <td>Postgraduate bachelors degree at level H</td>
  <td></td>
  <td>H50</td>
  <td></td>
 </tr>
 <tr>
  <td>H60</td>
  <td>Graduate diploma/certificate at level H</td>
  <td></td>
  <td>H60</td>
  <td></td>
 </tr>
 <tr>
  <td>H61</td>
  <td>Graduate diploma/certificate at level H but where a previous qualification at level H is a pre-requisite for course entry</td>
  <td></td>
  <td>H61</td>
  <td></td>
 </tr>
 <tr>
  <td>H62</td>
  <td>Pre-registration graduate diploma/certificate leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory
body</td>
  <td></td>
  <td>H62</td>
  <td></td>
 </tr>
 <tr>
  <td>H70</td>
  <td>Professional qualification at level H other than a first degree with honours</td>
  <td></td>
  <td>H70</td>
  <td></td>
 </tr>
 <tr>
  <td>H71</td>
  <td>Professional Graduate Certificate in Education</td>
  <td></td>
  <td>H71</td>
  <td></td>
 </tr>
 <tr>
  <td>H72</td>
  <td>Professional qualification at level H for serving schoolteachers other than a first degree with honours</td>
  <td></td>
  <td>H72</td>
  <td></td>
 </tr>
 <tr>
  <td>H76</td>
  <td>Post-registration health and social care qualification at level H other than a first degree with honours</td>
  <td></td>
  <td>H76</td>
  <td></td>
 </tr>
 <tr>
  <td>H78</td>
  <td>Other qualification at level H (where other qualifications at level H are a pre-requisite for course entry) leading towards registration with the Architects Registration Board (Part 3 qualification)</td>
  <td></td>
  <td>H78</td>
  <td></td>
 </tr>
 <tr>
  <td>H79</td>
  <td>Level 6 Diploma in Teaching in the Lifelong Learning Sector</td>
  <td></td>
  <td>H79</td>
  <td></td>
 </tr>
 <tr>
  <td>H80</td>
  <td>Other qualification at level H</td>
  <td></td>
  <td>H80</td>
  <td></td>
 </tr>
 <tr>
  <td>H81</td>
  <td>Other qualification at level H but where a previous qualification at level H is a pre-requisite for course entry</td>
  <td></td>
  <td>H81</td>
  <td></td>
 </tr>
 <tr>
  <td>H88</td>
  <td>Qualification at level H (where another qualification at level H is a pre-requisite for course entry) leading towards registration with the Architects Registration Board (Part 2 qualification)</td>
  <td></td>
  <td>H88</td>
  <td></td>
 </tr>
 <tr>
  <td>H90</td>
  <td>Credits at level H</td>
  <td></td>
  <td>H90</td>
  <td></td>
 </tr>
 <tr>
  <td>H91</td>
  <td>Visiting students at level H, with formal or informal credit</td>
  <td></td>
  <td>H91</td>
  <td></td>
 </tr>
 <tr>
  <td>H99</td>
  <td>Taught work at level H with an unspecified qualification aim</td>
  <td></td>
  <td>H99</td>
  <td></td>
 </tr>
 <tr>
  <td>I00</td>
  <td>Ordinary (non-honours) first degree</td>
  <td></td>
  <td>I00</td>
  <td></td>
 </tr>
 <tr>
  <td>I11</td>
  <td>Ordinary (non-honours) first degree leading to Qualified Teacher Status (QTS)/registration with a General Teaching Council (GTC)</td>
  <td></td>
  <td>I11</td>
  <td></td>
 </tr>
 <tr>
  <td>I12</td>
  <td>Ordinary (non-honours) first degree leading to Early Years Teacher Status (EYTS)</td>
  <td></td>
  <td>I12</td>
  <td></td>
 </tr>
 <tr>
  <td>I16</td>
  <td>Pre-registration ordinary (non-honours) first degree leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>I16</td>
  <td></td>
 </tr>
 <tr>
  <td>I60</td>
  <td>Graduate diploma/certificate at level I</td>
  <td></td>
  <td>I60</td>
  <td></td>
 </tr>
 <tr>
  <td>I61</td>
  <td>Graduate diploma/certificate at level I but where a previous qualification at level I or H is a pre-requisite for course entry</td>
  <td></td>
  <td>I61</td>
  <td></td>
 </tr>
 <tr>
  <td>I70</td>
  <td>Professional qualification at level I other than an ordinary (non-honours) first degree</td>
  <td></td>
  <td>I70</td>
  <td></td>
 </tr>
 <tr>
  <td>I71</td>
  <td>Qualified Teacher Status (QTS)/registration with a General Teaching Council (GTC) only</td>
  <td></td>
  <td>I71</td>
  <td></td>
 </tr>
 <tr>
  <td>I72</td>
  <td>Professional qualification at level I for serving schoolteachers</td>
  <td></td>
  <td>I72</td>
  <td></td>
 </tr>
 <tr>
  <td>I73</td>
  <td>Early Years Teacher Status (EYTS) only</td>
  <td></td>
  <td>I73</td>
  <td></td>
 </tr>
 <tr>
  <td>I74</td>
  <td>Teaching certificate (trained through the medium of Welsh)</td>
  <td></td>
  <td>I74</td>
  <td></td>
 </tr>
 <tr>
  <td>I76</td>
  <td>Post-registration health and social care qualification at level I other than an ordinary (non-honours) first degree</td>
  <td></td>
  <td>I76</td>
  <td></td>
 </tr>
 <tr>
  <td>I79</td>
  <td>Level 5 Diploma in Teaching in the Lifelong Learning Sector</td>
  <td></td>
  <td>I79</td>
  <td></td>
 </tr>
 <tr>
  <td>I80</td>
  <td>Other qualification at level I</td>
  <td></td>
  <td>I80</td>
  <td></td>
 </tr>
 <tr>
  <td>I81</td>
  <td>Other qualification at level I but where a previous qualification at level I or H is a pre-requisite for course entry</td>
  <td></td>
  <td>I81</td>
  <td></td>
 </tr>
 <tr>
  <td>I90</td>
  <td>Credits at level I</td>
  <td></td>
  <td>I90</td>
  <td></td>
 </tr>
 <tr>
  <td>I91</td>
  <td>Visiting students at level I, with formal or informal credit</td>
  <td></td>
  <td>I91</td>
  <td></td>
 </tr>
 <tr>
  <td>I99</td>
  <td>Taught work at level I with an unspecified qualification  aim</td>
  <td></td>
  <td>I99</td>
  <td></td>
 </tr>
 <tr>
  <td>J10</td>
  <td>Foundation degree</td>
  <td></td>
  <td>J10</td>
  <td></td>
 </tr>
 <tr>
  <td>J16</td>
  <td>Foundation degree which on completion meets entry  requirement for pre-registration health and social care qualification</td>
  <td></td>
  <td>J16</td>
  <td></td>
 </tr>
 <tr>
  <td>J20</td>
  <td>Diploma of Higher Education (DipHE)</td>
  <td></td>
  <td>J20</td>
  <td></td>
 </tr>
 <tr>
  <td>J26</td>
  <td>Diploma of Higher Education (DipHE) leading towards obtaining eligibility to register to practice with a health or social care or veterinary statutory regulatory body</td>
  <td></td>
  <td>J26</td>
  <td></td>
 </tr>
 <tr>
  <td>J30</td>
  <td>Higher National Diploma (HND)</td>
  <td></td>
  <td>J30</td>
  <td></td>
 </tr>
 <tr>
  <td>J41</td>
  <td>Diploma at level J</td>
  <td></td>
  <td>J41</td>
  <td></td>
 </tr>
 <tr>
  <td>J42</td>
  <td>Certificate at level J</td>
  <td></td>
  <td>J42</td>
  <td></td>
 </tr>
 <tr>
  <td>J43</td>
  <td>National Vocational Qualification (NVQ) at level J</td>
  <td></td>
  <td>J43</td>
  <td></td>
 </tr>
 <tr>
  <td>J45</td>
  <td>Scottish Vocational Qualification (SVQ) 4</td>
  <td></td>
  <td>J45</td>
  <td></td>
 </tr>
 <tr>
  <td>J76</td>
  <td>Post-registration health and social care qualification at level J</td>
  <td></td>
  <td>J76</td>
  <td></td>
 </tr>
 <tr>
  <td>J80</td>
  <td>Other qualification at level J</td>
  <td></td>
  <td>J80</td>
  <td></td>
 </tr>
 <tr>
  <td>J90</td>
  <td>Credits at level J</td>
  <td></td>
  <td>J90</td>
  <td></td>
 </tr>
 <tr>
  <td>J99</td>
  <td>Taught work at level J with an unspecified qualification aim</td>
  <td></td>
  <td>J99</td>
  <td></td>
 </tr>
 <tr>
  <td>C20</td>
  <td>Certificate of Higher Education (CertHE)</td>
  <td></td>
  <td>C20</td>
  <td></td>
 </tr>
 <tr>
  <td>C30</td>
  <td>Higher National Certificate (HNC)</td>
  <td></td>
  <td>C30</td>
  <td></td>
 </tr>
 <tr>
  <td>C41</td>
  <td>Diploma at level C</td>
  <td></td>
  <td>C41</td>
  <td></td>
 </tr>
 <tr>
  <td>C42</td>
  <td>Certificate at level C</td>
  <td></td>
  <td>C42</td>
  <td></td>
 </tr>
 <tr>
  <td>C43</td>
  <td>National Vocational Qualification (NVQ) at level C</td>
  <td></td>
  <td>C43</td>
  <td></td>
 </tr>
 <tr>
  <td>C77</td>
  <td>Level 4 Preparing to Teach in the Lifelong Learning Sector</td>
  <td></td>
  <td>C77</td>
  <td></td>
 </tr>
 <tr>
  <td>C78</td>
  <td>Level 4 Certificate in Teaching in the Lifelong Learning Sector</td>
  <td></td>
  <td>C78</td>
  <td></td>
 </tr>
 <tr>
  <td>C80</td>
  <td>Other qualification at level C</td>
  <td></td>
  <td>C80</td>
  <td></td>
 </tr>
 <tr>
  <td>C90</td>
  <td>Credits at level C</td>
  <td></td>
  <td>C90</td>
  <td></td>
 </tr>
 <tr>
  <td>C99</td>
  <td>Taught work at level C with an unspecified qualification aim</td>
  <td></td>
  <td>C99</td>
  <td></td>
 </tr>
 <tr>
  <td>P41</td>
  <td>Diploma at level P</td>
  <td></td>
  <td>P41</td>
  <td></td>
 </tr>
 <tr>
  <td>P42</td>
  <td>Certificate at level P</td>
  <td></td>
  <td>P42</td>
  <td></td>
 </tr>
 <tr>
  <td>P43</td>
  <td>National Vocational Qualification (NVQ) 3</td>
  <td></td>
  <td>P43</td>
  <td></td>
 </tr>
 <tr>
  <td>P45</td>
  <td>Scottish Vocational Qualification (SVQ) 3</td>
  <td></td>
  <td>P45</td>
  <td></td>
 </tr>
 <tr>
  <td>P50</td>
  <td>A/AS level</td>
  <td></td>
  <td>P50</td>
  <td></td>
 </tr>
 <tr>
  <td>P55</td>
  <td>Advanced Higher (Scotland)</td>
  <td></td>
  <td>P55</td>
  <td></td>
 </tr>
 <tr>
  <td>P56</td>
  <td>Higher (Scotland)</td>
  <td></td>
  <td>P56</td>
  <td></td>
 </tr>
 <tr>
  <td>P70</td>
  <td>Professional qualification at level 3</td>
  <td></td>
  <td>P70</td>
  <td></td>
 </tr>
 <tr>
  <td>P77</td>
  <td>Level 3 Preparing to Teach in the Lifelong Learning Sector</td>
  <td></td>
  <td>P77</td>
  <td></td>
 </tr>
 <tr>
  <td>P78</td>
  <td>Level 3 Certificate in Teaching in the Lifelong Learning Sector</td>
  <td></td>
  <td>P78</td>
  <td></td>
 </tr>
 <tr>
  <td>P80</td>
  <td>Other qualification at level 3</td>
  <td></td>
  <td>P80</td>
  <td></td>
 </tr>
 <tr>
  <td>P85</td>
  <td>Diploma in Foundation Studies (Art and Design) at level 3</td>
  <td></td>
  <td>P85</td>
  <td></td>
 </tr>
 <tr>
  <td>P90</td>
  <td>Credits at level 3</td>
  <td></td>
  <td>P90</td>
  <td></td>
 </tr>
 <tr>
  <td>Q41</td>
  <td>Diploma at level Q</td>
  <td></td>
  <td>Q41</td>
  <td></td>
 </tr>
 <tr>
  <td>Q42</td>
  <td>Certificate at level Q</td>
  <td></td>
  <td>Q42</td>
  <td></td>
 </tr>
 <tr>
  <td>Q43</td>
  <td>National Vocational Qualification (NVQ) 2</td>
  <td></td>
  <td>Q43</td>
  <td></td>
 </tr>
 <tr>
  <td>Q45</td>
  <td>Scottish Vocational Qualification (SVQ) 2</td>
  <td></td>
  <td>Q45</td>
  <td></td>
 </tr>
 <tr>
  <td>Q50</td>
  <td>GCSE at grade A*-C</td>
  <td></td>
  <td>Q50</td>
  <td></td>
 </tr>
 <tr>
  <td>Q56</td>
  <td>Intermediate 2 (Scotland)</td>
  <td></td>
  <td>Q56</td>
  <td></td>
 </tr>
 <tr>
  <td>Q57</td>
  <td>Standard Grade Credit (Scotland)</td>
  <td></td>
  <td>Q57</td>
  <td></td>
 </tr>
 <tr>
  <td>Q70</td>
  <td>Professional qualification at level 2</td>
  <td></td>
  <td>Q70</td>
  <td></td>
 </tr>
 <tr>
  <td>Q80</td>
  <td>Other qualification at level 2</td>
  <td></td>
  <td>Q80</td>
  <td></td>
 </tr>
 <tr>
  <td>Q90</td>
  <td>Credits at level 2</td>
  <td></td>
  <td>Q90</td>
  <td></td>
 </tr>
 <tr>
  <td>R42</td>
  <td>Certificate at level R</td>
  <td></td>
  <td>R42</td>
  <td></td>
 </tr>
 <tr>
  <td>R43</td>
  <td>National Vocational Qualification (NVQ) 1</td>
  <td></td>
  <td>R43</td>
  <td></td>
 </tr>
 <tr>
  <td>R45</td>
  <td>Scottish Vocational Qualification (SVQ) 1</td>
  <td></td>
  <td>R45</td>
  <td></td>
 </tr>
 <tr>
  <td>R50</td>
  <td>GCSE at grade D-G</td>
  <td></td>
  <td>R50</td>
  <td></td>
 </tr>
 <tr>
  <td>R56</td>
  <td>Intermediate 1 (Scotland)</td>
  <td></td>
  <td>R56</td>
  <td></td>
 </tr>
 <tr>
  <td>R57</td>
  <td>Standard Grade General (Scotland)</td>
  <td></td>
  <td>R57</td>
  <td></td>
 </tr>
 <tr>
  <td>R70</td>
  <td>Professional qualification at level 1</td>
  <td></td>
  <td>R70</td>
  <td></td>
 </tr>
 <tr>
  <td>R80</td>
  <td>Other qualification at level 1</td>
  <td></td>
  <td>R80</td>
  <td></td>
 </tr>
 <tr>
  <td>R90</td>
  <td>Credits at level 1</td>
  <td></td>
  <td>R90</td>
  <td></td>
 </tr>
 <tr>
  <td>S42</td>
  <td>National Vocational Qualification (NVQ) Entry level certificate</td>
  <td></td>
  <td>S42</td>
  <td></td>
 </tr>
 <tr>
  <td>S57</td>
  <td>Standard Grade Foundation (Scotland)</td>
  <td></td>
  <td>S57</td>
  <td></td>
 </tr>
 <tr>
  <td>S80</td>
  <td>Other qualification at further education (FE) access level</td>
  <td></td>
  <td>S80</td>
  <td></td>
 </tr>
 <tr>
  <td>S90</td>
  <td>Credits at further education (FE) access level</td>
  <td></td>
  <td>S90</td>
  <td></td>
 </tr>
 <tr>
  <td>X00</td>
  <td>Higher education (HE) access course, Quality Assurance Agency (QAA) recognised</td>
  <td></td>
  <td>X00</td>
  <td></td>
 </tr>
 <tr>
  <td>X01</td>
  <td>Higher education (HE) access course, not Quality Assurance Agency (QAA) recognised</td>
  <td></td>
  <td>X01</td>
  <td></td>
 </tr>
 <tr>
  <td>X41</td>
  <td>Welsh for Adults Entry level</td>
  <td></td>
  <td>X41</td>
  <td></td>
 </tr>
 <tr>
  <td>X42</td>
  <td>Welsh for Adults level 1</td>
  <td></td>
  <td>X42</td>
  <td></td>
 </tr>
 <tr>
  <td>X43</td>
  <td>Welsh for Adults level 2</td>
  <td></td>
  <td>X43</td>
  <td></td>
 </tr>
 <tr>
  <td>X44</td>
  <td>Welsh for Adults level 3</td>
  <td></td>
  <td>X44</td>
  <td></td>
 </tr>
 <tr>
  <td>X45</td>
  <td>Welsh for Adults level 4</td>
  <td></td>
  <td>X45</td>
  <td></td>
 </tr>
 <tr>
  <td>X46</td>
  <td>Welsh for Adults specialist/arbennig</td>
  <td></td>
  <td>X46</td>
  <td></td>
 </tr>
 <tr>
  <td>X98</td>
  <td>No formal qualification aim, below FE level</td>
  <td></td>
  <td></td>
  <td></td>
 </tr>
 <tr>
  <td>X99</td>
  <td>No formal qualification aim, below HE level</td>
  <td></td>
  <td>X99</td>
  <td></td>
 </tr>
</table>
 

###References

###Format
String (255)

###Notes
This field uses the HESA "COURSEAIM" codeset initially - with the addition of new code 'X98' to denote 'No formal qualification aim, below FE level' for FE equivalent denotation to HE code 'X99'. All course levels are denoted here (TBC with FE college, for final implementation). Specific use of the LARS codeset for FE (from ILR) may need to be considered, or a mapping/ amalgamation with the HESA codeset. This is to be discussed in consultation with the FE sector.


##INST_TIER_1
Details the top level of an institutional structure (e.g. Faculty Details)

###Purpose
For display purposes and further analysis

###Derivation
https://www.hesa.ac.uk/component/studrec/show_file/13041/a%5E_%5ETIER1.html

###Valid Values
https://www.hesa.ac.uk/component/studrec/show_file/13041/a%5E_%5ETIER1.html

###References

###Format
String (255)

###Notes


##INST_TIER_2
Details the middle level of an institutional structure (e.g. department details)

###Purpose
For display purposes and further analysis

###Derivation
https://www.hesa.ac.uk/component/studrec/show_file/13041/a%5E_%5ETIER2.html

###Valid Values
https://www.hesa.ac.uk/component/studrec/show_file/13041/a%5E_%5ETIER2.html

###References

###Format
String (255)

###Notes


##INST_TIER_3
Details the lower level of an institutional structure (e.g. department details)

###Purpose
For display purposes and further analysis

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=13041&href=^_^A^_^DEPARTMENT.html

###Valid Values
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=13041&href=^_^A^_^DEPARTMENT.html

###References

###Format
String (255)

###Notes
