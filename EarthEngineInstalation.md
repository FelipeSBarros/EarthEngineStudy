#https://docs.conda.io/en/latest/miniconda.html
#https://anaconda.org/conda-forge/earthengine-api
# https://developers.google.com/earth-engine/python_install-conda
conda create -n earthengine python
conda install -c conda-forge earthengine-api 
 python -c "import ee; ee.Initialize()"
 earthengine authenticate

conda update earthengine-api
conda install -c conda-forge Ipython


import ee
print(ee.__version__)

OU
https://www.earthdatascience.org/tutorials/intro-google-earth-engine-python-api/




pip install -U folium, matplotlib

