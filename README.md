# Exploring NASAs turbofan data set
This repo contains the notebooks accompanying a small series of blog posts [1] on the NASA turbofan degradation data set [2]. The turbofan data set consists of 4 separate challenges of increasing difficulty. The engines operate normally in the beginning but develop a fault over time. For each challenge, the engines in the train set are run to failure. The timeseries in the test set end 'sometime' before failure. The goal is to predict the Remaining Useful Life (RUL) of each turbofan engine in the test set.  See the table below for a short overview of the challenges.


| Data set | Operating conditions | Fault modes | Train size (nr. of engines) | Test size (nr. of engines) |
| --- | --- | --- | --- | --- |
| FD001 | 1 | 1 | 100 | 100 | 
| FD002 | 6 | 1 | 260 | 259 |
| FD003 | 1 | 2 | 100 | 100 |
| FD004 | 6 | 2 | 248 | 249 |

The notebooks are used to explore the data set and try various modeling techniques (both Machine Learning and Neural Networks). For the full explanation of the techniques and choices made during model development I recommend reading the blog posts [1].

## Running the notebooks
- clone this repository to your computer
- navigate into the folder:  `cd exploring-nasas-turbofan-data-set`
- create a folder for the data: `mkdir data`
	- download the data from the official [NASA data repository](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan) [3] 
	- Extract the `.zip` file to `exploring-nasas-turbofan-data-set/data/`
	- You should now have all the data in `exploring-nasas-turbofan-data-set/data/CMAPSSData/`
- use the requirements.txt to recreate the Python environment used to run these notebooks. I prefer using Anaconda, but any Python environment manager will do.
- Activate the environment the environment from your preferred command line tool, navigate to `exploring-nasas-turbofan-data-set` and start your local notebook server by typing `jupyter notebook`
- Have fun following along with the notebooks!

## References
[1] [blog post series](https://towardsdatascience.com/tagged/exploring-nasa-turbofan)  
[2] A. Saxena, K. Goebel, D. Simon, and N. Eklund, “Damage Propagation Modeling for Aircraft Engine Run-to-Failure Simulation”, in the Proceedings of the Ist International Conference on Prognostics and Health Management (PHM08), Denver CO, Oct 2008.  
[3] data repository: [https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan)
