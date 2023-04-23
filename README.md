Download Link: https://assignmentchef.com/product/solved-assignment-1-mission-plan-program
<br>
<u>Aim</u>

The objectives of this assignment includes:

<ul>

 <li>Learning about classes, objects, functions and composition</li>

 <li>Apply the concepts learnt by developing a space travel planning program</li>

</ul>

<u>Background</u>

In a theoretical flat-land universe, everything is in 2 dimensions. People, animals, plants to planets, moons, galaxies and even space itself, is in 2D. In our flat-land space (i.e. ‘flat-space’), there is a powerful organization called 2D-StarFleet (2DSF), whose goals include seeking out new life and civilization via exploration.

For this assignment, you take on the role of a mission planning specialist. You are supplied with statistical data from 2DSF’s deep space observation array, and you need to develop a program that does the following:

<ol>

 <li>read in statistical data (via manual input)</li>

 <li>compute the likelihood of life / civilization evolving in each location</li>

 <li>prioritize a list of top 5 locations for flat-space exploration</li>

 <li>compute total travel distance based on priority in c)</li>

</ol>

You need to develop a minimum of 3 classes : PointTwoD, LocationData and MissionPlan.  The next section describes the requirements for each of these classes.




<u>Task Requirements</u>




<ol>

 <li>2DSF has adopted a mapping coordinate system with its current headquarters as the origin. Please refer to <strong>Appendix A</strong>, which elaborates on this coordinate system, the unit representation and relative positioning of different star systems.</li>

</ol>




<ol>

 <li>The LocationData class helps to store statistical data (such as sun type, no. of earth-like planets, etc) that will be keyed into your program. It also implements a formula to compute a location’s <strong>civilization index</strong>, to help determine if this star system is worth travelling millions of kilometers to check out. <strong>Appendices</strong> <strong>B</strong> &amp; <strong>C</strong> provides more information about implementing this class.</li>

</ol>
















<ol>

 <li>The PointTwoD class helps to store (x, y) coordinate info, and encapsulates a LocationData object that stores the star system data pertaining to the coordinate position. It should be noted that information stored within LocationData objects are classified ‘secret’, and should not be stored / accessed elsewhere, other than via PointTwoD object ! <strong>Appendix D</strong> provides more information about implementing this class.</li>

</ol>




<ol>

 <li>The MissionPlan class is the main driver class whose methods are called to start the program. When started, it should print a menu providing the following functionalities :</li>

</ol>




<ul>

 <li>Allow user to input the statistical data</li>

 <li>Compute the <strong>civilization index</strong> (based on all statistical data entered so far)</li>

 <li>Print top 5 exploration destinations (based on all location data available)</li>

 <li>Total travel distance (to explore all recommended destinations)</li>

</ul>




<strong>Appendix E</strong> provides more information about implementing this class.




<ol>

 <li>Once the program is completed and tested to be working successfully, you are highly encouraged to add on “new features” to the program that you feel are relevant to the problem. Additional marks may be awarded subject to the relevancy and correctness of the new functionalities.</li>

</ol>




<ol>

 <li>You are to use only C++ language to develop your program. There is no restriction on the IDE as long as your source files can be compiled by g++ compiler (that comes packaged in Ubuntu Linux) and executed in the Ubuntu terminal shell environment.</li>

</ol>







<u>Deliverables</u>




<ul>

 <li>The deliverables include the following:</li>

</ul>




<ol>

 <li>The actual working C++ program (soft copy), <strong><em><u>with comments on each file, function or block of code</u></em></strong> to help the tutor understand its purpose.</li>

</ol>




<ol>

 <li>A softcopy word document that elaborates on:

  <ul>

   <li>(Interpreted) requirements of the program</li>

   <li>Diagram / Illustrations of program design</li>

   <li>Summary of implementation of each module in your program</li>

   <li>Reflections on program development (e.g. assumptions made, difficulties faced, what could have been done better, possible enhancements in future, <strong><em>what have you learnt</em></strong>, etc)</li>

  </ul></li>

</ol>




<ol>

 <li>A program demo/evaluation during lab session. You must be prepared to perform certain tasks / answer any questions posed by the tutor.</li>

</ol>










<ul>

 <li>IMPT: Please <strong>follow closely</strong>, to the submission instructions in <strong>Appendix F</strong>, which contains details about what to submit, file naming conventions, when to submit, where to submit, etc.</li>

</ul>




<ul>

 <li>The evaluation will be held during lab session where you are supposed to submit your assignment. Some time will be allocated for you to present / demonstrate your program during the session.</li>

</ul>







<u>Grading</u>




Student’s deliverable will be graded according to the following criteria:




<ul>

 <li>Program fulfills all the basic requirements stipulated by the assignment</li>

</ul>




<ul>

 <li>Successful demonstration of a working program, clarity of presentation and satisfactory answers provided during Q &amp; A session.</li>

</ul>




<ul>

 <li>Additional effort (e.g. enhancing the program with <em><u>relevant</u></em> features over and above task requirements, impressive, ‘killer’ presentation)</li>

</ul>




<ul>

 <li>After the submission of deliverables, students will be required undergo an evaluation process (to determine fulfillment of task requirements.) Further instructions will be given by the Tutor during the subsequent respective labs. Please pay attention as failure to adhere to instructions may result in deduction of marks.</li>

</ul>







Tutor’s note:

In the real working world, satisfactory completion of your tasks is no longer enough. The ability to <u>add value</u>, <u>communicate</u> and/or <u>demonstrate</u> your ideas with clarity is just as important as correct functioning of your program. The grading criteria is set to imitate such requirements on a ‘smaller scale’.

























<u>APPENDIX A</u>

<u> </u>

(Coordinate System of 2D Star Fleet, in Flat-Space)




<table>

 <tbody>

  <tr>

   <td width="113"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

























<u>APPENDIX B</u>

<u> </u>

(Implementation info for : LocationData)




Note :

The section below describes the compulsory requirements for class constructors, attributes and methods. However, you are free to implement any additional attributes / methods, as long as it is related to the purpose of the class.




Class Name : LocationData




Attributes :




<table>

 <tbody>

  <tr>

   <td width="170"><strong>Name</strong></td>

   <td width="69"><strong>Type</strong></td>

   <td width="456"><strong>Remarks</strong></td>

  </tr>

  <tr>

   <td width="170">sunType</td>

   <td width="69">String</td>

   <td width="456">Different types sun has great influence on the possibility of life in the star system.</td>

  </tr>

  <tr>

   <td width="170">noOfEarthLikePlanets</td>

   <td width="69">integer</td>

   <td width="456">The bigger this number, the better the chances that life can be found</td>

  </tr>

  <tr>

   <td width="170">noOfEarthLikeMoons</td>

   <td width="69">integer</td>

   <td width="456">The bigger this number, the better the chances that life can be found</td>

  </tr>

  <tr>

   <td width="170">aveParticulateDensity</td>

   <td width="69">float</td>

   <td width="456">Refers to density of particulates like sand, rocks, asteroids over the area of the star system. The lower the number, the better</td>

  </tr>

  <tr>

   <td width="170">avePlasmaDensity</td>

   <td width="69">float</td>

   <td width="456">Refers to the density of radiation and gases averaged over the area of the star system. The lower the number, the better</td>

  </tr>

  <tr>

   <td width="170"> </td>

   <td width="69"> </td>

   <td width="456"> </td>

  </tr>

 </tbody>

</table>







Constructors :




1<sup>st</sup> Constructor –

no parameters. Initialize all String variables to empty string, all int and float variables to 0.




2<sup>nd</sup> Constructor –

5 parameters. Initialize <u>all attribute variables</u> to the parameter’s values respectively.







Methods :

<ul>

 <li>Assessor (get) and Mutator (set) for each attribute(s)</li>

 <li>toString() method that returns a String, containing the name of each attribute and its value respectively</li>

 <li><strong>static</strong> method computeCivIndex()    Note : refer to Appendix C, for this method’s                                                                                          algorithm!</li>

</ul>













<u>APPENDIX C</u>

<u> </u>

(Implementation algorithm for : computeCivIndex())




<u>Return type</u>




A float value, (the higher this value, the greater the possibility of life in the star system)




<u>Parameters (arguments) </u>




1<sup>st</sup> Parameter            : sunType, String

2<sup>nd</sup> Parameter           : noOfEarthLikePlanets, integer

3<sup>rd</sup> Parameter            : noOfEarthLikeMoons, integer

4<sup>th</sup> Parameter            : aveParticulateDensity, float

5<sup>th</sup> Parameter            : avePlasmaDensity, float




<u>Algorithm</u>




1<sup>st</sup> step, is to convert sunType into a percentage value ‘sunTypePercent’, based on the table below.

<table>

 <tbody>

  <tr>

   <td width="7"></td>

   <td width="336"></td>

   <td width="49"></td>

   <td width="276"></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="2"></td>

   <td rowspan="3"></td>

  </tr>

  <tr>

   <td></td>

   <td width="336">

    <table width="100%">

     <tbody>

      <tr>

       <td>

        <table>

         <tbody>

          <tr>

           <td width="86">sunType</td>

           <td width="240">%-tage value(possibility of supporting life …)</td>

          </tr>

          <tr>

           <td width="86">“Type O”</td>

           <td width="240">30%</td>

          </tr>

          <tr>

           <td width="86">“Type B”</td>

           <td width="240">45%</td>

          </tr>

          <tr>

           <td width="86">“Type A”</td>

           <td width="240">60%</td>

          </tr>

          <tr>

           <td width="86">“Type F”</td>

           <td width="240">75%</td>

          </tr>

          <tr>

           <td width="86">“Type G”</td>

           <td width="240">90%</td>

          </tr>

          <tr>

           <td width="86">“Type K”</td>

           <td width="240">80%</td>

          </tr>

          <tr>

           <td width="86">“Type M”</td>

           <td width="240">70%</td>

          </tr>

         </tbody>

        </table> </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

  <tr>

   <td></td>

  </tr>

 </tbody>

</table>














































2<sup>nd</sup> step, is to compute based on the formula below:




Civ. Index =

[ (sunTypePercent / 100) – (aveParticulateDensity + avePlasmaDensity)  / 200 ]  x

[ noOfEarthLikePlanets +  noOfEarthLikeMoons ]




<em>E.g.  Assuming : </em>

<em>sunType</em><em> = “Type B”, aveParticulateDensity = 20%, avePlasmaDensity  = 50%, noOfEarthLikePlanets = 5, noOfEarthLikeMoons  = 10, then</em>

<em> </em>

<em>Civ. Index = [ (45/100) – (20 + 50) / 200 ] x [ 5 + 10 ] = 1.5</em>










<u>APPENDIX D</u>

<u> </u>

(Implementation info for : PointTwoD)




Note :

The section below describes the compulsory requirements for class constructors, attributes and methods. However, you are free to implement any additional attributes / methods, as long as it is related to the purpose of the class.




Class Name : PointTwoD




Attributes :




<table>

 <tbody>

  <tr>

   <td width="103"><strong>Name</strong></td>

   <td width="109"><strong>Type</strong></td>

   <td width="480"><strong>Remarks</strong></td>

  </tr>

  <tr>

   <td width="103">x</td>

   <td width="109">integer</td>

   <td width="480">The x-ordinate of the candidate star system, w.r.t. 2DSF’s HQ (origin)</td>

  </tr>

  <tr>

   <td width="103">y</td>

   <td width="109">integer</td>

   <td width="480">The y-ordinate of the candidate star system, w.r.t. 2DSF’s HQ (origin)</td>

  </tr>

  <tr>

   <td width="103">locationData</td>

   <td width="109">LocationData</td>

   <td width="480">The statistical data about the star system, tied to this (x, y) coordinate</td>

  </tr>

  <tr>

   <td width="103">civIndex</td>

   <td width="109">float</td>

   <td width="480">The computed civilization index value should be stored here</td>

  </tr>

 </tbody>

</table>







Constructors :




1<sup>st</sup> Constructor –

no parameters. Initialize all String variables to empty string, all int and float variables to 0.




2<sup>nd</sup> Constructor –

3 parameters. Initialize <u>all attribute variables</u> to the parameter’s values respectively.







Methods :

<ul>

 <li>Assessor (get) and Mutator (set) for each attribute(s)</li>

 <li>toString() method that returns a String, containing the name of each attribute and its value respectively</li>

</ul>


































<u>APPENDIX E</u>

<u> </u>

(Implementation info for : MissionPlan class)




This class contains the <strong>main ()</strong> method which declares and instantiates all other classes (i.e. LocationData, PointTwoD) and sets up all the necessary interactions to perform its task.







The figure on the left describes a sample interaction between the main menu and ‘<em>Input statistical data</em>’ sub-menu



































































The figure on the right describes a sample interaction between the main menu and ‘<em>Compute civ. index value (for all records)</em>’ function.




<strong>Note</strong> : The example assumes the case where there has only been 3 statistical data records input so far, hence, the message that ‘<em>3 records were updated</em>’!










The figure on the right describes a sample interaction between the main menu and ‘<em>Print top 5 exploration destinations</em>’ function.




<strong>Note</strong> : The example assumes the case where there has only been 3 statistical data records input so far. Hence all records are displayed, sorted in descending order by Civ Idx value!

<table>

 <tbody>

  <tr>

   <td width="512"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>































The figure on the right describes a sample interaction between the main menu and ‘<em>Print total travel distance</em>’ function.




<strong>Note 1</strong> : The formula to compute a straight line distance between 2 points on the map is …

<table>

 <tbody>

  <tr>

   <td width="3"></td>

   <td width="203"></td>

   <td width="329"></td>

   <td width="133"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="2"></td>

   <td></td>

  </tr>

 </tbody>

</table>
















<strong>Note 2</strong> : Assuming there are only

3 records with Civ Idx computed,

the total travel distance would be :




dist (HQ <strong><em>to</em></strong> Star Sys. 1) + dist (Star Sys. 1 <strong><em>back to</em></strong> HQ to re-fuel)


dist (HQ <strong><em>to</em></strong> Star Sys. 2) + dist (Star Sys. 2 <strong><em>back to</em></strong> HQ to re-fuel)


dist (HQ <strong><em>to</em></strong> Star Sys. 3) + dist (Star Sys. 3 <strong><em>back to</em></strong> HQ to re-fuel)




= 2 (d1 + d2 + d3)




<strong>Note 3</strong> : If there are more than 5 records (e.g. 15), then total travel distance should compute the total distances for the trips to the <u>top 5 exploration destinations</u> output by your menu choice 3) !










<u>APPENDIX F</u>

<u> </u>

Submission Instructions  (V. IMPT!!)







<ul>

 <li><strong>Deliverables</strong></li>

</ul>




<ol>

 <li>All submissions should be in <strong>softcopy</strong>, unless otherwise instructed</li>

</ol>




<ol>

 <li>For the actual files to be submitted, you typically need to include the following:</li>

</ol>




<ul>

 <li>word document report (e.g. <strong>*.doc</strong>), save as <u>MS Word 97-2003</u> format</li>

</ul>




<ul>

 <li>the source file(s), (e.g. *<strong>.h</strong>, *<strong>.o</strong>, or *<strong>.cpp</strong> files)</li>

</ul>




<ul>

 <li>the executable file, compile into an executable file with <strong>*.exe</strong></li>

</ul>

(e.g. Assn1.<strong>exe</strong>)







<ul>

 <li><strong>How to package</strong></li>

</ul>




Compress all your assignment files into a <u>single zip file</u>. Please use the following naming             format :




<strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong>_Assn<strong>1</strong>_<strong>&lt;Stud. No.&gt;_&lt;Name&gt;.zip</strong>













<em>Example : </em> <strong>FT</strong>_Assn<strong>1</strong>_<strong>1234567_JohnDoeAnderson. zip</strong>







<ul>

 <li><strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong> Use “<strong>FT</strong>” for <strong>F</strong>ull-<strong>T</strong>ime student, “<strong>PT</strong>” if you are <strong>P</strong>art-<strong>T</strong>ime student</li>

</ul>




<ul>

 <li>Assn<strong>1</strong> if you are submitting assignment <strong>1</strong>, Assn<strong>2</strong> if submitting assignment <strong>2</strong></li>

</ul>




<ul>

 <li><strong>&lt;Stud. No.&gt;</strong> refers to your UOW student number (e.g. 1234567)</li>

</ul>




<ul>

 <li><strong>&lt;Name&gt;</strong> refers to your UOW registered name (e.g. JohnDoeAnderson)</li>

</ul>

























<ul>

 <li><strong>Where to submit </strong></li>

</ul>




Please submit your assignment via Moodle eLearning site.







<strong>In the event of UNFORSEEN SITUATIONS : </strong>

( E.g.  Student’s moodle account not ready, cannot login to moodle, eLearning site down on submission day, unable to upload assignment, etc )







Please email your single zip file to your tutor at :




<a href="/cdn-cgi/l/email-protection#5f3c2c3c366d6f6b2a30281f263e373030713c3032"><span class="__cf_email__" data-cfemail="620111010b505256170d15221b030a0d0d4c010d0f">[email protected]</span></a>      for<em> <strong>FULL</strong></em> TIME students

<table>

 <tbody>

  <tr>

   <td width="498"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>







<a href="/cdn-cgi/l/email-protection#fa99899993c8cace8f958dba839b929595d4999597"><span class="__cf_email__" data-cfemail="197a6a7a702b292d6c766e596078717676377a7674">[email protected]</span></a>      for <strong><em>PART</em></strong> TIME students




In your email <strong>subject</strong> line, type in the following information :




<strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong> &lt;assignment info&gt; &lt;<strong>student number</strong>&gt; and &lt;<strong>name</strong>&gt;.

<table>

 <tbody>

  <tr>

   <td width="155"></td>

   <td width="41"></td>

   <td width="40"></td>

   <td width="14"></td>

   <td width="57"></td>

   <td width="47"></td>

   <td width="33"></td>

   <td width="47"></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="2"></td>

   <td rowspan="3"></td>

   <td></td>

   <td rowspan="4"></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="2"></td>

   <td></td>

   <td></td>

   <td rowspan="4"></td>

  </tr>

  <tr>

   <td></td>

   <td rowspan="4"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

 </tbody>

</table>










Example:




<strong>            To</strong>                   :           <strong><a href="/cdn-cgi/l/email-protection#a5c6d6c6cc979591d0cad2e5dcc4cdcaca8bc6cac8">tutor’s</a> email</strong> (see above)




<strong>            Subject</strong>          :           <strong>FT</strong> Assn<strong>1</strong> <strong>1234567</strong> <strong>JohnDoeAnderson</strong>







<strong><em>Note 1 : </em></strong>        The timestamp shown on tutor’s email Inbox will be used to determine if the                               assignment is late or not.




<strong><em>Note 2 : </em></strong>        After email submission, your mailbox’s  <strong><em>sent folder</em></strong>  would have a                                         copy (record) of your sent email, please <strong><u>do not delete</u></strong> that copy !!  It could                                     be used to prove your timely submission, in case the Tutor did not receive                                     your email!



















<ul>

 <li><strong>When to submit</strong></li>

</ul>




<ol>

 <li>Depending on the time-table, a <u>demo / evaluation for your assignment</u> may be scheduled during the:

  <ul>

   <li>3<sup>rd</sup> – 5<sup>th</sup> lab session for the semester (i.e. lab 3 – 5), for Full Time (<strong>FT</strong>) students</li>

   <li>2<sup>nd</sup> – 4<sup>th</sup> lab session for the semester (i.e. lab 2 – 4), for Part Time (<strong>PT</strong>) students</li>

  </ul></li>

</ol>




Please consult your tutor for further details. Some time may be allocated for each student to present / explain your system design during the session.







<ol>

 <li>Please refer to the following table on the different submission events and deadlines</li>

</ol>




<table>

 <tbody>

  <tr>

   <td width="93"><strong>Assignment</strong></td>

   <td colspan="2" width="228"><strong>Submission Deadline</strong><strong>(latest by 2300 hrs)</strong></td>

   <td rowspan="2" width="150"><strong>Assignment Evaluation (Tasks), during …</strong></td>

   <td rowspan="2" width="182"><strong>Email Evaluation files by :</strong></td>

  </tr>

  <tr>

   <td width="93"> </td>

   <td width="114">PT</td>

   <td width="114">FT</td>

  </tr>

  <tr>

   <td width="93">1</td>

   <td width="114">23 / 10 / 2016</td>

   <td width="114">26 / 10 / 2016</td>

   <td width="150">Lab 2(PT), Lab 3(FT)</td>

   <td width="182">End of Lab 2(PT), Lab 3(FT)</td>

  </tr>

  <tr>

   <td width="93">2</td>

   <td width="114">01 / 11 / 2016</td>

   <td width="114">02 / 11 / 2016</td>

   <td width="150">Lab 3(PT), Lab 4(FT)</td>

   <td width="182">End of Lab 3(PT), Lab 4(FT)</td>

  </tr>

  <tr>

   <td width="93">3</td>

   <td width="114">13 / 11 / 2016</td>

   <td width="114">15 / 11 / 2016</td>

   <td width="150">Lab 4(PT), Lab 5(FT)</td>

   <td width="182">End of Lab 4(PT), Lab 5(FT)</td>

  </tr>

 </tbody>

</table>







Note: (PT) = Part Time Students, (FT) = Full Time Students !







<ol>

 <li><strong>Example #1</strong>, for Full Time (<strong>FT</strong>) students submitting Assignment <strong>1</strong> …</li>

</ol>




<ul>

 <li>Submit your zip file to Tutor by <strong>26</strong> / <strong>10</strong> / <strong>2016</strong>, 2330 hrs</li>

</ul>




<ul>

 <li>Setup your <u>Assn <strong>1</strong></u> program for evaluation <u>on the date</u> of : <strong>Lab 3</strong></li>

</ul>




<ul>

 <li>Finish evaluation tasks, email <u>Assn <strong>1</strong></u> evaluation files <u>by end</u> of : <strong>Lab 3</strong></li>

</ul>







<ol>

 <li><strong>Example #2</strong>, for Part Time (<strong>PT</strong>) students submitting Assignment <strong>3</strong> …</li>

</ol>




<ul>

 <li>Submit your zip file to Tutor by <strong>13</strong> / <strong>11</strong> / <strong>2016</strong>, 2330 hrs</li>

</ul>




<ul>

 <li>Setup your <u>Assn <strong>3</strong></u> program for evaluation <u>on the date</u> of : <strong>Lab 4</strong></li>

</ul>




<ul>

 <li>Finish evaluation tasks, email <u>Assn <strong>3</strong></u> evaluation files <u>by end</u> of : <strong>Lab 4</strong></li>

</ul>













<ul>

 <li><strong>Please help by paying attention to the following …</strong></li>

</ul>







<strong>! VERY IMPORTANT !</strong>




PLEASE FOLLOW THE GUIDELINES IN ALL ASSIGNMENT APPENDICES !!




PLEASE FOLLOW THE SUBMISSION INSTRUCTIONS FROM <strong>1</strong> TO <strong>4</strong> !!




IF YOU ARE <strong>NOT SURE</strong>,




PLEASE <strong>CHECK WITH YOUR TUTOR</strong> DURING LABS / LECTURES !




OR …




PLEASE EMAIL YOUR ENQUIRIES TO YOUR TUTOR !







MARKS <u>WILL BE DEDUCTED</u> IF YOU FAIL TO FOLLOW INSTRUCTIONS !!







Example :




<ul>

 <li>Your report document or zip file does not follow naming convention</li>

 <li>Your email address does not include your name (i.e. cannot be used to identify sender)</li>

 <li>You have no email subject</li>

</ul>




<ul>

 <li>Wrong naming or <strong>misleading information</strong> given</li>

</ul>

(e.g. putting “Assn2” in email subject, when you are submitting “Assn1”)

(e.g. naming “Assn1” in your zip file, but inside contains Assn2 files )




<ul>

 <li>Your submission cannot be downloaded and unzipped</li>

 <li>Your report cannot be opened by Microsoft Word 2003</li>

 <li>Your program cannot be re-compiled and/or executable file cannot run</li>

 <li>You email to the WRONG tutor</li>

</ul>







<strong> </strong>

<ul>

 <li><strong>Re-submission administration</strong></li>

</ul>




After the deadline, (on case-by-case basis), some students / grp may be granted             an opportunity for an un-official resubmission by the tutor. If this is so, please adhere to the following instructions carefully:




&lt;Step 1&gt;




Zip up for re-submission files according to the following format :




<strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong>_Assn<strong>1</strong>_<strong>Resubmit_v1</strong>_<strong>&lt;Stud. No.&gt; _&lt;Name&gt;.zip</strong>




<em>    Example : </em> <strong>FT</strong> _ Assn<strong>1</strong>_Resubmit_v1_<strong>1234567_JohnDoeAnderson. zip</strong>




<ul>

 <li><strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong> Use “<strong>FT</strong>” for <strong>F</strong>ull-<strong>T</strong>ime student, “<strong>PT</strong>” if you are <strong>P</strong>art-<strong>T</strong>ime student</li>

</ul>




<ul>

 <li>Assn<strong>1</strong> if you are submitting assignment <strong>1</strong>, Assn<strong>2</strong> if submitting assignment <strong>2</strong></li>

</ul>




<ul>

 <li><strong>Resubmit_v1 </strong>if this is your <strong>1<sup>st</sup> </strong>re-submission</li>

</ul>




<ul>

 <li><strong>Resubmit_v2</strong> if this is your <strong>2<sup>nd</sup> </strong>re-submission</li>

</ul>




<ul>

 <li><strong>&lt;Stud. No.&gt;</strong> refers to your UOW student number (e.g. <strong>1234567</strong>)</li>

</ul>




<ul>

 <li><strong>&lt;Name&gt;</strong> refers to your UOW registered name (e.g. <strong>JohnDoeAnderson</strong>)</li>

</ul>




<ul>

 <li>IMPT – To prevent Tutor’s Inbox from blowing up in his face, each student is <u>only allowed to re-submit twice</u>, for each assignment only!</li>

</ul>







&lt;Step 2&gt;




Please email your single zip file to your tutor’s email (refer to section 3) – Where to submit)




In your email <strong>subject</strong> line, type in the following information :




<strong>&lt;FT</strong><strong>/</strong><strong>PT&gt;</strong> &lt;assignment info&gt;  &lt;re-submission ver.&gt; &lt;<strong>student number</strong>&gt; and &lt;<strong>name</strong>&gt;

<table>

 <tbody>

  <tr>

   <td width="93"></td>

   <td width="102"></td>

   <td width="9"></td>

   <td width="41"></td>

   <td width="34"></td>

   <td width="29"></td>

   <td width="80"></td>

   <td width="83"></td>

   <td width="25"></td>

   <td width="123"></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="4"></td>

   <td rowspan="3"></td>

   <td colspan="3"></td>

   <td rowspan="6"></td>

  </tr>

  <tr>

   <td></td>

   <td colspan="4"></td>

   <td></td>

   <td rowspan="4"></td>

  </tr>

  <tr>

   <td></td>

   <td rowspan="4"></td>

   <td></td>

   <td rowspan="2"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

 </tbody>

</table>










Example:




<strong>            To</strong>                   :           <strong>tutor’s email</strong> (refer to section 3) – Where to submit)




<strong>            Subject</strong>          :           <strong>FT</strong> Assn<strong>1</strong> <strong>Resubmit_v1</strong> <strong>1234567</strong> <strong>JohnDoeAnderson</strong>


