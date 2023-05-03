Download Link: https://assignmentchef.com/product/solved-cs1134-homework-2-using-the-definitions-of-o-and-of-%ce%b8
<br>
<strong>Homework #2</strong>







<strong><u>Question 1: </u></strong>

Use the definitions of O and of Θ in order to show the following:

<table>

 <tbody>

  <tr>

   <td width="31">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>5 n<sup>3</sup> + 2 n<sup>2</sup> + 3 n = O <sup>3</sup></li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="14">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="24">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

b . 7n<sup>2</sup> + 2 n − 8 = Θ

c . Show that if <em>d(n)=O(f(n)) </em>and <em>e(n)=O(g(n))</em>, then the product <em>d(n)e(n) </em>is O <em>( f (n)g(n))</em>.

<strong><u>Question 2 : </u></strong>

Give a θ characterization, in terms of <em>n</em>, of the running time of the following four functions:

<strong>de f </strong>example1(lst):

”””Return the sum of the prefix sums of sequence S.ÓÓÓ

n = len(lst) total = 0

<strong>for </strong>j <strong>in </strong>range(n):

<strong>for </strong>k <strong>in</strong> range(1+j):

total += lst[k]

<strong>return </strong>total <strong>def </strong>example2(lst): ”””Return the sum of the prefix sums of sequence S.ÓÓÓ

n = len(lst) prefix = 0

total = 0

<strong>for</strong> j <strong>in </strong>range(n):

prefix += lst[j]

total += prefix

<strong>return</strong> total

<strong>def </strong>example3(n): i = 1

sum = 0

<strong>while </strong>(i &lt; n*n):

i *= 2

sum += i <strong>return </strong>sum

<strong>def </strong>example4(n):

i = n

sum = 0

<strong>while </strong>(i &gt; 1):

<strong>for </strong>j <strong>in </strong>range(i):sum += i*j

i //= 2

<strong>return </strong>sum




<strong><u>Question 3: </u></strong>

Implement a function <strong>def </strong>factors(num) . This function is given a positive

integer num, and returns a <u>generator,</u> that when iterated over, it will have all of num’s divisors in an <strong>ascending order</strong>.

For Example, if we execute the following code: <strong>for </strong>curr_factor <strong>in </strong>factors(100): print(curr_factor)

The expected output is:

1 2 4 5 10 20 25 50 100

<u>Implementation requirement:</u> Pay attention to the running time of your

<table>

 <tbody>

  <tr>

   <td width="58">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

implementation. The <strong>for </strong>loop like the above, should run in a total cost of Θ  .

<strong><u>Question 4: </u></strong>

The number <strong><em>e </em></strong>is an important mathematical constant that is the base of the natural logarithm. <strong><em>e </em></strong>also arises in the study of compound interest, and in many other applications.

Background of <strong><em>e</em></strong>:<u> <a href="https://en.wikipedia.org/wiki/E">https://en.wikipedia.org/wiki/E</a> (mathematical constant)</u>

<strong><em>e </em></strong>can be calculated as the sum of the infinite series:

4             4            4           4

= 1 +______ +____ +____ +___


The value of <strong><em>e </em></strong>is approximately equal to 2.71828. We can get an approximate value of <strong><em>e</em></strong>, by calculating only a partial sum of the infinite sum above (the more addends we add, the better approximation we get).

Implement the function <strong>def </strong>e_approx(n). This function is given a positive integer n, and returns an approximation of <strong><em>e</em></strong>, calculated by the sum of the first (n + 1) addends of the infinite sum above.

To test your function use the following main:

<strong>def</strong> main():

<strong>for</strong> n<strong> in </strong>range(15):

curr_approx = e_approx(n)

approx_str =<strong> “{:.15f}”</strong> .format(curr_approx)

print(<strong>“n</strong><strong> =”</strong> , n,<strong> “Approximation:”</strong>, approx_str)

<u>Note:</u> Pay attention to the running time of e_approx. By calculating the factorials over for each addend, your running time could get inefficient. An efficient

<table>

 <tbody>

  <tr>

   <td width="24">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

implementation would run in Θ  .




<table>

 <tbody>

  <tr>

   <td width="10">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="9">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<strong><u>Question 5: </u></strong>

Implement the function <strong>def </strong>split_parity(lst) . That takes lst, a listof integers. When called, the function changes the order of numbers in lst so that all the odd numbers will appear first, and all the even numbers will appear last. Note that the inner order of the odd numbers and the inner order of the even numbers don’t matter.

For example, if lst is a list containing [1, 2, 3, 4], after calling split_parity, l s t could look like: [ 3, 1, 2, 4].

<u>Implementation requirements:</u>

1 . You are <strong>not allowed </strong>to use an auxiliary list (a temporary local list).

2 . Pay attention to the running time of your implementation. An efficient

implementation would run in a linear time. That is, if <em>n </em>is the length of lst, the

<table>

 <tbody>

  <tr>

   <td width="24">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

running time should be Θ  .

<strong><u>Question 6: </u></strong>

Implement the function <strong>def </strong>two_sum(srt _lst, target). This function is given:

<ul>

 <li>srt _lst – a list of integers arranged in a <strong>sorted </strong>order</li>

 <li>target – an integer</li>

</ul>

When called, it returns two indices (collected in a tuple), such that the elements in their positions add up to target. If there are no such indices, the function should return None.

For example, if srt_lst=[-2, 7, 11, 15, 20, 21], and target=22, your function would return (1, 3) because srt_lst[1]+ srt_lst[3]=7+15=22

<u>Note:</u> Pay attention to the running time of your function. Aim for a linear time algorithm.

<strong><u>Question 7: </u></strong>

Implement the function <strong>def </strong>findChange(lst01). This function is given l s t 0 1 , a list of integers containing a sequence of 0 s followed by a sequence of 1 s.

When called, it returns the index of the first 1 in l s t 0 1 .

For example, if lst01 is a list containing [0, 0, 0, 0, 0, 1, 1, 1], calling findChange(lst01) will return 5.