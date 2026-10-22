Code runs as expected, but there are two ways that the tests run correctly when executed in this specified order of running: 

- Way 1: run proj2_test 0 and then proj2_test 1 (right after)

Or
 
- Way 2: run proj2_test 0 (or) 1, then reset the system, then run proj2_test 0 (or) 1; this works as expected as well. 
