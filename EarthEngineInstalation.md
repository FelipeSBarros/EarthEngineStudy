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
