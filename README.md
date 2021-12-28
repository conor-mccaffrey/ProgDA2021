# <u> Participant Representation in Cancer Clinical Trials </u>
## Author: Conor McCaffrey

![python&jupy.png](Images/jupyter.png)
<i>Reference 1 </i>

This repository contains a Jupyter notebook and relevant Images/Files demonstrating the use of `pandas` , `numpy` , `matplotlib`, `seaborn` and other packages in the analysis of Clinical Trial Participant demographics in Oncological Trials.

This notebook is not only of use to those who want to gain familiarity with `matplotlib` and `python`, but it also serves as a resource for analysing different demographics of participants in Clinical Trials. We cover the basic idea of Clinial Trials, profit margins of certain Pharama companies and then explore different variables in a common clinical trial dataset. We also cover the idea behind synthetic datasets and it's advantages going forward. 

You can view the static version of the  `pyplot.ipynb`  notebook by clicking the following button:

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/conor-mccaffrey/ProgDA2021/blob/main/Programming%20for%20Data%20Analysis.ipynb)


Alternatively, you can view the notebook in dynamic form by clicking the following button:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/conor-mccaffrey/ProgDA2021/main?filepath=Programming%20for%20Data%20Analysis.ipynb)

***
The notebook `Programming for Data Analysis.ipynb` contains a detailed clinical trial participants based on different demographics. Some interesting observations were deducted from our analysis. This is acheived through the incorporation of `pandas` dataframes, histograms, descriptive analyses and pie-charts. `Matplotlib` and `seaborn` were heavily incorporated for this notebook. 

This notebook would be suitable for people looking to see different characteristics of clinical trial participants. There is a dearth of reviews conducted that cover this topic. Building more awareness on participant demographics will highlight the fact certain demographics are under-represented. I think this would be a beneficial tool for everyone as it will then lead to increased efforts to widen eligibility criteria and promote efforts for more inclusiveness. This will prevent 'gaps in understanding' for certain conditions like we have today.


### Installation

1. Download Anaconda if space permits. 
2. Alternatively, download the latest version of Python (3.10.0).
3. Consult `requirements.txt` for packages used in the notebook. 

### Run

Here is how to run the `Programming for Data Analysis.ipynb` notebook:
1. Open cmdr terminal.
2. Go to notebook location.
3. Run Jupyter with `Programming for Data Analysis.ipynb` using code `Jupyter Notebook`.   
4. Copy code in cmdr if page does not load automatically.



### Explore

Have a look at the notebook in this repo in Jupyter.
Some interesting aspects for `Programming for Data Analysis.ipynb`:

- We can see how White males are over-represented in clinical trials. 
- There is also the intersting anamoly that estrogen was first used in studies for treating heard conditions in men. 
- We identify how older people are excluded from participation due to strict enrollment criteria,
- We discover that individuals earning less money are less likely to participate in clinical trials. This needs to be addressed urgently as we know certain conditions affect lower 'socio-economic' classes more directly.

Change the following code (fontsizes and colours) and see how the plot changes in respect to its appearance:
```python
# Let's use subplots to plot our data
fig, (ax1,ax2,ax3,ax4) = plt.subplots(1,4, figsize=(12, 12))

ax1.bar(OF['Gender'], OF['Count'], label='Over 50', color = 'green',)
ax1.set_title('Over 50 Female', fontsize = 15)
ax1.set_ylabel('Occurrences', fontsize = 15)
ax1.set_ylim([0, 120]) # setting y limits



ax2.bar(YF['Gender'], YF['Count'], label='Under 50', color = 'orange')
ax2.set_title('Under 50 Female', fontsize = 15)
ax2.set_ylim([0, 120])


ax3.bar(YM['Gender'], YM['Count'], label='Under 50', color = 'blue')
ax3.set_title('Under 50 Male', fontsize = 15)
ax3.set_ylim([0, 120])


ax4.bar(OM['Gender'], OM['Count'], label='Over 50', color = 'red')
ax4.set_title('Over 50 Male', fontsize = 15)
ax4.set_ylim([0, 120]);

```


### Credits


I heavily relied on StackOverflow for solving many issues. You can find the main homepage here for Python queries: [StackOverflow](https://stackoverflow.com/questions/tagged/python).

All other resources are referenced in the notebook. 


## Conclusion

The notebooks contained in this repository serve as a great resource into various aspects of coding: 
- The use of `python` and `jupyter`
- The use of `pandas`, `numpy` and `matplotlib`
- Overview of functionalities of plotting
- Generation of synthetic datasets.

These aspects are the foundation of good programming and therefore this repository can be consulted at any stage. The generation of synthetic datasets will become an important tool in the future due to the decreased costs, enhanced patient data privacy and the ease at which data can be generated.


## References for README
1. https://www.dataquest.io/blog/jupyter-notebook-tutorial/
