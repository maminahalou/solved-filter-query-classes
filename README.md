Download Link: https://assignmentchef.com/product/solved-filter-query-classes
<br>
5/5 - (2 votes)

Project Outline



The input consists of a set s of N two-dimensional records of integers, each of which consists of a pair of coordinates (xLiJ ) for o i N-l, where the x[iJ are distinct (i.e., no two are

equal) and the y[il are also distinct.

Intuitively, the x coordinates represent one desirable attribute of each record, whereas the y coordinates represent another (different) desirable attribute of the record.

Part 1

Overview

Write a program that eliminates from s every record for which there exists another record having both x[jl x[iJ and ylj] y[i].

Intuitively, we want to eliminate all records that are doubly inferior to at least one Other record, where “doubly” means in terms of both x coordinate and in terms of y coordinate.

Output the surviving (“filtered”) records in s sorted according to increasing order of their x coordinates.

Note: You am allowed to use existing sorts (no need to write your own).

Implementation

Create a class Filter. java to perform the task described above. Your program should process input using Stdln. java in the following format.

The first line consists of a single integer N, the number of records to read. This is followed by a list of N records, one per line, each consisting of two integers x and y separated by a space. The

records do not appear in any specific order.

Your program should output the filtered, sorted records using Stdout. java. Write one record per line, x followed by y separated by a space.

We have provided example input / output files in the archive linked at the beginning of the handout. Use filterl . txt, filter2. txt, and filter3. txt as input, and txt,

filter20ut. txt, and filter30ut. txt as output to test your program.

Part 2

Overview

Put the sorted input N records (unfiltered) into an array, sorted by their x coordinates in increasing order. That array can be viewed as representing a complete binary tree T. For every node v of T,

create an array that contains the records in the subtree of v in T, sorted according to their y coordinates. Note that this creates multiple copies of a record (as many as the record’s ancestors in

Hint: After turning T into a search tree by x coordinates, create the L v ‘s in bottom-up order, so that you can obtain the L v of a v whose children are u and w by merging the already-computed

L[u] with the already-computed L[w] and with v.

Use the tree T and the L [v 1 lists to efficiently process queries of the type Q (a, b) that outputs the records whose x coordinate is greater than a AND y coordinate is greater than b. The records Output

from each query, should be sorted by their x coordinates in increasing order.

Performance for each such query should be + m log m) time where m is the number of output records.

Note: O(log N + m log m) time performance is possible, but not required.

Implementation

Create a class Query. java to perform the task described above. Your program should process input using Stdln. java in the following format.

The first part of the input is the same as for part I : the first line has a single integer N, followed by N records, one record per line, each consisting of two integers x and y separated by a space. As in

part 1 , the records do not appear in any specific order. The line following the last record contains a single integer Q, the number of queries to process. This is followed by Q lines, one query per line,

consisting of two integers a and b separated by a space. Your program should process and output each query in the order it appears.

Your program should print the records output from each query to std0ut. java. For each query, output m records, one per line, each consisting of two integers x and y separated by a space, where m

is the number of records returned by that query? If a query returns zero records, Output a single line with the string “none’ (without quotes).

As with part I , we ve included example input / output files in the archive linked at the top of the handout. Use queryl . txt, query2 *txt, and query3. txt as input, and querylout. txt,

query20ut. txt, and query30ut. txt as output to test your program.