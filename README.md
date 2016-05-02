# 3050FinalProject
Final Project for CS 3050 at UM-Columbia

CS 3050: Group Project
April 12, 2016
DUE: 05/05/2016
Topic: Optimal trading strategies
This is the nal project of the course. The project can be done alone or in a group of at most 3 people. The project
contributes to 12% of your total grade. You should send an email to Eric, Elizabeth and myself by April 21 with the
subject \CS3050 project" indicating whether you are choosing to do the project alone or in a group. If you choose to do
the project in a group, please include the name of your teammates in the project (one email per team is ne).
Description
The purpose of this project is to build upon your algorithm design and general programming skills. Algorithms play
an important role in trading strategies at investment rms. In this project, you will model and implement a relatively
\simple" trading strategy. Imagine you are working at an investment rm, say X, and are responsible for trading a stock
for a company, say Y. The company has an excellent predictive modeling team and can predict the stocks for the company
Y for the next n days with reasonable accuracy. Let the predicted prices be p1; p2; : : : ; pn: So p1 is the predicted stock
price at day 1; p2 is the predicted stock price at day 2, and so on. Your goal is to buy and sell stocks of Y in order to
maximize prots. For this you shall be using r-trades strategy, described below.
An r-trades strategy, for an integer r, is a sequence of 2k integers :
Strat = b1; s1; b2; s2; : : : ; bk; sk where k  r:
1. The sequence Strat means that you will make k-trades as follows.
 You will buy Y 's stock at day b1
 You will sell Y 's stock at day s1
 You will buy Y 's stock again at day b2
 You will sell Y 's stock again at day s2
 : : :
2. The sequence Strat is strictly increasing, i.e., b1 < s1 < b2 < s2 < : : : bk < sk:
3. The numbers in Strat are at least 1 and atmost n:
Your task is to write a program that given n; r and p1; : : : ; pn; outputs the r-trades strategy that maximizes the prot,
i.e., maximizes the quantity
Prot(Strat) = (ps1 􀀀 pb1 ) + (ps2 􀀀 pb2 ) + : : : (psk 􀀀 pbk ):
For example, suppose n = 6 and the predicted prices for the next 6 days are:
p1 = 1; p2 = 3; p3 = 4; p4 = 6; p5 = 2; p6 = 10:
If r = 1 then the optimal strategy is b1 = 1; s1 = 6; i.e, buy at day 1 and sell at day 6: If r = 2 then the optimal
strategy is b1 = 1; s1 = 4; b2 = 5; s2 = 6; i.e, buy at day 1, sell at day 4; buy at day 5 and sell at day 6: If r = 3 then the
optimal strategy is again b1 = 1; s1 = 4; b2 = 5; s2 = 6:
1
Constraints
The constraints of the program include:
1. The program can be written in C or C++. If you want to use a dierent language, please check with us.
2. Either use a netbeans project or use a Makele to compile and run the program.
3. Include a README le to tell the TA's how to run your program.
4. You should include a project report in which you detail your eorts, the algorithms used (along with their complexity)
and the contribution of your team members. We shall use this report primarily to give you partial credit if your
program does not work.
5. A moderate amount of error checking and resource management is required. Your application should check that each
line from the input le is properly formatted, that the le is successfully opened, the le is successfully closed upon
reading of the le and that all allocated space is de-allocated at the exit. If the input is not properly formatted, you
should report the error on stdout and exit the program.
6. You may use standard input/output libraries, arrays, vectors, stacks, heaps, lists and queues. If using other libraries,
please please check with us.
7. A moderate amount of formatting and documentation is required. Comments should be descriptive and used to
illustrate the purpose and inner workings of an algorithm or function; they should not be used to annotate each line
or self-evident logic.
8. For substantial credit, your program should work for at least the cases when r = 1; r = 2 and r = 3:
Input
Your program should take at least three arguments on the command line. The rst argument is the number of days n; the
second is the parameter r and the third argument in an input le which contains the list of predicted prices p1; p2; : : : pn:
Each line of an input le consists of a non-negative integer followed by a newline character. Each integer is a string of
digits. The ith line of this le is pi, the predicted price of stock at day i: A sample input le is included on Blackboard.
Output
Each line printed to standard output should consist of a non-negative integer followed by a newline character. The rst
line of the output is value of b1; the second line of the le is s1, the third line of the le is b2; the fourth line of the le
is s2 and so on. A sample output le is included on Blackboard which includes the optimal strategy for the prices in the
sample input le for r = 3:
Due Dates
 April 21 is the date that you must inform us about the composition of your team.
 During the week of April 25-April 29; please try to meet one of the TAs or myself during oce hours and show the
progress of the project. If the times do not work, please send us an email and we will try to nd additional time to
check the progress.
 The nal submission is due May 5 at 11:59:59 pm.
Submission
You should place all your submission material into a folder named as follows: pawprint1 pawprint2 pawprint3 project.
Where the pawprint1 pawprint2 pawprint3 is the list of you and your group member pawprints.
You will submit one le, a compressed directory containing all the source code and appropriate Makele(s). The naming
convention should be: pawprint1 pawprint2 pawprint3 project.tgz or pawprint1 pawprint2 pawprint3 project.zip.
2
Grading
There are 120 points possible for this assignment. The grade breakdown is as follows:
 15 points for README, error checking and resource management.
 15 points for general programming style and adherence to the constraints.
 20 points for the project report.
 10 points for correctly inputting the predicted prices.
 60 points for correctly outputting the strategy.
3
