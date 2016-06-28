#Student
* [STUDENT_ID](#student_id) [1]
* [ULN](#uln) [0..1]
* [DOB](#dob) [1]
* [ETHNICITY](#ethnicity) [1]
* [SEXID](#sexid) [1]
* [AGE](#age) [1]
* [LEARN_DIF](#learn_dif) [1]
* [DISABILITY1](#disability1) [1]
* [DISABILITY2](#disability2) [1]
* [DOMICILE](#domicile) [1]
* [TERMTIME_ACCOM](#termtime_accom) [1]
* [PARENTS_ED](#parents_ed) [1]
* [SOCIO_EC](#socio_ec) [1]
* [OVERSEAS](#overseas) [1]
* [APPSHIB_ID](#appshib_id) [0..1]
* [VLE_ID](#vle_id) [0..*]
* [HUSID](#husid) [0..1]

##STUDENT_ID
###Description
The institution's own unique identifier of the student. In the case or event of requiring to provide anonymous data for trial/ evaluation purposes with JISC, institutions should use a suitable method or algorithm (which can be reversed by that institution, for evaluation purposes thereafter) to ensure that this studentid provided is different to that actual ID held locally.

###Purpose
To identify the student across multiple records within an institution

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^OWNSTU.html

###References

###Format
String 255

###Notes


##ULN
###Description
Unique Learner Number. For initial trial and data model development for the predictive model, this field should be left NULL.

###Purpose
For future use, tracking student journey.

###Derivation
Skills Funding Agency: See https://www.gov.uk/government/publications/lrs-unique-learner-numbers

###References

###Format
String (10)

###Notes
The ULN can be provided as an additional point of reference, however the STUDENT_ID will always take precedence as the unique learner/ student identifier


##DOB
###Description
Student's date of birth

###Purpose
For analytics comparisons.

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^BIRTHDTE.html

###References

###Format
ISO8601 format of YYYY-MM-DD

###Notes
Cannot be NULL - a valid date of birth must be provided for all learners. A date of birth of 2099-12-31 can be provided on a temporary basis.


##ETHNICITY
###Description
This field records the ethnicity of the student, on the basis of their own self-assessment

###Purpose
To allow equal opportunities monitoring, within detailed learning analytics/ data modelling.

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^ETHNIC.html

###Format
String (10)

###Valid Values & Mappings:  

<table>
<tr><td>ETHNICITY</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td><td>HESA(ETHNIC)</td><td>FEILR(ETHNICITY)</td></tr>
<tr><td>10</td><td>White</td><td>Gwyn</td><td>10</td><td>31</td></tr>
<tr><td>13</td><td>White - Scottish</td><td>Gwyn - Alban</td><td>13</td><td>N/A</td></tr>
<tr><td>51</td><td>Irish</td><td>Gwyddel</td><td>N/A</td><td>32</td></tr>
<tr><td>14</td><td>Irish Traveller</td><td></td><td>14</td><td>N/A</td></tr>
<tr><td>15</td><td>Gypsy or Traveller</td><td></td><td>15</td><td>33</td></tr>
<tr><td>19</td><td>Other White background</td><td>Gwyn Arall</td><td>19</td><td>34</td></tr>
<tr><td>21</td><td>Black or Black British - Caribbean</td><td></td><td>21</td><td>45</td></tr>
<tr><td>22</td><td>Black or Black British - African</td><td></td><td>22</td><td>44</td></tr>
<tr><td>29</td><td>Other Black background</td><td></td><td>29</td><td>46</td></tr>
<tr><td>31</td><td>Asian or Asian British - Indian</td><td></td><td>31</td><td>39</td></tr>
<tr><td>32</td><td>Asian or Asian British - Pakistani</td><td></td><td>32</td><td>40</td></tr>
<tr><td>33</td><td>Asian or Asian British - Bangladeshi</td><td></td><td>33</td><td>41</td></tr>
<tr><td>34</td><td>Chinese</td><td></td><td>34</td><td>42</td></tr>
<tr><td>39</td><td>Other Asian background</td><td></td><td>39</td><td>43</td></tr>
<tr><td>41</td><td>Mixed - White and Black Caribbean</td><td></td><td>41</td><td>35</td></tr>
<tr><td>42</td><td>Mixed - White and Black African</td><td></td><td>42</td><td>36</td></tr>
<tr><td>43</td><td>Mixed - White and Asian</td><td></td><td>43</td><td>37</td></tr>
<tr><td>49</td><td>Other mixed background</td><td></td><td>49</td><td>38</td></tr>
<tr><td>50</td><td>Arab</td><td></td><td>50</td><td>47</td></tr>
<tr><td>80</td><td>Other ethnic background</td><td>Cefndir Ethnig Arall</td><td>80</td><td>98</td></tr>
<tr><td>90</td><td>Not known</td><td>Anhysbys</td><td>90</td><td>N/A</td></tr>
<tr><td>98</td><td>Information refused</td><td></td><td>98</td><td>99</td></tr>
<tr><td>NULL</td><td>No data</td><td> </td><td>NULL</td><td>NULL</td></tr>
</table>

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)  

###Notes
Where any ethnicity details are unknown, this field must be coded with '90'


##SEXID
###Description
To record a Learner's current sex, on the basis of their own self-assessment

###Purpose
For equal opportunities monitoring within learning analytics / data modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^SEXID.html

###Format
Int

###Valid Values & Mappings

<table>
<tr><td>SEXID</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td><td>HESA(SEXID)</td><td>FEILR(SEX)</td></tr>
<tr><td>1</td><td>Male</td><td>Gwryw</td><td>1</td><td>M  </td></tr>
<tr><td>2</td><td>Female</td><td>Beny</td><td>2</td><td>F  </td></tr>
<tr><td>3</td><td>Other</td><td>Arall</td><td>3</td><td>N/A  </td></tr>
<tr><td>4</td><td>Unknown</td><td>Anhysbys</td><td>N/A</td><td>N/A</td></tr>
<tr><td>NULL</td><td>No data</td><td> </td><td>NULL</td><td>NULL  </td></tr>
</table>

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)   

###Notes
If the sex is unknown, return code '4' in all cases


##AGE
###Description
The current age of the learner/ student

###Purpose
To be used purely for display purposes within the Learning Analytics software suite

###Format
Int

###Notes
This will typically auto-calculated on a daily basis, based on field DOB. The LA system will provide this field.


##LEARN_DIF
###Description
This field records whether the learner considers themselves to have a learning difficulty

###Purpose
For detailed analysis or intervention purposes within Learning Analytics eg. Data Insight Tool

###Derivation
https://www.hesa.ac.uk/component/studrec/show_file/14051/a%5E_%5ELEARNDIF.html

###Valid Values & Mappings

<table>
<tr><td>LEARN_DIF</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td><td>HESA(LEARNDIF)</td><td>FEILR(LLDDCAT)  </td></tr>
<tr><td>1</td><td>Moderate learning difficulty</td><td></td><td>1</td><td>10  </td></tr>
<tr><td>2</td><td>Severe learning difficulty</td><td></td><td>2</td><td>11  </td></tr>
<tr><td>10</td><td>Dyslexia</td><td></td><td>10</td><td>12  </td></tr>
<tr><td>11</td><td>Dyscalculia</td><td></td><td>11</td><td>13  </td></tr>
<tr><td>19</td><td>Other specific learning difficulty</td><td></td><td>19</td><td>94  </td></tr>
<tr><td>20</td><td>Autism spectrum disorder</td><td></td><td>20</td><td>14  </td></tr>
<tr><td>90</td><td>Multiple learning difficulties</td><td></td><td>90</td><td>3  </td></tr>
<tr><td>97</td><td>Other</td><td></td><td>97</td><td>96  </td></tr>
<tr><td>98</td><td>No learning difficulty</td><td></td><td>98</td><td>N/A  </td></tr>
<tr><td>99</td><td>Not known / information not provided</td><td></td><td>99</td><td>N/A  </td></tr>
<tr><td>NULL</td><td>No data</td><td></td><td>NULL</td><td>NULL  </td></tr>
</table>

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)  

###Format
Int

###Notes
If a learner's learning difficulty is unknown, then code '99' should be used for those cases


##DISABILITY1
###Description
Whether the student is indicated as being disabled, according to their own self-assessment. This will be their primary disability.

###Purpose
For equal opportunities monitoring within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5eDISABLE.html

###Valid Values & Mappings

<table>
<tr>
<td>DISABILITY1</td>
<td>DESCRIPTION(ENGLISH)</td>
<td>DESCRIPTION(WELSH)</td>
<td>HESA(DISABLE)</td>
<td>FEILR(LLDDCat) </td>
</tr>
<tr>
<td>0</td>
<td>No known disability</td>
<td>Dim Anabledd</td>
<td>0</td>
<td>N/A </td>
</tr>
<tr>
<td>5</td>
<td>Personal care support</td>
<td></td>
<td>5</td>
<td>N/A </td>
</tr>
<tr>
<td>7</td>
<td>An unseen disability, e.g. diabetes, epilepsy, asthma</td>
<td></td>
<td>7</td>
<td>N/A </td>
</tr>
<tr>
<td>8</td>
<td>Two or more impairments and/or disabling medical conditions</td>
<td></td>
<td>8</td>
<td>2 </td>
</tr>
<tr>
<td>51</td>
<td>A specific learning difficulty such as dyslexia dyspraxia or AD(H)D</td>
<td></td>
<td>11</td>
<td>12 </td>
</tr>
<tr>
<td>53</td>
<td>A social/communication impairment such as Asperger's syndrome/other autistic
spectrum disorder</td>
<td></td>
<td>53</td>
<td>15, 1</td>
</tr>
<tr>
<td>54</td>
<td>A long standing illness or health condition such as cancer HIV diabetes chronic
heart disease or epilepsy</td>
<td></td>
<td>54</td>
<td>95 </td>
</tr>
<tr>
<td>55</td>
<td>A mental health condition such as depression schizophrenia or anxiety
disorder</td>
<td></td>
<td>6, 55</td>
<td>9 </td>
</tr>
<tr>
<td>56</td>
<td>A physical impairment or mobility issues such as difficulty using arms or using
a wheelchair or crutches</td>
<td></td>
<td>4, 56</td>
<td>6, 93</td>
</tr>
<tr>
<td>57</td>
<td>Deaf or a serious hearing impairment</td>
<td></td>
<td>3, 57</td>
<td>5 </td>
</tr>
<tr>
<td>58</td>
<td>Blind or a serious visual impairment uncorrected by glasses</td>
<td></td>
<td>2, 58</td>
<td>4 </td>
</tr>
<tr>
<td>96</td>
<td>A disability impairment or medical condition that is not listed above</td>
<td></td>
<td>96</td>
<td>7, 8, 16, 97</td>
</tr>
<tr>
<td>97</td>
<td>Information refused</td>
<td></td>
<td>97</td>
<td>98 </td>
</tr>
<tr>
<td>98</td>
<td>Information not sought</td>
<td></td>
<td>98</td>
<td>N/A </td>
</tr>
<tr>
<td>99</td>
<td>Not known</td>
<td>Anhysbys</td>
<td>99</td>
<td>99 </td>
</tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>  

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)  

###Format
Int

###Notes
If disability is unknown, code '0' or '99' should be provided


##DISABILITY2
###Description
Whether the student is indicated as being disabled, according to their own self-assessment. This will be their secondary disability.

###Purpose
For equal opportunities monitoring within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5eDISABLE.html

###Valid Values & Mappings

<table>
<tr>
<td>DISABILITY2</td>
<td>DESCRIPTION(ENGLISH)</td>
<td>DESCRIPTION(WELSH)</td>
<td>HESA(DISABLE)</td>
<td>FEILR(LLDDCat) </td>
</tr>
<tr>
<td>0</td>
<td>No known disability</td>
<td>Dim Anabledd</td>
<td>0</td>
<td>N/A </td>
</tr>
<tr>
<td>5</td>
<td>Personal care support</td>
<td></td>
<td>5</td>
<td>N/A </td>
</tr>
<tr>
<td>7</td>
<td>An unseen disability, e.g. diabetes, epilepsy, asthma</td>
<td></td>
<td>7</td>
<td>N/A </td>
</tr>
<tr>
<td>8</td>
<td>Two or more impairments and/or disabling medical conditions</td>
<td></td>
<td>8</td>
<td>2 </td>
</tr>
<tr>
<td>51</td>
<td>A specific learning difficulty such as dyslexia dyspraxia or AD(H)D</td>
<td></td>
<td>11</td>
<td>12 </td>
</tr>
<tr>
<td>53</td>
<td>A social/communication impairment such as Asperger's syndrome/other autistic
spectrum disorder</td>
<td></td>
<td>53</td>
<td>15, 1</td>
</tr>
<tr>
<td>54</td>
<td>A long standing illness or health condition such as cancer HIV diabetes chronic
heart disease or epilepsy</td>
<td></td>
<td>54</td>
<td>95 </td>
</tr>
<tr>
<td>55</td>
<td>A mental health condition such as depression schizophrenia or anxiety
disorder</td>
<td></td>
<td>6, 55</td>
<td>9 </td>
</tr>
<tr>
<td>56</td>
<td>A physical impairment or mobility issues such as difficulty using arms or using
a wheelchair or crutches</td>
<td></td>
<td>4, 56</td>
<td>6, 93</td>
</tr>
<tr>
<td>57</td>
<td>Deaf or a serious hearing impairment</td>
<td></td>
<td>3, 57</td>
<td>5 </td>
</tr>
<tr>
<td>58</td>
<td>Blind or a serious visual impairment uncorrected by glasses</td>
<td></td>
<td>2, 58</td>
<td>4 </td>
</tr>
<tr>
<td>96</td>
<td>A disability impairment or medical condition that is not listed above</td>
<td></td>
<td>96</td>
<td>7, 8, 16, 97</td>
</tr>
<tr>
<td>97</td>
<td>Information refused</td>
<td></td>
<td>97</td>
<td>98 </td>
</tr>
<tr>
<td>98</td>
<td>Information not sought</td>
<td></td>
<td>98</td>
<td>N/A </td>
</tr>
<tr>
<td>99</td>
<td>Not known</td>
<td>Anhysbys</td>
<td>99</td>
<td>99 </td>
</tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>  

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)  

###Format
Int

###Notes
If disability is unknown, code '0' or '99' should be provided


##DOMICILE
###Description
This field holds the country code of the student's permanent home address prior to entry to the course. It is not necessarily the correspondence address of the student.

###Purpose
For detailed analysis within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5eDOMICILE.html

###Format
String (2)

###Valid Values (No Mappings)
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5eDOMICILE.html

###Notes
If a domicile country is unknown, please use code 'ZZ'


##TERMTIME_ACCOM
###Description
The current term time accomodation type of student

###Purpose
For detailed analysis within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5eTTACCOM.html

###Valid Values & Mappings

<table>
<tr><td>TERMTIME_ACCOM</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td><td>HESA(TTACCOM)</td><td>FEILR(ACCOM)  </td></tr>
<tr><td>1</td><td>Provider maintained property</td><td></td><td>1</td><td>5  </td></tr>
<tr><td>2</td><td>Parental/guardian home</td><td></td><td>2</td><td>N/A  </td></tr>
<tr><td>4</td><td>Other</td><td>Arall</td><td>4</td><td>NULL  </td></tr>
<tr><td>5</td><td>Not known</td><td>Anhysbys</td><td>5</td><td>N/A  </td></tr>
<tr><td>6</td><td>Not in attendance at the provider</td><td></td><td>6</td><td>N/A  </td></tr>
<tr><td>7</td><td>Own residence</td><td></td><td>7</td><td>N/A  </td></tr>
<tr><td>8</td><td>Other rented accommodation</td><td></td><td>8</td><td>N/A  </td></tr>
<tr><td>9</td><td>Private-sector halls</td><td></td><td>9</td><td>N/A  </td></tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>   

Please Note - N/A denotes that no mapping value is applicable (and should not be confused with NULL)  

###Format
Int

###Notes
If the type is unknown, code '5' should be used


##PARENTS_ED
###Description
Whether parents have higher education qualification

###Purpose
For detailed analysis within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a%5e_%5ePARED.html

###Valid Values

<table>
<tr><td>PARENTS_ED</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Yes</td><td>Ie  </td></tr>
<tr><td>2</td><td>No</td><td>Na  </td></tr>
<tr><td>7</td><td>No response given</td><td>Dim Ateb  </td></tr>
<tr><td>8</td><td>Don't know</td><td>Anhysbys  </td></tr>
<tr><td>9</td><td>Information refused</td><td>Gwybodaeth wedi ei ddal yn ol  </td></tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
</tr>
</table>

###Format
Int

###Notes
Where this is unknown, the code '8' should be provided. This information may not be available for FE/ ILR institutions, and only HE.


##SOCIO_EC
###Description
This field collects the socio-economic classification of students participating in HE if 21 or over at the start of their course or parental classification if under 21

###Purpose
For detailed analysis within Learning Analytics/ Data Modelling

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=14051&href=a^_^SEC.html

###Valid Values

<table>
<tr><td>SOCIO_EC</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)  </td></tr>
<tr><td>1</td><td>Higher managerial &amp; professional occupations</td><td>  </td></tr>
<tr><td>2</td><td>Lower managerial &amp; professional occupations</td><td>   </td></tr>
<tr><td>3</td><td>Intermediate occupations</td><td>  </td></tr>
<tr><td>4</td><td>Small employers &amp; own account workers</td><td>  </td></tr>
<tr><td>5</td><td>Lower supervisory &amp; technical occupations</td><td>  	</td></tr>
<tr><td>6</td><td>Semi-routine occupations</td><td>  	</td></tr>
<tr><td>7</td><td>Routine occupations</td><td>  	</td></tr>
<tr><td>8</td><td>Never worked &amp; long-term unemployed</td><td>  	</td></tr>
<tr><td>9</td><td>Not classified</td><td>Dim math</td></tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
</tr>
</table>  

###Format
Int

###Notes
Where this is unknown, the code '9' should be provided. This information may not be available for FE/ ILR institutions, and only HE.


##OVERSEAS
###Description
Whether the student is classified as a home student (UK), or European (EU) or as Overseas (rest of the world)

###Purpose
For detailed analysis within Learning Analytics/ Data Modelling

###Derivation
Jisc

###Valid Values

<table>
<tr><td>OVERSEAS</td><td>DESCRIPTION(ENGLISH)</td><td>DESCRIPTION(WELSH)</td></tr>
<tr><td>1</td><td>United Kingdom</td><td>Deyrnas Unedig  </td></tr>
<tr><td>2</td><td>Europe (EU)</td><td>Ewrop (UE)  </td></tr>
<tr><td>3</td><td>Rest of the World (Overseas)</td><td>Gweddill y Byd  </td></tr>
<tr><td>99</td><td>Not Known</td><td>Anhysbys</td></tr>
<tr>
<td>NULL</td>
<td>No data</td>
<td> </td>
</tr>
</table>  

###Format
Int

###Notes
If this value is unknown, then code '99' should be used. The mapping for these fields could be done using the Nationality indicator, or other relevant source within the HESA/ student records system database.


##APPSHIB_ID
###Description.
The person identifier used by Shibboleth / The UK Access Management Federation to grant access to the Jisc analytics student app via the Shibboleth - JWT gateway.

###Purpose
Analytics

###Derivation
https://www.internet2.edu/media/medialibrary/2013/09/04/internet2-mace-dir-eduperson-200604.html

###Valid Values
Not specified

###Format
String (256)

###Notes
There may be a more general AIM_ID property later that can be used for any UK Federation service provider ID, not just the Jisc analytics student app Shibboleth - JWT gateway.


##VLE_ID
###Description.
The ID assigned to a student by the VLE.

###Purpose
Analytics

###Derivation
Jisc

###Valid Values
Not specified

###Format
String (256)

###Notes
Note that this is not a universal user ID; there maybe several VLEs, or records from other types of tools.


##HUSID
###Description.
A HESA student identifier unique to each student. It is intended that the identifier is to be transferred with the student to each provider of higher education he or she may attend. The objective is that the use of this number will facilitate the accurate tracking of students throughout their experience within the sector for which HESA collects data.

###Purpose
Analytics

###Derivation
https://www.hesa.ac.uk/index.php?option=com_studrec&task=show_file&mnl=15051&href=a^_^HUSID.html

###Format of Valid Values
- First 2 digits:</td><td>Year of entry into provider (last 2 digits of year)
- Next 4 digits:</td><td>HESA institution identifier + 1000
- Next 6 digits:</td><td>6 digit reference number internally allocated by provider.
- Last digit:</td><td>Check digit.

###Format
String (13)

###Notes
