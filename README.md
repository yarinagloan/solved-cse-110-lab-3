Download Link: https://assignmentchef.com/product/solved-cse-110-lab-3
<br>
<h1>Lab Topics</h1>




<ul>

 <li>Familiarization with basic data types.</li>

 <li>Using the Scanner Class with input validation.</li>

 <li>Understanding order of operations.</li>

 <li>Getting familiar with the basic flow control in Java.</li>

</ul>

<h1>Use the following Coding Guidelines</h1>




<ul>

 <li>When declaring a variable, you usually want to initialize it.</li>

 <li>Remember you cannot initialize a number with a string.</li>

 <li>Remember variable names are case sensitive.</li>

 <li>Use tabs or spaces to indent code within blocks (code surrounded by braces). This includes classes, methods, and code associated with ifs, switches and loops.</li>

 <li>Be consistent with the number of spaces or tabs that you use to indent.</li>

 <li>Use white space to make your program more readable.</li>

 <li>Use comments after the ending brace of classes, methods, and blocks to identify to which block it belongs.</li>

</ul>

<h1>Problem Description: Final Weighted Total Calculator</h1>




Please design a program which takes 3 user inputs as homework grade, midterm exam grade, and final exam grade. Then use the following formula to calculate the weighted total:




<em>Total<sub>weighted </sub></em>= (<em>Exam<sub>final</sub></em> / 200 × 50) + (<em>Exam<sub>midterm </sub></em>× 0.25) + (<em>Homework </em>× 0.25)




If the weighted total is greater or equal to 50 (&gt;=50), show <em>“Student PASSED the class”</em>​   ​. Otherwise, show ​<em>“Student FAILED the class”</em>​.




Your program have to validate the input values. A homework grade and midterm exam score should be in the range [0, 100]. The final exam grade should be in the range [0, 200]. If an input is invalid, you have to let the user retry immediately until it is a valid input.




<strong>Note: To get full marks, you must use only one loop. </strong>

<strong>           </strong>

<h1>Sample Output</h1>




<strong><u>Sample Run 1 (The user passed the class):</u> </strong>




Enter your HOMEWORK grade: ​<strong>100 </strong>




Enter your MIDTERM EXAM grade: ​<strong>76 </strong>




Enter your FINAL EXAM grade: ​<strong>80</strong>




[INFO] Student’s Weighted Total is 64.00




[INFO] Student PASSED the class




<strong><u>Sample Run 2 (The user failed the class):</u> </strong>




Enter your HOMEWORK grade: ​<strong>30 </strong>




Enter your MIDTERM EXAM grade: ​<strong>40</strong>




Enter your FINAL EXAM grade: ​<strong>35</strong>




[INFO] Student’s Weighted Total is 26.25




[INFO] Student FAILED the class







<strong><u>Sample Run 3 (Input validation, minimum requirement)</u> </strong>




Enter your HOMEWORK grade: ​<strong>100</strong>




Enter your MIDTERM EXAM grade: ​<strong>76</strong>




Enter your FINAL EXAM grade: ​<strong>8000</strong>

[ERR] Invalid input. A final grade should be in [0, 200].




Enter your FINAL EXAM grade: ​<strong>40</strong>




[INFO] Student’s Weighted Total is 54.00




[INFO] Student PASSED the class




<strong>             </strong>

<h1>A Challenge (not required, not part of the lab grade)<u>  </u></h1>




Limit the number of chances that the user can retry to 3. It means when one input is invalid, the user will have 3 extra times to retry. If a user has retried three times consecutively and fails, the program loop should terminate immediately and show the error message: ​<em>“You have retried 3 times, Please restart your program.”</em>​ In total, a user can input four times in a sequence with the first three inputs invalid. The counter will be reset to 0 when an input is correct. Your program’s output messages should change according to the user input states.




<strong><u>Sample Run for Challengers</u></strong>




Enter your HOMEWORK grade:​<strong> 100</strong>




Enter your MIDTERM EXAM grade:​<strong> 76</strong>




Enter your FINAL EXAM grade: ​<strong>1000 </strong>

[ERR] Invalid input. A final grade should be in [0, 200].




Enter your FINAL EXAM grade (2 chances left): ​<strong>-1293</strong> [ERR] Invalid input. A final grade should be in [0, 200].




Enter your FINAL EXAM grade (1 chances left): ​<strong>8023</strong>

[ERR] Invalid input. A final grade should be in [0, 200].




Enter your FINAL EXAM grade (0 chances left): ​<strong>12342314</strong> [ERR] Invalid input. A final grade should be in [0, 200].




[ERR] You have retried 3 times. Please restart your program.




<strong> </strong>

<h1>Step 1: Get started with the header</h1>




Create a class called Lab3. Use the same setup for setting up your class and main method as you did in previous labs and assignments. Be sure to name your file Lab3.java.




At the beginning of each programming assignment you must have a comment block with the following information:







/*————————————————————- // AUTHOR: your name.

// FILENAME: title of the source file.

// SPECIFICATION: your own description of the program.

// FOR: CSE 110- Lab #3

// TIME SPENT: how long it took you to complete the assignment.

//———————————————————–*/




<h1>Step 2: Declare variables you need</h1>




<table width="624">

 <tbody>

  <tr>

   <td width="624">        ​// This scanner is prepared for you to get inputs​Scanner​ ​scanner​ = ​new​ ​Scanner​(​System​.​in​);​// Declare three variables for HW, midterm, and final exam grades         ​// –&gt;​// Declare a loop control variable i         ​// –&gt;</td>

  </tr>

 </tbody>

</table>




Since your program will ask the user for the homework score, midterm exam score, and final exam score. Please declare three double variables to save these input values.




In addition, you might need a variable to control your while loop. Please declare an integer i for this purpose.




You can declare extra variables if you think they are needed.

<strong>           </strong>

<h1>Step 3: Use a while loop with the right condition</h1>




​while​ (​/* Put in the condition involving i */​) {         }




We hope the program will restart automatically when the user give you an invalid input.

Intuitively, we should use a loop structure to make it restart if a certain condition is not correct. Please first make a while loop statement and one loop control variable i. Then design the loop condition you need. Refer the template file if you are not sure what to do.




Hint: It might be challenging to design such a condition sometimes. To help you think about what it should be, here is a simple logic we hope the program to follow:




<ol>

 <li>Inside this while loop, the program asks three inputs from the user.</li>

 <li>If any of the three inputs is not valid, the loop will restart and let the user input that number again (for example, if the midterm grade is invalid, let the user type the midterm grade again. Do NOT ask the user start from the homework grade.)</li>

 <li>The while loop will stop when all inputs are done and valid.</li>

</ol>

<h1>Step 4: Use if-else statements to control input flow</h1>




<table width="624">

 <tbody>

  <tr>

   <td width="624">            ​if​ (i == ​0​) {​// Ask the user for homework grade​// –&gt;                 // …             }</td>

  </tr>

 </tbody>

</table>




Inside the while loop, the program asks the user for the three grades. Since we are using only one while loop to do three inputs at the same time, we need a proper flow control to make the loop asks for the right input in different moments. To do so, please construct three if-else statements involving your loop variable i, specifically:




<ol>

 <li>if i is 0, asks for the homework grade</li>

 <li>if i is 1, asks for the midterm exam grade</li>

 <li>if i is 2, asks for the final exam grade</li>

</ol>

<strong>           </strong>

<h1>Step 5: Use if-else statements to validate the input values</h1>




<table width="624">

 <tbody>

  <tr>

   <td width="624">                ​// Do input validation​// –&gt;​if​ (​/* the HW grade is not valid */​) {​// Show the error message​// –&gt;} ​else​ {​// Update the loop variable​// –&gt;                 }</td>

  </tr>

 </tbody>

</table>




Following Step 4, inside each if-else statement the program asks for the user input. To ensure the user gives you a valid number, you have to design another if-else statement to validate the input. For your reference, the valid ranges are




<ol>

 <li>[0, 100] for a homework grade</li>

 <li>[0, 100] for a midterm exam grade</li>

 <li>[0, 200] for a final exam grade</li>

</ol>




Hint: You should update the loop control variable i when any of these input is valid, so as to make your program approach the terminal condition of the loop.

<strong>           </strong>

<h1>Step 6: Calculate the weighted total and show the value</h1>




double​ ​weighted_total​ = …;




After the while loop, please calculate the weighted total by the formula provided above. The result should be saved into another variable and showed in your console.

<h1>Step 7: Show the student passed or failed</h1>




​if​ (​/* … */​) {

​// Print “the student PASSED the class.”

} ​else​ {

​// Print “the student FAILED the class.”         }




Finally, according to the weighted total, the program determines whether the user passed the class or not. Please design another if-else statement to do so. The conditions are




<ol>

 <li>if the weighted total is greater than or equal to 50, show “[INFO] The student PASSED the class”</li>

 <li>Otherwise, show “[INFO] The student FAILED the class”.</li>

</ol>