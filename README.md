## Relating paper ##
Information Design for Congestion Games with Unknown Demand. \
S. M. Griesbach, M. Hoefer, M. Klimm, T. Koglin. \
Accepted at AAAI24. \
[Link to Arxiv](https://arxiv.org/abs/2310.08314)


## General information ##

This repository provides the code and data used in the computational study of the paper combined in a single zip-file.

The main code for computing the flows in Wardrop equilibrium is highly based on the work of Matteo Bettini (https://github.com/matteobettini/Traffic-Assignment-Frank-Wolfe-2021; last accessed: 2022-01-06). Yet, we adjusted it to our model and the information design framework.

The network data was obtained from the Transportation Networks for Research Core Team (https://github.com/bstabler/TransportationNetworks; last accessed: 2022-01-14.).

## Guiding notes for using the repository ##

### Code ###
- Main code for data generation, the next three codes contain subroutines ("./compute_data.py")
- Implementation of LP for determining range of supports ("./lp_solver.py")
- Flow assignment ("./Traffic-Assignment-Frank-Wolfe-2021-main/assignment.py")
- Loading networks ("./Traffic-Assignment-Frank-Wolfe-2021-main/network_import.py", "./Traffic-Assignment-Frank-Wolfe-2021-main/utils.py")
- Postprocessing of data files ("./find_duplicates.py")
- Code for computing the statistic quantities in Tables 2 and 3 ("./compute_stats.py")


### Data ###
For each instance, a file 'support_{four-digit number}.txt' stores all simulation results.
The four-digit numbers are assigned as follows:
SF: 19...
EM: 20...
BF: 21...
BP: 22...
BT: 23...
BM: 24...

Navigation:
- All support-files generated in terms of our computational study ("./loop_results/stat_data/")
- Support-files considered in our results, after clearing by find_duplicates.py ("./loop_results/stat_data/cleared/")
- Results computes by compute_stats.py ("./loop_results/stat_eval/")
- Network data ("./TransportationNetworks-master/")


### Miscellaneous ###
- Handbook for flow assignment techniques for references ("./traffic_assignment_book.pdf")
  Source: https://sboyles.github.io/teaching/ce392c/book.pdf (last accessed: 2022-01-07)
