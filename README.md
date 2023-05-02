Download Link: https://assignmentchef.com/product/solved-computer-graphics-assignment-1-basic-opengl-viewer-drawing-a-hierarchical-model
<br>
<strong>Computer Graphics Assignment 1: Basic OpenGL viewer &amp; drawing a hierarchical model </strong>

<ul>

 <li>Only accept answers submitted via git push to this course project for you at <a href="https://hconnect.hanyang.ac.kr/">https://hconnect.hanyang.ac.kr</a> (&lt;Year&gt;_&lt;Course no.&gt;_&lt;Class code&gt;/&lt;Year&gt;_&lt;Course</li>

</ul>

no.&gt;_&lt;Student ID&gt;.git).

<ul>

 <li>Place your files under the directory structure <strong>&lt;Assignment name&gt;/&lt;your files&gt;</strong> just like</li>

</ul>

the following example.

<table width="234">

 <tbody>

  <tr>

   <td width="234">+ 2020_ITE0000_2019000001+ ClassAssignment1/–  main.py–  report.docx</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>The submission time is determined not when the commit is made but when the git push</li>

</ul>

is made.




<ol>

 <li>Implement a basic OpenGL viewer and show an animation of a hierarchical model using the viewer. This viewer will also be used in future class assignments.

  <ol>

   <li>You have to implement all requirements in a single program. This assignment DOES NOT require each requirement to be a separate program</li>

   <li>The window size doesn’t need to be (480, 480). Use the larger window that is enough to</li>

  </ol></li>

</ol>

see the details of the viewer.




<ol start="2">

 <li><strong>Requirements </strong>

  <ol>

   <li><strong>Manipulate the camera with mouse movement (50 pts)</strong>

    <ol>

     <li>Refer the camera manipulation of Blender software.

      <ol>

       <li><a href="https://www.blender.org/download/">https://www.blender.org/download/</a></li>

      </ol></li>

     <li>The camera of your program should initially look at a target point, similar to that of Blender.

      <ol>

       <li>Initialize the target point to the origin (0, 0, 0)</li>

       <li></li>

      </ol></li>

    </ol></li>

  </ol></li>

</ol>

iii.       Provide the following three camera control operations.

<ol>

 <li><strong>Orbit</strong>: Rotate the camera around the target point by changing azimuth / elevation angles. (MMB (mouse middle button) in Blender)<strong> (15 pts)</strong>

  <ol>

   <li>Do not rotate the camera about a vector from the camera to the target point.</li>

  </ol></li>

 <li><strong>Panning</strong>: Move both the target point and camera in left, right, up and down direction of the camera (Shift-MMB in Blender) <strong>(15 pts)</strong>

  <ol>

   <li>More specifically, translate both the target point and camera along u axis (left &amp; right) and v axis (up &amp; down) of the camera frame</li>

  </ol></li>

 <li><strong>Zooming</strong>: Move the camera forward toward the target point (zoom in) and backward away from the target point (zoom out) (Ctrl-MMB in Blender) <strong>(15 pts)</strong> A. More specifically, translate the camera along w axis of the camera frame</li>

 <li></li>

 <li>You MUST use the following mouse movement:

  <ol>

   <li><strong>Orbit: Click </strong><strong>mouse left button &amp; drag</strong></li>

   <li><strong>Panning: Click </strong><strong>mouse right button &amp; drag</strong></li>

  </ol></li>

</ol>

<h1>C.      Zooming: Rotate mouse wheel</h1>

<ol>

 <li><strong>Using above mouse movements is essential for scoring your assignment, so if you use any other set of mouse movement or keyboard shortcuts </strong></li>

</ol>

<strong>for Orbit / Panning / Zooming, </strong><strong>you won’t get any score </strong><strong>for them. </strong>

<ol>

 <li>Use perspective projection</li>

 <li>Draw <strong>a rectangular grid with lines (not polygons) on xz plane</strong> as a reference ground plane (similar to Blender). Choose number of rows and columns, size as you want. <strong>(5 pts)</strong></li>

</ol>




<ol>

 <li><strong>Create an animating hierarchical model using OpenGL matrix stacks (40 pts).</strong></li>

 <li>The model should consist of <strong>3D primitives</strong> such as boxes and spheres,</li>

 <li>You can use drawCube() and drawSphere() in the last page, or your own drawing</li>

</ol>

functions (which should use only numpy, opengl, glfw).

<ul>

 <li><strong>DO NOT use glut or glu functions to draw 3D primitives</strong> (e.g., glutSoildBox(), gluSphere(),…) because they generate runtime crashes on some systems (maybe</li>

</ul>

problems of some python bindings, but don’t use them anyway). iv.         Because we’ve not covered shading yet, just draw your model in <strong>wireframe mode</strong> by calling the following function at the beginning of your render function:

<ol>

 <li>glPolygonMode( GL_FRONT_AND_BACK, GL_LINE ) # call this at the beginning of</li>

</ol>

your render function

<ol start="2">

 <li>You can change the color of your wireframe primitives using glColor*().</li>

</ol>

<ol>

 <li><strong>You should use OpenGL matrix stack</strong> to draw and animate your hierarchical model.</li>

 <li>The model should have a<strong> hierarchy of at least 3 levels</strong> <strong>(20 pts)</strong>.

  <ol>

   <li>For example, the following model has a hierarchy of 4 levels.</li>

   <li></li>

  </ol></li>

</ol>

vii.       <strong>Animate the model</strong> to show the hierarchical structure <strong>(20 pts)</strong>.

<ol>

 <li><strong>Make all child body parts move relative to their parent body part. </strong>

  <ol>

   <li>In the above example, part 2, 3, 4, 5, 6 should move relative to part 1, part 7 should move relative to part 2, part 11 should move relative to part 7, … and</li>

  </ol></li>

</ol>

so on.

<ol>

 <li><strong>If any of the child bodies does not move relative to its parent, you will </strong></li>

</ol>

<strong>get -10 pts. </strong>

<ol start="2">

 <li>You can make any hierarchical system freely. Be creative.</li>

 <li>Eg) a hand with fingers bending</li>

 <li>Eg) a runner with arms and legs swing</li>

 <li>The model should be <strong>automatically animated without any mouse or keyboard </strong></li>

</ol>

<strong>inputs. </strong>




<ol start="3">

 <li><strong>Report (10 pts) </strong>

  <ol>

   <li>Submit a report of <strong>at most 2 pages</strong> in docx file format (MS Word). Do not exceed the</li>

  </ol></li>

</ol>

limit.

<ol>

 <li>The report should include:

  <ol>

   <li>Which requirements you implemented (5 pts) ii. A few screenshot images of your program (5 pts)</li>

  </ol></li>

 <li>You do not need to try to write a long report. Just write down the required information.</li>

</ol>

Use either English or Korean.

<strong> </strong>

<ol start="4">

 <li><strong>Runtime Environment </strong>

  <ol start="3">

   <li><strong>Your program should be able to run on systems only with Python 3.7 or later, NumPy, </strong></li>

  </ol></li>

</ol>

<strong>PyOpenGL, glfw. Do not use any other additional python modules. </strong>

<ol>

 <li>Only <strong>glfw</strong> is allowed for event processing and window &amp; OpenGL context management. <strong>Do not use glut functions for this purpose.</strong></li>

 <li><strong>If your program does not meet this requirement, it will not run on TA’s computer </strong><strong>so </strong></li>

</ol>

<strong>you will not get any score for this assignment </strong><strong>(except report). </strong>

<strong> </strong>

<ol start="5">

 <li><strong>What you have to submit: </strong>

  <ol>

   <li><strong>.py files</strong>

    <ol>

     <li>You can use multiple .py files for this assignment. In this case, explain how to run the</li>

    </ol></li>

  </ol></li>

</ol>

program in the report.

<ol>

 <li><strong>.docx report file</strong></li>

</ol>




<ol start="6">

 <li>drawCube() and drawSphere() code:</li>

</ol>

<table width="548">

 <tbody>

  <tr>

   <td width="548"># draw a cube of side 2, centered at the origin.<strong>def</strong> drawCube<strong>():</strong>glBegin<strong>(</strong>GL_QUADS<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong> glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong> glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong></td>

  </tr>

  <tr>

   <td width="548">     glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong>      glVertex3f<strong>(-</strong>1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong>     glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong>      glVertex3f<strong>(-</strong>1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,-</strong>1.0<strong>)</strong>      glVertex3f<strong>(</strong> 1.0<strong>,</strong> 1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,</strong> 1.0<strong>)</strong>     glVertex3f<strong>(</strong> 1.0<strong>,-</strong>1.0<strong>,-</strong>1.0<strong>)</strong>     glEnd<strong>()</strong>  # draw a sphere of radius 1, centered at the origin.# numLats: number of latitude segments # numLongs: number of longitude segments <strong>def</strong> drawSphere<strong>(</strong>numLats<strong>=</strong>12<strong>,</strong> numLongs<strong>=</strong>12<strong>):</strong>     <strong>for</strong> i <strong>in</strong> range<strong>(</strong>0<strong>,</strong> numLats <strong>+</strong> 1<strong>):</strong>lat0 <strong>=</strong> np<strong>.</strong>pi <strong>*</strong> <strong>(-</strong>0.5 <strong>+</strong> float<strong>(</strong>float<strong>(</strong>i <strong>–</strong> 1<strong>)</strong> <strong>/</strong> float<strong>(</strong>numLats<strong>)))</strong>         z0 <strong>=</strong> np<strong>.</strong>sin<strong>(</strong>lat0<strong>)</strong>         zr0 <strong>=</strong> np<strong>.</strong>cos<strong>(</strong>lat0<strong>)</strong> lat1 <strong>=</strong> np<strong>.</strong>pi <strong>*</strong> <strong>(-</strong>0.5 <strong>+</strong> float<strong>(</strong>float<strong>(</strong>i<strong>)</strong> <strong>/</strong> float<strong>(</strong>numLats<strong>)))</strong>         z1 <strong>=</strong> np<strong>.</strong>sin<strong>(</strong>lat1<strong>)</strong>         zr1 <strong>=</strong> np<strong>.</strong>cos<strong>(</strong>lat1<strong>)</strong> # Use Quad strips to draw the sphere         glBegin<strong>(</strong>GL_QUAD_STRIP<strong>)</strong><strong>for</strong> j <strong>in</strong> range<strong>(</strong>0<strong>,</strong> numLongs <strong>+</strong> 1<strong>):</strong>lng <strong>=</strong> 2 <strong>*</strong> np<strong>.</strong>pi <strong>*</strong> float<strong>(</strong>float<strong>(</strong>j <strong>–</strong> 1<strong>)</strong> <strong>/</strong> float<strong>(</strong>numLongs<strong>))</strong>             x <strong>=</strong> np<strong>.</strong>cos<strong>(</strong>lng<strong>)</strong>             y <strong>=</strong> np<strong>.</strong>sin<strong>(</strong>lng<strong>)</strong>             glVertex3f<strong>(</strong>x <strong>*</strong> zr0<strong>,</strong> y <strong>*</strong> zr0<strong>,</strong> z0<strong>)</strong>             glVertex3f<strong>(</strong>x <strong>*</strong> zr1<strong>,</strong> y <strong>*</strong> zr1<strong>,</strong> z1<strong>)</strong> glEnd<strong>()</strong>  </td>

  </tr>

 </tbody>

</table>


