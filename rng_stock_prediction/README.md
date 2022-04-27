# Random Walk for stock price prediction using true Random Numbers

Provided are 2 Jupyter notebooks demonstrating how to generate random numbers and how to further process them, as well as the underlying source code wrapped by the PlanQK user code template within `src`.  
`rng_local.ipynb` is a self consistent notebook which includes the main logic of `src/program.py`.  
`rng_platform.ipynb` is basically a copy of the the former notebook except that it includes the necessary steps for communicating with services on the platform and retrieving results from them. It was created with an already existing service and application, which is to be replaced by your own.  
In order to do this, follow the steps described in [this](https://docs.platform.planqk.de/en/latest/platform_instructions/service_platform.html#deploy-services-on-the-planqk-platform) tutorial using `user_code.zip` (which ist just the already zipped version of the `src` repo).  
If you successfully deployed the service, you should publish it internally and subscribe to it from within a (new or existing) application. By doing so, you should be able to follow the steps within `rng_platform.ipynb` and be able to execute the service from within the notebook.

## Executing Jupyter notebooks
We recommend working with a separate Python environment, e.g. via [conda](https://www.anaconda.com/products/distribution) by running
```
conda create --name=planqk python=3.9
conda activate planqk
```
While being in this repository, run
```
pip install -r requirements.txt
```
to install the packages necessary for running the notebooks and the service. For running the notebook from within jupyter lab, we refer to the authors and recommend to install it via a conda channel:
```
conda install -c conda-forge jupyter-lab
```
After installation, simply run 
```
jupyter lab <noteboook-name>.ipynb
```
in order to run the notebook. Both notebooks should work by executing cell after cell.