Automated reporting with EcoInvent
==============================

Automating the visualization of data sets from the EcoInvent data base in their automatic pdf creator.

Project Team
-----------

[Sarah Dutschke](https://www.linkedin.com/in/sarah-dutschke/), 
[Angela Niederberger](https://www.linkedin.com/in/angela-niederberger/)

Supervisors
-----------

[Marie Bocher](linkedin.com/in/marie-bocher-8b6b5562), 
[Albin Plathottathil](https://www.linkedin.com/in/albin-plathottathil/), 
[Nitin Kumar](https://www.linkedin.com/in/drnitinkumar)

Company
-------
[EcoInvent](https://www.ecoinvent.org/) & [Propulsion Academy](https://propulsion.academy/)

Project description
-------------------
Organisations increasingly look to understand the end-to-end impact a product has on the environment. For this purpose, ecoinvent provides a comprehensive life cycle assessment database to thousands of companies such as Toyota, Lego and Procter & Gamble as well as government organisations and universities. Though the data sets are comprehensible on their own, the underlying calculations and methods used to estimate environmental impacts can be complex and overwhelming to understand for most people. 
In this project, Angela Niederberger and Sarah Dutschke helped ecoinvent make their holistic reports more user friendly by adding data visualisations representing the impacts and network structure of production chains. The main challenges were to make those visualisations fit for about 60’000 diverse data sets in a uniform way, displaying only the most relevant information statically. The python script produced in this project will be integrated into ecoinvent’s automatic pdf generator, thereby reaching thousands of clients.

Key words & Features of the code
--------------------------------
Matrix calculations, list preparation, logging functions, save to powerpoint, save as png/jpg/svg file, automatic scaling where necessary, handling of negative values, plotly, nested treemaps, horizontal bar plots, visualization of network structures, life-cycle assessment


Project Milestones
-------------------

### Milestone 1
Impact visualization: Improve the table showing impact score, by adding a chart that shows the most significant contributors ('flow compartments'). Use data calculated from our release script, provided as csv files. This chart should allow to identify which part of the supply chain is responsible for impact score on the commonly used impact assessment methods.

### Milestone 2
Network structure visualization: Add a treemap plot for each method to show the main contributors (impacts and emissions). It should display as many levels as necessary until it the main contributor is below 50%. However, total limit of levels to diplay are 5. Use data calculated from our release script, provided as csv files. 

### Milestone 3
Transform exploratory analysis results from previous milestones into a high quality documented code that can run on a large amount of datasets and integrate flawlessly into the existing release pipeline.

Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   └── raw            <- 6 csv matrices each for 3 system models: 'A_public', 'B_public', 'C_public', 'ie_index', 'ee_index', 'LCIA_index'
    │        └── 'cutoff'
    │        └── 'consequential'
    │        └── 'apos' 
    │
    ├── logs             <- new dir, created automatically, contains generated log for barplot and treemap generation
    ├── plots            <- new dir, created automatically, contains generated example plots in png format
    │
    ├── environment.yml   <- The requirements file for reproducing the analysis environment
    │         
    ├── environment_details.yml   <- The requirements file for reproducing the analysis environment, indicating library versions.
    │
    ├── data_loading.py        <- Adjust general settings here (path, font_type, hues, etc.) and find script for data importation
    │
    ├── data_processing.py        <- Script to preprocess data for both, barplots and treemaps.
    │
    ├── helper_functions.py        <- Script for auxiliary functions, such as split_subitem, split_method_name, plot_type_definition, shorten_product_name etc.
    │
    ├── list_preparation.py        <- Script for further data processing for treemaps.
    │
    ├── main.py        <- Run script to produce barplots and treemaps in png format while generating a log in excel/csv.
    │
    └── plotting_functions.py     <- Scripts with subfunctions to plot barcharts and/or treemaps while generating a log in excel/csv.
    
  

--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
