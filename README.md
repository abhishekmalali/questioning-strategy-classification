# questioning-strategy-classification
Repository for AM207 final project for finding the optimal method of asking questions when making experts classify images/cases in a multi-class classification problem.


Important Notebooks 
-------------------

1) MC_posterior.ipynb - This notebook uses PyMC to recover separate confusion matrices for every worker from the generated data. We only attempted this for the Multiclass case in this notebook.

2) PyMC-MC-posterior.ipynb - This notebook uses PyMC to recover the shared confusion matrices for all workers from the generated data. We attempted the Multiclass case in the notebook. All PyMC based results for Multiclass data are present in this notebook.

3) PyMC-YN-posterior.ipynb - This notebook recovers the shared consuion matrices for all workers using the data in the Yes/No paradigm. All PyMC based results for the Yes/no paradigm are present in this notebook.

4) Simulated-annealing-MC-non-constrained.ipynb - This notebook solves for the shared confusion matrix and the correct class assignments given the mulitclass data. We use simulated annealing to solve for them. All results for multiclass simulated annealing are present in this notebook.

5) Simulated-annealing-YN.ipynb - This notebook solves for shared confusion matrix and correct class assignments for Yes/No data. All results for the Yes/No data are present in this notebook.

6) Dawid-Skene.ipynb - This notebook solves for the confusion matrices, class distributions and class assignments for the following cases:
 * Expectation Maximization for Multiclass data with a shared confusion matrix
 * Expectation Maximization for Multiclass data with separate confusion matrices for each worker
 * Expectation Maximization for Yes/No data with separate confusion matrices for each worker
This notebook also contains all the code for generating the visualizations in the paper and poster, which are side-by-side comparisons for the various methods.  



Other Notebooks 
---------------

1) simulated-annealing-mc.ipynb - This notebook has an attempt at running Simulated annealing in an constrained enviroment. We assume we know the confusion matrix(Assume it to be near identity matrix) and the class distribution. This was an initial starting attempt at solving the class inference problem using the Simulated annealing approach.

2) simulated-annealing-multiple-c-mc.ipynb - This notebook has an attempt at Simulated annealing to recover the individual confusion matrix instead of the shared confusion matrix. This is to determine the workers with bad labeling performance. Simulated annealing does not converge to a solution since the space in which it is searching grows by separating the confusion matrices, making it much harder for Simulated annealing to converge to a global or in this case even the local maximum.
