CSE 141: Introduction to Computer Architecture
=====================================

<div class="row flex-nowrap no-gutters">
<div class="col-lg-2 col-xs-4">
<img src="/images/research/m3-finger-square.jpg" alt="M3 sensor on a finger" />
</div>
<div class="col-lg-2 col-xs-4">
<img src="/images/research/vlc-centers.png" alt="Luxapose image processing pipeline" />
</div>
<div class="col-lg-2 col-xs-4">
<img src="/images/research/signpost-closeup-square.jpg" alt="Signpost platform deployed outside" />
</div>
<div class="col-lg-2 d-none d-sm-block">
<img src="/images/research/tottag-overlay.png" alt="TotTag ranging platform" />
</div>
<div class="col-lg-2 d-none d-sm-block">
<img src="/images/research/opo-tie.png" alt="Opo interaction tracker clipped to a tie" />
</div>
<div class="col-lg-2 d-none d-sm-block">
<img src="/images/research/powerblade.jpg" alt="Powerblade power meter on a plug" />
</div>
</div>

## Section A00 – Fall 2020
Meets M/W/F from 10:00 to 10:50 US/Pacific, online.<br/>
[Pat Pannuto](https://patpannuto.com) is the instructor and their office is [CSE 3202](https://cse.ucsd.edu/about/floormaps) (right in the corner).

Pat's office hours are M/W from 14:00 to 14:50 US/Pacific, online.<br/>
Other times available by appointment.

---

## Overview

The course covers the basics of modern processor design and operation.
Topics include instruction set architectures, computer system performance, machine organization, pipelining, branch prediction, memory-hierarchy design, and an introduction to multiprocessor considerations (and possibly security considerations as well).

This course is designed to run alongside CSE 141L.
We expect that you are enrolled in both.

### Prerequisites

CSE 140 and 140L are required prerequisites for this course.
We expect that you are comfortable with the basics of digital logic, including the fundamentals of logic timing and how 1's and 0's can be used for higher-level operations like addition.

We further expect a basic familiarity with C or C-like code, i.e. you should be comfortable understanding what the following code does:

```c
int twoDarray[256][256];
int sum = 0;

for (int i=0; i<256; i++) {
  for (int j=0; j<256; j++) {
    sum += twoDarray[i][j];
  }
}

printf("%d\n", sum);
```

---

## Syllabus

_DISCLAIMER: Due to our unusual circumstances, the details in this syllabus may change (e.g. schedule, grading policy, assignments, etc.). We will update this syllabus in the event of changes as the course progresses._

### Instructors

 - <a href="https://patpannuto.com">Pat Pannuto</a> (Section A00)
 - <a href="https://cseweb.ucsd.edu/~tullsen/">Dean Tullsen</a> (Section B00)

#### TAs

 - Kazem Taram - mtaram@eng.ucsd.edu
 - Nitish Kulshrestha - nikulshr@eng.ucsd.edu
 - Shanti Modi - shmodi@eng.ucsd.edu
 - Sumiran Shubhi - sshubhi@eng.ucsd.edu


### Grading

A quick reminder: Effective learning comes from **active engagement** and **re-enforcement**.
Activities, assignments, and grading are designed to help with this.

_You get out of class what you put into it._

#### 10%: Participation (Mini-Quizzes)

During lectures, we will have interactive question and answer segments (zoom polls).
These are opportunities to check your understanding and for us to go back and help explain concepts more thoroughly that may be confusing folks.
To accommodate asynchronous participants, these in-lecture polls will not be graded for correctness or attendance.

At the end of each week, we will collect all of the poll questions and release a mini-quiz on canvas.
The quiz must be completed by midnight (campus time) the following Tuesday.

_These quizzes are primarily for you, to help you stay on track and to check your own understanding._
Therefore, we **will not grade them for correctness**.
If you complete the quiz, you will earn full points for that week.
However, if your raw score on a quiz is low, _come to discussion sections or office hours and get help!_

> ##### Mini-Quiz Late Policy
>
> As the purpose of these mini-quizzes is to help you keep up with class, there will be no extensions or late submissions.
> However, we also recognize that life does happen, especially now.
> We will release (at least two) bonus quizzes during the term that can be used to make-up a missed mini-quiz.
> The current thinking is one before the midterm and one before the final, which you can use to help check your understanding, but this is highly subject to change.
>
> Make-up quizzes will allow for up-to full participation. They will not count for extra credit.

#### 15%: Homework

These are longer form assignments, assigned roughly every other week.

You are welcome discuss homework problems with other students or in groups, however, you must complete your final writeup alone.

#### 30%: Midterm

This course will have one midterm exam.

We recognize that students may be attending class from all around the world. For this reason, we will offer the midterm exam as a <strong>ninety minute exam to be completed any time in a twelve hour window</strong>.

#### 45%: Final Exam

The registrar has assigned: `CSE 141 A00 and B00: Common Final, 12/12/20, 11:30 AM - 2:29 PM` as the final exam time slot for this course.

However, we recognize that students may be attending class from all around the world. For this reason, we will offer the final exam as a <strong>two hour exam to be completed any time in a twelve hour window</strong>.

> We recognize that Saturday can be a challenging day for some people to block off time, however, we also need to respect that folks have exams in other courses and the purpose of a harmonized exam schedule is to not conflict with those exams.
>
> If you absolutely cannot make Saturday work, please contact Pat directly **before Thanksgiving** to arrange an alternative.

The final exam will be cumulative over all of the course content.

#### Academic Integrity


### Schedule

Reminder: You will get more out of lecture if you have completed the pre-class reading.
We try to be clear about what is okay to skim and what will be helpful to read deeply.

Bonus materials are for those interested in learning more about a topic.
The are **not** required in any way and their content will **not** be tested in quizzes, homework, or exams.

<table class="table table-bordered table-hover">
  <tr class="table-primary">
    <th>Date</th>
    <th>Topic</th>
    <th>Pre-Class Assignment</th>
    <th>Bonus Material</th>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 0: Welcome!</td>
  </tr>
  <tr>
    <td>Oct&nbsp;2</td>
    <td><a href="2020-10-02-cse141-intro.pptx">Introduction and Motivation</a></td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 1: Instruction Set Architectures</td>
  </tr>
  <tr>
    <td>Oct&nbsp;5</td>
    <td>What computing looks like; intro to instructions</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;7</td>
    <td>ISA design and memory</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;9</td>
    <td>Control flow; RISC vs CISC</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 2: Quantifying Performance</td>
  </tr>
  <tr>
    <td>Oct&nbsp;12</td>
    <td colspan="3"><i>Indigenous Peoples' Day</i></td>
  </tr>
  <tr>
    <td>Oct&nbsp;14</td>
    <td>Defining performance, time</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;16</td>
    <td>Improving performance, Amdahl's law</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 3: The Single-Cycle Computer, Pieces and Parts</td>
  </tr>
  <tr>
    <td>Oct&nbsp;19</td>
    <td>Introducing Functional Units and a basic ALU</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;21</td>
    <td>Architectural considerations in ALU design</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;23</td>
    <td>RTL</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 4: The Single-Cycle Computer, Putting it Together</td>
  </tr>
  <tr>
    <td>Oct&nbsp;26</td>
    <td>Datapaths</td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;28</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Oct&nbsp;30</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 5: Pipelining</td>
  </tr>
  <tr>
    <td>Nov&nbsp;2</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;3</td>
    <td colspan="2"><i>Election Day</i></td>
  </tr>
  <tr>
    <td>Nov&nbsp;4</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;6</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 6: Hazards</td>
  </tr>
  <tr>
    <td>Nov&nbsp;9</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;11</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;13</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 7: Advanced Pipelining</td>
  </tr>
  <tr>
    <td>Nov&nbsp;16</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;18</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;20</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 8: Memory</td>
  </tr>
  <tr>
    <td>Nov&nbsp;16</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;18</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Nov&nbsp;3</td>
    <td colspan="2"><i>Thanksgiving Holiday</i></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 9: Virtual Memory</td>
  </tr>
  <tr>
    <td>Nov&nbsp;30</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Dec&nbsp;2</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Dec&nbsp;4</td>
    <td></td>
    <td></td>
  </tr>

  <tr class="table-info">
    <td colspan="4">Week 10: Multiprocessing</td>
  </tr>
  <tr>
    <td>Dec&nbsp;7</td>
    <td></a></td>
    <td></td>
  </tr>
  <tr>
    <td>Dec&nbsp;9</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Dec&nbsp;11</td>
    <td>Final Exam Review</td>
    <td></td>
  </tr>

  <!-- CSE 141 A00 and B00: Common Final, 12/12/20, 11:30 AM - 2:29 PM -->
  <tr class="table-warning">
    <td colspan="4"><strong>Final Exam: December 12</strong></td>
  </tr>


</table>

