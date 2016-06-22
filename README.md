# bash-script
A Bash script that computes simple statistics from Operating Systems Course

A Bourne shell script that calculates the average(s) and median(s) from an input file of numbers. The input file must have whole number 
values separated by tabs, and each line of this file will have the same number of values. The script can calculate the average and median 
across the rows (calculating a students grade) or down the columns (calculating the average scrore on an assignment). 

Command structure:
stats {-rows|- cols} [input_file]

The curly braces separated by a vertical bar, means you should choose one of the things; here for example, you must choose either 
-rows or -cols. The option -rows calculates the average and median across the rows; the option -cols calculates the average and median 
down the columns. The input file, in square brackets, is optional. If you specify an input_file the data is read from that file; otherwise, 
it is read from standard input.

Example usage of program:

% cat test_file

1 1 1 1 1

9 3 4 5 5

6 7 8 9 7

3 6 8 9 1

3 4 2 1 4

6 4 4 7 7

% stats -rows test_file

Average Median

1       1

5       5

7       7

5       6

3       3

6       6

% cat test_file | stats –c

Averages:

5 4 5 5 4

Medians:

6 4 4 7 5

% echo $?

0

% stats

Usage: stats {-rows|- cols} [file]

% stats -r test_file nya-nya- nya

Usage: stats {-rows|- cols} [file]

% stats -both test_file

Usage: stats {-rows|- cols} [file]

% chmod -r test_file

% stats -columns test_file

stats: cannot read test_file

% stats -columns no_such_file

stats: cannot read no_such_file

% echo $?

1
