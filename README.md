# Evolutionary Algorithm to Schedule TAs to class sections
This algorithm was part of a Fall 2023 homework assignment for DS3500 - Advanced Programming with Data at Northeastern University. Worked with @sahana-dhar and @payeurjeremiah to optimize scheduling inspired by biological processes. With data on class scheules and TA's preferences, our metrics are: overallocation of TAs to a section, time conflicts, undersupported sections (not enough TAs), sections TAs are unwilling to be assigned to, and sections TAs do not prefer. Some of these metrics are more important than others; for example, time conflicts of TA assignments are more significant to the success of the scheduling algorithm than whether or not a TA prefers to be in a certain section. 

## How to Schedule
1. Clone this repository.
2. Run `ta_assign_evo.py`.
3. The output is a csv file titled `nondominated_solutions.csv` (this is already included in the repository, remove the file or change the output name before running to avoid overwriting it).

## Understanding the Outputs
1. Every 44 rows of `solutions.csv` corresponds to one solution of the scheduling algorithm, where each row is a TA in trasnposed order of their listing in `tas.csv` and a 1 indicates that they were assigned to the class section corresponding to the column. The `solutions.csv` file columns represent the class sections in transposed order of their listing in `sections.csv`.
2. `nondominated_solutions.csv` contains the 'better' solutions from `solutions.csv` and their number of overallocation, conflicts, undersupported, unwilling, and unpreffered TAs. 
3. One of our best solutions has 6 overallocations, 4 conflicts, 5 unprefered, 0 unwilling and 26 unprefered, see assignments_solution.pdf for the full TA assignment. 
