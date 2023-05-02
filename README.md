Download Link: https://assignmentchef.com/product/solved-cnt4714-project4-sneakyknights
<br>
This problem is similar to SneakyQueens, but the solution requires a bit of a twist that will push you to employ your knowledge of data structures in clever ways. It has more restrictive runtime and space complexity requirements, as well: Your program needs to have an average-case / expected runtime complexity that does not exceed O(<em>nk</em>), and a worst-case space complexity that does not exceed O(<em>nk</em>) (where <em>n</em> is the number of knights and <em>k</em> is the max length of any of their coordinate strings).

The assignment also has a different board size restriction: The maximum board size is now Integer.MAX_VALUE × Integer.MAX_VALUE.

Please feel free to seek out help in office hours if you’re lost, and remember that it’s okay to have conceptual discussions with other students about this problem, as long as you’re not sharing code (or pseudocode, which is practically the same thing). Just keep in mind that you’ll benefit more from this problem if you struggle with it a bit before discussing it with anyone else.

<h1>Deliverables</h1>

SneakyKnights.java

<strong><em>Note!</em></strong> The capitalization and spelling of your filename matter!

<strong><em>Note!</em></strong> Code must be tested on Eustis, but submitted via Webcourses.

<h1>1.    Problem Statement</h1>

You will be given a list of coordinate strings for knights on an arbitrarily large square chess board, and you need to determine whether any of the knights can attack one another in the given configuration.

In the game of chess, knights can move two spaces vertically (up or down) and one space to the side (left or right), or they can move two spaces horizontally (left or right) and one space vertically (up or down). For example, the knight on the following board (denoted with a letter ‘N’, since the letter ‘K’ is traditionally reserved for the king in formal chess notation systems) can move to any position marked with an asterisk (‘*’), and no other positions:

<strong><em>Figure 1:</em></strong><em> The knight at position d3 can move to any square marked with an asterisk.</em>

Thus, on the following board, none of the knights (denoted with the letter ‘N’) can attack one another:

<strong><em>Figure 2:</em></strong><em> A 4×4 board in which none of the knights can attack one another.</em>

In contrast, on the following board, the knights at <em>c6</em> and <em>d8</em> can attack one another, as can the knights at c<em>6</em> and <em>d4</em>:

<strong><em>Figure 3:</em></strong><em> An 8×8 board in which some of the knights can attack one another.</em>

<ol start="2">

 <li><strong> Coordinate System</strong></li>

</ol>

This program uses the same coordinate system given in the SneakyQueens assignment.

<h1>3.     Runtime and Space Requirements</h1>

In order to pass all test cases, the average-case / expected runtime of your solution cannot exceed O(<em>nk</em>), and the worst-case space complexity cannot exceed O(<em>nk</em>) (where <em>n</em> is the number of coordinate strings to be processed and <em>k</em> is the maximum length of any of those coordinate strings). So, you can only process the full length of each coordinate string some small, constant number of times.

<em>Continued on the following page…</em>

<h1>4.     Method and Class Requirements</h1>

Implement the following methods in a class named <em>SneakyKnights</em>. Please note that they are all <strong><em>public </em></strong>and <strong><em>static</em></strong>. You may implement helper methods as you see fit.

<strong> public static boolean </strong> allTheKnightsAreSafe(ArrayList&lt;String&gt; coordinateStrings, <strong>int</strong> boardSize)

<strong>Description:</strong> Given an ArrayList of coordinate strings representing the locations of the knights on a <em>boardSize</em> × <em>boardSize</em> chess board, return <em>true</em> if none of the knights can attack one another. Otherwise, return <em>false</em>.

<strong>Parameter Restrictions:</strong> <em>boardSize</em> will be a positive integer less than or equal to <em>Integer.MAX_VALUE</em>. <em>boardSize </em>describes both the length and width of the square board. (So, if <em>boardSize</em> = 8, then we have an 8 × 8 board.) <em>coordinateStrings</em> will be non-null, and any strings within that ArrayList will follow the format described above for valid coordinates on a <em>boardSize</em> × <em>boardSize</em> board. Each coordinate string in the ArrayList is guaranteed to be unique; the same coordinate string will never appear in the list more than once.

<strong>Output:</strong> This method should <strong><u>not</u></strong> print anything to the screen. Printing stray characters to the screen (including newline characters) is a leading cause of test case failure.

<strong> public static double </strong>difficultyRating()

Return a double indicating how difficult you found this assignment on a scale of 1.0 (ridiculously easy) through 5.0 (insanely difficult).

<strong> public static double</strong> hoursSpent()

Return a realistic and reasonable estimate (greater than zero) of the number of hours you spent on this assignment.

<h1>5.      Style Restrictions (Same as in Program #1) (<em>Super Important!</em>)</h1>

Please conform as closely as possible to the style I use while coding in class. To encourage everyone to develop a commitment to writing consistent and readable code, the following restrictions will be strictly enforced:

 Capitalize the first letter of all class names. Use lowercase for the first letter of all method names.

 Any time you open a curly brace, that curly brace should start on a new line.

 Any time you open a new code block, indent all the code within that code block one level deeper than you were already indenting.

 Be consistent with the amount of indentation you’re using, and be consistent in using either spaces or tabs for indentation throughout your source file. If you’re using spaces for indentation, please use at least

two spaces for each new level of indentation, because trying to read code that uses just a single space for each level of indentation is downright painful.

 Please avoid block-style comments: /*<em> comment </em>*/

 Instead, please use inline-style comments: //<em> comment</em>

 Always include a space after the “//” in your comments: “// <em>comment</em>” instead of “//<em>comment</em>”  The header comments introducing your source file (including the comment(s) with your name, course number, semester, NID, and so on), should always be placed <em><u>above</u></em> your import statements.

 Use end-of-line comments sparingly. Comments longer than three words should always be placed <em><u>above</u></em> the lines of code to which they refer. Furthermore, such comments should be indented to properly align with the code to which they refer. For example, if line 16 of your code is indented with two tabs, and line 15 contains a comment referring to line 16, then line 15 should also be intended with two tabs.

 Please do not write excessively long lines of code. Lines must be no longer than 100 characters wide.  Avoid excessive consecutive blank lines. In general, you should never have more than one or two consecutive blank lines.

 Please leave a space on both sides of any binary operators you use in your code (i.e., operators that take two operands). For example, use <em>(a + b) – c</em> instead of <em>(a+b)-c</em>. (The only place you do <em><u>not</u></em> have to follow this restriction is within the square brackets used to access an array index, as in: <em>array[i+j]</em>.)  When defining or calling a method, do not leave a space before its opening parenthesis. For example:

use <em>System.out.println(“Hi!”)</em> instead of <em>System.out.println (“Hi!”)</em>.

 Do leave a space before the opening parenthesis in an <em>if</em> statement or a loop. For example, use use <em>for (i = 0; i &lt; n; i++)</em> instead of <em>for(i = 0; i &lt; n; i++)</em>, and use <em>if (condition)</em> instead of <em>if(condition)</em> or <em>if( condition )</em>.

 Use meaningful variable names that convey the purpose of your variables. (The exceptions here are when using variables like <em>i</em>, <em>j</em>, and <em>k</em> for looping variables or <em>m</em> and <em>n</em> for the sizes of some inputs.)  Do not use <em>var</em> to declare variables.

<h1>6.       Compiling and Testing SneakyKnights on Eustis (and the <em>test-all.sh</em> Script!)</h1>

Recall that your code must compile, run, and produce precisely the correct output on Eustis in order to receive full credit. Here’s how to make that happen:

<ol>

 <li>To compile your program with one of my test cases:</li>

</ol>

javac SneakyKnights.java TestCase01.java

<ol start="2">

 <li>To run this test case and redirect your output to a text file:</li>

</ol>

java TestCase01 &gt; myoutput01.txt

<ol start="3">

 <li>To compare your program’s output against the sample output file I’ve provided for this test case:</li>

</ol>

diff myoutput01.txt sample_output/TestCase01-output.txt

If the contents of <em>myoutput01.txt</em> and <em>TestCase01-output.txt</em> are exactly the same, <em>diff</em> won’t print anything to the screen. It will just look like this:

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="87f4e2e6e9f4fdc7e2f2f4f3eef4">[email protected]</a>:~$ diff myoutput01.txt sample_output/TestCase01-output.txt <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="116274707f626b51746462657862">[email protected]</a>:~$ _

Otherwise, if the files differ, <em>diff</em> will spit out some information about the lines that aren’t the same.

<ol start="4">

 <li>I’ve also included a script, <em>test-all.sh</em>, that will compile and run all test cases for you. You can run it on Eustis by placing it in a directory with <em>java</em> and all the test case files and typing:</li>

</ol>

bash test-all.sh

<strong><em>Note!</em></strong> Because the last four test cases are very large, you might not be able to transfer them to Eustis without exceeding your disk quota there. You might have to run only the first five tests on Eustis. If you’re running these test cases on your own system, you’ll want to force the <em>test-all.sh</em> script to run all test cases (including the very large ones) by typing:

bash test-all.sh –include-the-really-big-test-cases