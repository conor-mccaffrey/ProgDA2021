# <u> Programming for Data Analysis </u>
## Author: Conor McCaffrey

![python&jupy.png](Images/jupyter.png)
<i>Reference 1 </i>

This repository contains a Jupyter notebook and relevant Images/Files demonstrating the use of `pandas` , `numpy` , `matplotlib`, `seaborn` and other packages in the analysis of Clinical Trial Participant demographics in Oncological Trials.


This notebook is not only of use to those who want to gain familiarity with `matplotlib` and `python`, but it also serves as a resource for analysing different demographics of participants in Clinical Trials. We cover the basic idea of Clinial Trials, profit margins of certain Pharam companies and thenexplore different variables in a common clinical trial dataset. We also cover the idea behind synthetic datasets and it's uses going forward. 

You can view the static version of the  `pyplot.ipynb`  notebook by clicking the following button:

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/conor-mccaffrey/ProgDA2021/blob/main/Programming%20for%20Data%20Analysis.ipynb)


Alternatively, you can view the notebook in dynamic form by clicking the following button:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/conor-mccaffrey/ProgDA2021/main?filepath=Programming%20for%20Data%20Analysis.ipynb)

***
The notebook `cao-points-analysis.ipynb` contains a detailed analysis of CAO points in 2019, 2020 and 2021. Some interesting observations were deducted from our analysis. This is acheived through the incorporation of `pandas` dataframe, histograms, scatterplots and pie-charts. `Matplotlib` , `seaborn` and `plotly` were heavily incorporated for this notebook. `Plotly` was brought into this notebook as I believe the plots to be more accessible than through `matplotlib`. A challenge here however, is that `plotly` will not render on GitHub (so in this case I saved the figures and laoded them onto the notebook) but they render perfectly using `nbviewer` and `binder`.

This notebook would be suitable for people looking to see differences in points between certain CAO courses over the period 2019-2021 and also for identifying trends in courses (i.e Top 5 courses). I think this would be a beneficial tool for everyone as I don't think it currently exists (not that I have seen anyway).

You can view the static version of the  `cao-points-analysis.ipynb`  notebook by clicking the following button:

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/conor-mccaffrey/fundamentals_of_Data_Analysis/blob/main/cao-points-analysis.ipynb)


Alternatively, you can view the notebook in dynamic form by clicking the following button:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/conor-mccaffrey/fundamentals_of_Data_Analysis/main?filepath=cao-points-analysis.ipynb)


### Installation

1. Download Anaconda if space permits. 
2. Alternatively, download the latest version of Python (3.10.0).
3. Consult `requirements.txt` for packages used in the notebook. 

### Run

Here is how to run the `cao-points-analysis.ipynb` notebook:
1. Open cmdr terminal.
2. Go to notebook location.
3. Run Jupyter with `cao-points-analysis.ipynb` using code `Jupyter Notebook`.   
4. Copy code in cmdr if page does not load automatically.



### Explore

Have a look at the two notebooks in this repo in Jupyter.
Some interesting aspects for `pyplot.ipynb`:

- The notebook `plots.ipynb` has three difference plot types as examples. You can edit the parameters of the plots to see different effects.

Change the following code (numbers and colours) and see how the plot changes in respect to its appearance:

```python

```

Some interesting aspects for `cao-points-analysis.ipynb`:

- The notebook `cao-points-analysis.ipynb` contains a detailed analysis of CAO points from 2019-2021.
- Some courses contain no data which is clearly an error on the CAO team's part. 
- We have delved into 'points differences' in the certain courses over a period of years which is very informative.
- There is a wealth of information to be gleaned from these datasets. For example, the parameters in a lot of code can be altered to display difference results. The following code can be easily altered to compare difference parameters:
```python
# Let's look at the value differences between some courses in this dataframe
# Let's convert our Points_R1_2021 column to a float as it is currently an 'object'
level_seven_clean['Points_R1_2021']= pd.to_numeric(level_seven_clean['Points_R1_2021'], errors='coerce').astype('float')
# Code to find the difference in values between EOS and Mid [25]
level_seven_clean['Val_Diff'] = level_seven_clean['Points_Mid_2019'] - level_seven_clean['Points_R1_2021']
# Let's display our result
level_seven_clean.sort_values('Val_Diff', ascending = False).head(15)
```
  


### Credits

####

I heavily relied on StackOverflow for solving many issues in the generation of the two notebooks. You can find the main homepage here for Python queries: [StackOverflow](https://stackoverflow.com/questions/tagged/python)





## Troubleshooting
```python

import warnings
warnings.filterwarnings("ignore")
```
The warning package was incorporated into the notebooks in order to allow to following code to execute with no warning message. The code executed fine, this was just with the appearance in mind.


## Conclusion

The notebooks contained in this repository serve as a great resource into various aspects of coding: 
- The use of `python` and `jupyter`
- The use of `pandas`, `numpy` and `matplotlib`
- Overview of functionalities of plotting

These aspects are the foundation of good programming and therefore this repository can be consulted at any stage. The `pyplot.ipynb` and `cao=points-analysis.ipynb` noteboos have taken a dataset, prepared it for analyses and then plotted results i.e the whole process flow we would meet in industry when given a dataset to analyse.

## References for README
1. https://www.dataquest.io/blog/jupyter-notebook-tutorial/
