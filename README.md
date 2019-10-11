# KeplerGL Kepler.GL

My solution how to install keplergl==0.1.1 (and may be other versions too) and use it into Jupyter (https://github.com/keplergl/kepler.gl)

My current system config:
Windows 10 Pro x64. Python 3.7.3 x64
Anaconda 1.9.7 x64/Notebook 6.0.1/JupyterLab 1.1.4

1. pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org --user numpy bottleneck pandas shapely wheel munch cligj click-plugins pyproj pyparsing matplotlib kiwisolver cycler ply
2. U should install Generic installer for the GDAL core components https://www.gisinternals.com/query.html?content=filelist&file=release-1911-x64-gdal-3-0-0-mapserver-7-4-0.zip
then install GDAL 2.4.1 (coz GDAL 3.x.x dose not support Fiona) & Fiona 1.8.6 from whl packages
https://www.lfd.uci.edu/~gohlke/pythonlibs/#fiona
https://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal
python -m pip install c:\GDAL-2.4.1-cp37-cp37m-win_amd64.whl
python -m pip install c:\Fiona-1.8.6-cp37-cp37m-win_amd64.whl
3. pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org geopandas
4. pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org keplergl
5. Be shure that keplergl extension is installed and enabled into Jupyter
  5.1 jupyter nbextension install --py --sys-prefix keplergl # can be skipped for notebook 5.3 and above
  5.2 jupyter nbextension enable --py --sys-prefix keplergl # can be skipped for notebook 5.3 and above
#Optional:
6. Install NodeJs from Anaconda Navigator
7. Install "jupyter labextension install @jupyter-widgets/jupyterlab-manager keplergl-jupyter"
8. pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org --upgrade jupyterthemes
