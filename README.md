Download Link: https://assignmentchef.com/product/solved-cpsc-223n-assignment-4
<br>
<strong> </strong>

<strong>Ricochet Ball</strong>

<strong>Background</strong>

Think of your graphic area as the top of a billiard table.  When the cue ball hits the edge of the table it ricochets off the edge and continues traveling in another direction.  In a real billiards game friction will make the ball eventually stop moving or perhaps the ball falls into a pocket, and then it has obviously stopped moving.  In this assignment 4 we assume there are no side pockets and no friction.  Here the ball keeps moving forever at the same constant speed: well, actually it moves until you click on the new button or the exit button.




<ol start="4">

 <li><strong>Basic requirements</strong></li>

</ol>

Make a user interface similar to the diagram in this document.  This interface will have a small header panel at the top, a large graphic panel in the middle, and a medium size control panel at the bottom.  When the interface first appears there are no objects in view.  The plane background of the graphical area is the only thing visible.

<strong>Description of the components of the user interface</strong>




<ol>

 <li>At the top there is a thin rectangle that holds the title and your name. You choose a height for this rectangle.</li>

</ol>




<ol start="2">

 <li>In the middle is a large rectangle which represents the top of the billiard table. You choose its height.  Don’t make it small.  A height of 800 or more is ok.</li>

</ol>




<ol start="3">

 <li>The bottom of the frame is a rectangular area where the controls are placed. You pick a good height for the control panel.</li>

</ol>




<ol start="4">

 <li>When a user clicks on “New” all the input fields are set to blanks and a small red ball with a radius equal to 5 pixels appears in the center of the green graphical area.</li>

</ol>




<ol start="5">

 <li>In the speed box the user enters the motion speed of the ball. This number is often called the “linear speed” of the animated object.  Motion speed is measured in pixels/second.</li>

</ol>




<ol start="6">

 <li>The direction input box is expecting to receive a number of degrees. The ball will initially travel in the direction of the inputted number.  The inputted number should be stored in a variable of type double.</li>

</ol>







7.When the user clicks on the start button then the two input numbers are read: speed and direction.  Using those two numbers the ball starts moving in the given direction.

8.When the ball reaches one of the four walls it bounces off the wall and continues. We say that the ball ricochets off of the wall.  Then the ball continues in straight line in a new direction until it ricochets off of another wall.  This ricochet action continues until the user clicks on “Quit” or clicks on “New”.




<ol start="9">

 <li>If the user clicks on Quit then the frame closes. If the user clicks on New then ball stops and all the input fields become blank.</li>

</ol>




<ol start="11">

 <li>While the ball is moving the coordinates of the ball are displayed in the X and Y output fields. Remember to output the coordinates of the center of the ball – not the coordinates of the upper left corner of the ball.</li>

</ol>

<strong>Math for computer graphics</strong>




When a user inputs a direction such 58.5 degrees the program has to make several calculations like these.




<ol>

 <li>Convert the input degrees to radians. We’ll call the radian number Θ.</li>

</ol>




<ol>

 <li>Let S be the linear speed of the ball in pix/sec.  This is an input from the user.</li>

</ol>

Let  M be the rate of the motion clock in tic/sec.  This is set by the programmer.




<ol>

 <li>Compute C = S/M, which is called speed of ball measured in pix/tic.</li>

</ol>




<ol>

 <li>Compute delta x and delta y using right angle trigonometry:</li>

</ol>




deltax = C*cos(Θ)




deltay = C*sin(Θ)




Each time the motion clock tics the amount deltax is added to the x coordinate of the ball, and deltay is added to the y coordinate of the ball.

In the two equations above “direction” is the angle in radians in which the ball is moving relative to an invisible x-axis.

<table>

 <tbody>

  <tr>

   <td width="34">

    <table width="100%">

     <tbody>

      <tr>

       <td>x-axis</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




























<strong> </strong>


