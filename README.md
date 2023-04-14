<div align="center">
<img alt="EvoCluster-logo" src="http://evo-ml.com/wp-content/uploads/2021/06/EvoloPy-logo.png" width=80%>
</div>

# EvoloPy: An open source nature-inspired optimization toolbox for global optimization in Python

The EvoloPy toolbox provides classical and recent nature-inspired metaheuristic for the global optimization. The list of optimizers that have been implemented includes Particle Swarm Optimization (PSO), Bat Algorithm (BA), Firefly Algorithm (FA), Cuckoo Search (CS), and Whale Optimization Algorithm (WOA). The full list of implemented optimizers is available here https://github.com/7ossam81/EvoloPy/wiki/List-of-optimizers


## Installation
- Python 3.xx is required.

## Google Colaboratory

The code can be run directly in Google Colaboratory. It is good practice to create a copy of the Google Colaboratory and then perform the tests. A copy can be created from File-> Save a copy in Drive. The Link to the Google Colaboratory is Here: 

<a href = "https://colab.research.google.com/drive/1ewSAxctAXvc2YVTJQxADziLWtZ42cud4#scrollTo=eahYmfKKJ62g" target="_blank"> Google Colaboratory Code </a>

Each cell in Google Colaboratory needs to be run sequentially. In the "Convergence Curve Plot" and "Box Plot" section, the "select box" dropdown menu needs to be selected to get the desire figures. If the whole file is executed properly, a zip file will be downloaded. All the figures and output files will be inside the zip file. After Unzipping, Output file can be found at a directory like this "\EvoloPy\content\EvoloPy\2023-04-13-12-21-16"

`otherwise`

### Run

    pip3 install -r requirements.txt

(possibly with `sudo`)

That command above will install  `sklearn`, `NumPy`, and `SciPy` for you.

- If you are installing EvoloPy Toolbox onto Windows, please Install Anaconda from here https://www.continuum.io/downloads, which is the leading open data science platform powered by Python.
- If you are installing onto Ubuntu or Debian and using Python 3 then this will pull in all the dependencies from the repositories:
  
      sudo apt-get install python3-numpy python3-scipy liblapack-dev libatlas-base-dev libgsl0-dev fftw-dev libglpk-dev libdsdp-dev

### Get the source

Clone the Git repository from GitHub

    git clone https://github.com/7ossam81/EvoloPy.git

### Quick User Guide

EvoloPy toolbox contains twenty three benchamrks (F1-F23). The main file is the optimizer.py, which considered the interface of the toolbox. In the optimizer.py you can setup your experiment by selecting the optmizers, the benchmarks, number of runs, number of iterations, and population size. 
The following is a sample example to use the EvoloPy toolbox.  
Select optimizers from the list of available ones: "SSA","PSO","GA","BAT","FFA","GWO","WOA","MVO","MFO","CS","HHO","SCA","JAYA","DE". For example:
```
optimizer=["PSO", "BAT", "FFA" , "CS" , "WOA"]
```

After that, Select benchmark function from the list of available ones: "F1","F2","F3","F4","F5","F6","F7","F8","F9","F10","F11","F12","F13","F14","F15","F16","F17","F18","F19". For example:
```
objectivefunc=["F1","F5", "F10"] 
```

Select number of repetitions for each experiment. To obtain meaningful statistical results, usually 30 independent runs are executed for each algorithm.  For example:
```
NumOfRuns=30  
```
Select general parameters for all optimizers (population size, number of iterations). For example:
```
params = {'PopulationSize' : 100, 'Iterations' : 50}
```
Choose whether to Export the results in different formats. For example:
```
export_flags = {'Export_avg':True, 'Export_details':True, 'Export_convergence':True, 'Export_boxplot':True}
```





