# Google Earth Engine Python API
Repositório para organizar meus estudos em Google Earth Engine usando a API python.  

## Instalação  
Para melhorar minha organização, tenho usado o [mini conda](https://docs.conda.io/en/latest/miniconda.html), seguindo o processo de instalação mencionado no [GIS Unchained blog post](https://gisunchained.wordpress.com/2019/05/29/using-qgis-from-conda).  
Com as seguintes especificações:  
```
conda create -n earthengine python
conda install -c conda-forge earthengine-api 
```  
No ultimo comando estamos especificando um canal chamado [`earthengine-api`](https://anaconda.org/conda-forge/earthengine-api) com toos os módulos a serem instalados bem como suas dependencias, o que facilita bastante o processo de instalação.  
 
### Autenticação GEE Python API  
Para que as requisições sejam enviadas ao servidor da Google, será necessário criar uma autenticação. Para isso vamos usar o próprio módulo `ee` para iniciar a comunicação e autenticar.
:warning: Se vc ainda não configurou isso, dará erro.  
```
python -c "import ee; ee.Initialize()"
```  

Vamos então autenticar:  
```
earthengine authenticate
```  
Ao executar esse comando o seu browser será aberto e você precisará logar no Google. Tendo sucesso, será informada uma *key* a ser inserida no terminal python, e pronto. Já temos um computador com conexão autenticada.  

#### Checando versão  
```
import ee
print(ee.__version__)
```

### Atualização a instalação de outros módulos python  
Caso necessário, para atualizar os pacotes, ou instalar algum módulo python em específico:  
```
conda update earthengine-api
conda install -c conda-forge Ipython
# ou dentro do env
pip install -U folium, matplotlib
``` 

## Mais informações
https://docs.conda.io/en/latest/miniconda.html  
https://developers.google.com/earth-engine/python_install-conda  
https://www.earthdatascience.org/tutorials/intro-google-earth-engine-python-api/  

## Fontes de estudos:  
### Inicial  
* https://github.com/acgeospatial/GoogleEarthEnginePy  
* https://github.com/renelikestacos/Google-Earth-Engine-Python-Examples  
* https://github.com/tylere/ee-jupyter-examples  
* https://github.com/giswqs/Earth-Engine-Python  
* https://github.com/catherinekuhn/ee-python  
* https://geoscripting-wur.github.io/  

### Sensoriamento Remoto  
* https://github.com/renelikestacos/Google-Earth-Engine-Python-Examples  
* [Geo4Good14](https://github.com/tylere/g4g14-ee-python-api)  
* [
Jupyter notebooks for the Python session of the 2018 Earth Engine User Summit.
](https://github.com/tylere/EEUS2018-JupyterSession)  
* [pygeeltr](https://github.com/fitoprincipe/pygeeltr)  

### Novas ferramentas:  
* https://github.com/fitoprincipe/geebap
* [IpyGEE](https://github.com/fitoprincipe/ipygee)  
* https://github.com/gee-community  
* https://area2.readthedocs.io/en/latest/index.html  

### Cursos:  
* https://philippgaertner.github.io/2019/07/earth-engine-apps-gallery/  
* https://developers.google.com/machine-learning/crash-course/  
https://www.coursera.org/learn/machine-learning?ranMID=40328&ranEAID=je6NUbpObpQ&ranSiteID=je6NUbpObpQ-MCt62nyW6clOEkQssEGtoQ&siteID=je6NUbpObpQ-MCt62nyW6clOEkQssEGtoQ&utm_content=10&utm_medium=partners&utm_source=linkshare&utm_campaign=je6NUbpObpQ*  

# Geo4Good  
* https://medium.com/google-earth/a-new-dimension-in-earth-engine-3c25c89d0ece  
* https://medium.com/@kkrao/new-earth-engine-features-announced-at-geoforgood-summit-2019-57c33ef48bb8  

# Js  
* http://www.gisandbeers.com/scripts-para-google-earth-engine/  