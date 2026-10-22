Name: Evan Jorge-Munoz
UTA ID: 1002214605

Code runs as expected but there are two ways that the tests run functionally correct when executed in this specified order of running: 

- Way 1: run proj2_test 0 and then proj2_test 1 (right after)

Or
 
- Way 2: run proj2_test 0 (or) 1 then reset the system to then run proj2_test 0 (or) 1 this works as expected as well. 

If not ran in this specified order, then the output for proj2_test 1 tends to cut short for some reason.


Comment:

The output functions correctly and is represented as expected, however, when running the proj2_test 1 command for lazy allocation, the output is missing the print statement in line 4 for test 5 and in line 4 for test 6. Everything else executes as expected.
