<div align="center">

## Beginners C\+\+ \- Lesson 2: Variables, math and booleans


</div>

### Description

Learn how to do variables, math and booleans in C++! (from http://pa.pulze.com/)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the World Wide Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-world-wide-web.md)
**Level**          |Beginner
**User Rating**    |4.6 (46 globes from 10 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-world-wide-web-beginners-c-lesson-2-variables-math-and-booleans__3-418/archive/master.zip)





### Source Code


<h2>Beginners C++ - Lesson 2</h2>
<p><b style="FONT-WEIGHT: bold">Instructor</b>:&nbsp;&nbsp; Paul C. Benedict,
Jr. (<u><span style="COLOR: #0000ff">PCC PaulB</span></u>)</p>
<h2>Color coded text:</h2>
<p><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp; black&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
New things to Remember</b><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp;
blue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; C++
keywords (do, while)</b></span><br>
&nbsp;&nbsp;&nbsp; <span style="COLOR: #008800"><b style="FONT-WEIGHT: bold">green&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
C++ preprocessor directives (#include, #define)</b></span></p>
<p><br>
</p>
<h1><u><i>Section 2.1</i></u></h1>
<p>From last time, we learned how to declare numbers and do math with them. For
instance, lets declare an integer variable we call <i>x</i> and set it to five:</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.1.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 5;</span></p>
<p>This called <b style="FONT-WEIGHT: bold">initialization</b>! We call it
initialization because <i>x</i> was set to five when it was created (The <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">int</b></span>
means create an integer variable. It is not an abbrevation for initialization).
Now, if we left off the value (called the <b style="FONT-WEIGHT: bold">inital
value</b>), <i>x</i> would contain junk. What do we mean when we say it contains
junk? When <i>x</i> was <b style="FONT-WEIGHT: bold">allocated</b> (memory that
was set aside for <i>x</i>), whatever value that was in memory previously before
<i>x</i> is now the value of <i>x</i>. We call this value of <i>x</i> <b style="FONT-WEIGHT: bold">undefined</b>
because we did not define the value, and since the value is undefined, the
variable is <b style="FONT-WEIGHT: bold">uninitialized</b>. You cannot do
anything useful with the variable until it was initialized. You do not have to
initialize variables when you <b style="FONT-WEIGHT: bold">declare</b>
them.variable before using it.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.1.2</b></span><br>
Here you declare two variables, then assign them later.<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int y;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = 5;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; y = x * 3;</span></p>
<p>First <i>x</i> and <i>y</i> is declared (and has an undefined value because
it is uninitalized). Then <i>x</i> is initialized to the value five. They <i>y</i>
is initialized to the value of <i>x</i> times 3, which is fifteen.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.1.3</b></span><br>
What happened if we did this?<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x + 1;</span></p>
<p>What is the value of <i>x</i>? We don't know. <i>x</i> is whatever it was
plus one now. The value is completely meaningless to us. One of the most common <b style="FONT-WEIGHT: bold">bugs</b>
in programming is not initializing variables before you use it. (On a side note,
a bug is an &quot;unlisted feature&quot; in a program that makes the program not
work they way you want it - the last example shows this.).</p>
<p><br>
</p>
<h1><u><i>Section 2.2</i></u></h1>
<p>These are the current operators we know so far from our last lesson:<br>
&nbsp;&nbsp;&nbsp; Addition&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+<br>
&nbsp;&nbsp;&nbsp; Subtraction&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
-<br>
&nbsp;&nbsp;&nbsp; Multiplication&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
*<br>
&nbsp;&nbsp;&nbsp; Division&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
/<br>
&nbsp;&nbsp;&nbsp; Modular Division (Remainder)&nbsp;&nbsp;&nbsp;&nbsp; %</p>
<p>We are now going to learn some more operators to work with numbers:<br>
&nbsp;&nbsp;&nbsp; Increment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
++<br>
&nbsp;&nbsp;&nbsp; Decrement&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
--<br>
&nbsp;&nbsp;&nbsp; Addition Assignment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+=<br>
&nbsp;&nbsp;&nbsp; Subtraction Assignment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
-=<br>
&nbsp;&nbsp;&nbsp; Multiplication Assignment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
*=<br>
&nbsp;&nbsp;&nbsp; Division Assignment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
/=<br>
&nbsp;&nbsp;&nbsp; Remainder Assignment&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
%=</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.2.1</b></span><br>
The increment operator ++&nbsp; increments a variable by one.<br>
The decrement operator --&nbsp; decrements a variable by one.<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 10;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x++;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x + 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x--;</span></p>
<p>First <i>x</i> is initialized to the value ten.<br>
Then it is incremented to the value eleven.<br>
Next we add three to it.<br>
Then we decrement it.<br>
The final value for the variable <i>x</i> is now thirteen.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.2.2</b></span><br>
Now, with the += operator we can simply this even more:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 10;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x++;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x += 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x--;</span></p>
<p>Wow! Look at that!<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x += 3;</span><br>
Is an equivalent shorthand for<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x + 3;</span></p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.2.3</b></span><br>
So, lets see how we can reduce our typing on these next four statements:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x + 1;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x - 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x * 2;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x = x / 3;</span><br>
They reduce to:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x += 1;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x -= 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x *= 2;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x /= 3;</span></p>
<p>The C++ makers were nice enough to save some typing for us. You will always
see these shorthands in professional code, so always keep these in the back of
your mind. Once you begin programming, you will become very fluent in the
language and begin using it naturally.</p>
<p><br>
</p>
<h1><u><i>Section 2.3</i></u></h1>
<p>Now we are going to learn the all important <u>assignment precedence and
associativity</u> rules. In math, do you remember the &quot;Pretty Please My
Dear Aunt Sally&quot; (PPMDAS) phrase? That was a saying to remember the <b style="FONT-WEIGHT: bold">precedence</b>
rules of our operators:<br>
&nbsp;&nbsp;&nbsp; Parentheses&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Highest<br>
&nbsp;&nbsp;&nbsp; Powers<br>
&nbsp;&nbsp;&nbsp; Multiplication, Division<br>
&nbsp;&nbsp;&nbsp; Addition, Subtraction&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Lowest</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.3.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 2 + 5 * 3;</span></p>
<p>According to precedence, multiplication comes first before addition. So we
multiply five and three, then add two. <i>x</i> now contains seventeen. We could
have thrown in parentheses and got a different answer:</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.3.2</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = (2 + 5) * 3;</span></p>
<p>Parentheses has the highest precedence here, so we do the inside of them
first. Two plus five is seven, then we multiply by three and get twenty-one.</p>
<p>In C++, there are many other operators we must deal with. We will introduce
two other operators to you (one which you should already be familiar with). We
have the = operator (which we call the <b style="FONT-WEIGHT: bold">assignment
operator</b>), and we have the == operator (which we call the <b style="FONT-WEIGHT: bold">equality
operator</b>).</p>
<p>The = operator will assign what is on the right-hand side to the left-hand
side of the equal sign.</p>
<p>The == operator will test to see if what is on the right-hand side is equal
to the left-hand side. If they are equal, the == operator returns to use the
value of <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true </b></span>(which
is 1). If they are not equal, it returns the value of <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false
</b></span>(which is zero).</p>
<p>These two new operators are also on the precedence list, and now we can
expand the list to this:<br>
&nbsp;&nbsp;&nbsp; ( )&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Highest<br>
&nbsp;&nbsp;&nbsp; ==<br>
&nbsp;&nbsp;&nbsp; =<br>
&nbsp;&nbsp;&nbsp; *, /<br>
&nbsp;&nbsp;&nbsp; +, -&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Lowest</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.3.3</b></span><br>
Which means, if we did a statement like this:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 2;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int y = x == 3;</span></p>
<p><i>x</i> would first be assigned two. Then for <i>y</i>, first <i>x</i> would
be compared to three. Since they are not equal, we get a value of <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>
(which is zero), and assign that to <i>y</i>. <i>y</i> is now zero.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.3.4</b></span><br>
To complicate things a tad-bit further, say that we did this:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 0;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int y = x == 3 == 5;</span></p>
<p>First <i>x</i> is assigned zero. Then for <i>y</i>, we first compare three
against five. Since they are not equal, we get back the value <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>
(which is zero). We then compare the value of zero to the value of <i>x</i>.
They are equal so it returns the value of <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>(which is one) and assign it to <i>y</i>. <i>y</i> now equals one.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.3.5</b></span><br>
For fast initialization of many variables, we can even do this:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int y;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int z;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; z = y = x;</span></p>
<p>All variables now equal three.</p>
<p><br>
</p>
<h1><u><i>Section 2.4</i></u></h1>
<p>Next up in the wonderful world of C++..........<br>
<b style="FONT-WEIGHT: bold">boolean algebra</b> (created by Mr. Boole)</p>
<p>You will now learn how to do more algebra in binary! Remember our great
lesson from last time? We'll for the ones who asked why do I have to know this
stuff, it is because working with bits of a number is more important than the
number itself. I can guarantee that if you can't do boolean algebra, you will
not have a fun time finding a job as a C++ programmer. Boolean algebra is a
fundamental component of programming - rather it is C++, straight C, Visual
Basic, Pascal, etc. This might be a confusing part for non-programmers, so we
are going to spend the rest of the lesson nailing down the basics (What's the
use of a lesson if you left confused?).</p>
<p>The great geniuses of C++ came up with the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">bool</b>
data type (::ding, ding, ding::: New Data Type!). This is even a brand new type
for fellow C programmers who moved to C++ (Remember C++ is just a superset of C,
which means it adds on to C. And if you looked at the name &quot;C++&quot;, it
is C with the increment operator. Pretty cool, huh?).</span></p>
<p><span style="COLOR: #0000ff">Now, if you don't know, the <b style="FONT-WEIGHT: bold">bool</b></span>
data type can hold only two values: <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>
and <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.
If you want numerical value for these <b style="FONT-WEIGHT: bold">constants</b>,
constants are values that never change, use this simple rule:<br>
&nbsp;&nbsp;&nbsp; true&nbsp; = one<br>
&nbsp;&nbsp;&nbsp; false = zero</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.4.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool x = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool y = (false == x);</span></p>
<p>Since == has higher precedence over =, we do test for equality first.<br>
Since <i>false</i> does not equal <i>x</i>, it evaluates the value <i>false </i>which
is set to <i>y</i>.<br>
When we mean &quot;returns&quot;, just think of it as another meaning for the
word &quot;equals&quot;.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.4.2</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool x = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool y = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool z = (true == y) ==
true;</span><br>
&nbsp;<br>
First we test <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>
against <i>y</i> which evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.<br>
We than compare true against<i> </i><span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>
which is<i> </i><span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.4.3</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool x = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool y = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; z = (false == false) ==
true;</span></p>
<p><span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span> is
first compared to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
which returns <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.<br>
The returning <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true </b></span>than
is compared against <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>,
which returns <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.<br>
The returning <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true </b></span>is
now set to <i>z</i>.</p>
<p><br>
</p>
<h1><u><i>Section 2.5</i></u></h1>
<p>There are four main operations we use in logic:<br>
&nbsp;&nbsp;&nbsp; NOT&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; !<br>
&nbsp;&nbsp;&nbsp; AND&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&amp;&amp;<br>
&nbsp;&nbsp;&nbsp; OR&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
||<br>
&nbsp;&nbsp;&nbsp; XOR&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ^</p>
<p>NOT takes the opposite of a boolean value. If a variable is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>,
the NOT of it is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.
Think of it in English: if a value is not <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>,
it is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.</p>
<p>AND takes two variables and determines if both are <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
If both are, AND evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
If either one or both are <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
it evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.</p>
<p>OR takes two variables and determines if any of them are <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
If just one or both are, OR returns <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
Otherwise, it is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.</p>
<p>XOR won't be discussed in-depth. XOR stands for Exclusive-OR. It only returns
true when only one value is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
If both are the same value (either both <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>or both <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
it evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>).</p>
<p>Now we have to add these (yes, once again) to our precedence list:<br>
&nbsp;&nbsp;&nbsp; ( )&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Highest<br>
&nbsp;&nbsp;&nbsp; !<br>
&nbsp;&nbsp;&nbsp; ==<br>
&nbsp;&nbsp;&nbsp; =<br>
&nbsp;&nbsp;&nbsp; &amp;&amp;<br>
&nbsp;&nbsp;&nbsp; ||<br>
&nbsp;&nbsp;&nbsp; *, /<br>
&nbsp;&nbsp;&nbsp; +, -&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Lowest</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.5.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool x = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool y = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool z = x &amp;&amp; y;</span></p>
<p><i>x</i> and <i>y</i> is ANDed (&amp;&amp;) together. Since <i>y</i> is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
it makes the entire expression <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
and <i>z</i> is set to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 2.5.2</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool x = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool y = !true == x
&amp;&amp; !x;</span></p>
<p><i>!x </i>equals <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span><i>.</i><br>
ANDed with <i>x </i>which evaluates <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span><br>
And that evaluated <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span><i>
</i>compared to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">!<i>true
</i></b></span>evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.<br>
<i>y</i> evaluates <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.</p>
<p><br>
</p>
<h1><u><i>New terms to remember</i></u></h1>
<p>Allocate<br>
And<br>
Boolean<br>
Bugs<br>
Constant<br>
Decrement<br>
</p>
<h2><span style="COLOR: #0000ff">false</span></h2>
<p>Initialization<br>
Intial value<br>
increment<br>
Not<br>
Or<br>
Precedence<br>
Undefined<br>
Uninitalized<br>
</p>
<h2><span style="COLOR: #0000ff">true</span></h2>
<p>Xor</p>
<p><br>
</p>
<h1><u><i>Review problems</i></u></h1>
<p>01. What is wrong with this code? (find the bug)<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int x;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int y = 2;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int z;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
z = y + 1;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
y = z + y;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
z = z + x;</span></p>
<p>02.&nbsp; What values do we get for all the variables?<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int a = 3;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int b = 45;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int c = 1;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool d = c == 1;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool e = false == false == 1;</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
03. Why won't this code compile?<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
r = 44;</span></p>
<p>04. What do we get in this?<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool x = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool y = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool z = ((x == y) == y);</span></p>
<p>05. What do we get in this?<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool x = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool y = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool z = false == true == false == x;</span></p>
<p>We will be using these variables in the following examples:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool p = true;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool q = false;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
bool r = true;</span></p>
<p>06. <span style="FONT: 10pt/13pt Geneva">bool a = !true;</span></p>
<p>07. <span style="FONT: 10pt/13pt Geneva">bool b = (false == !false)
&amp;&amp; true;</span></p>
<p>08. <span style="FONT: 10pt/13pt Geneva">bool c = q &amp;&amp; r == false;</span></p>
<p>09. <span style="FONT: 10pt/13pt Geneva">bool d = (p &amp;&amp; q) || r;</span></p>
<p>11. <span style="FONT: 10pt/13pt Geneva">bool e = (r &amp;&amp; r) &amp;&amp;
q;</span></p>
<p>12. <span style="FONT: 10pt/13pt Geneva">bool f = p &amp;&amp; (q || r);</span></p>
<p>13. <span style="FONT: 10pt/13pt Geneva">bool g = !q &amp;&amp; p;</span></p>
<p>14. <span style="FONT: 10pt/13pt Geneva">bool h = !(q || p);</span></p>
<p>15. <span style="FONT: 10pt/13pt Geneva">bool k&nbsp; = p &amp;&amp; !q || r
|| p &amp;&amp; !p</span></p>
<p>ML&gt;<br>
</p>

