# ANN Regression with tensorflow on Render.com

# Demo
- call: https://linreg-3yev.onrender.com
Enter: 998 for feature1 and 1000 for feature2, check result: 425.12085

# Jupyter Notebook is used only with python 3.7.7 intel mac legacy

# installation
- `conda create --name tensorflow377 python=3.7.7`
- `conda info --envs`
- `conda activate tensorflow377`
- `conda install ipykernel`
- `python -m ipykernel install --user --name tensorflow377 --display-name "Python 3.7.7 (tensorflow)"`

# installation local of Jupyter Notebook
- `conda deactivate`
- `conda uninstall -y jupyter`

 # (Use pip if using legacy Python 2.)  locally on intel mac
- `conda activate tensorflow377`
- `pip3 install --upgrade pip`
- `pip3 install jupyter`
- `pip install notebook --upgrade`
- `pip install Jinja2==3.0.3`
- `pip install MarkupSafe==2.0.0`
- `pip install zipp==3.1.0`
- `pip3 install chardet`
- `conda install -c anaconda importlib-metadata`


- `conda activate tensorflow377`
- `conda install -y pandas`
- `conda install -y seaborn`
- `conda install -y matplotlib`
- `conda install -y tensorflow`
- run notebook: `jupyter notebook`

# on render.com
- Choose free plan 0$ and type: webservice

# buildsetting on render.com
- `pip install --upgrade pip && pip install -r requirements.txt`

# start command set
- `python app.py`

# under Environment set
- PYTHON_VERSION => 3.7.7
- PORT => 5000

# save requiremenrts.txt locally on intel mac
- `pip freeze > requirements.txt`

# scaler
```
import pickle
scalerfile = 'scaler.sav'
pickle.dump(scaler, open(scalerfile, 'wb'))
new_gem = scaler.transform(new_gem)

# use the scaler
scaler = pickle.load(open('scaler.sav', 'rb'))
new_gem2 = [[feat1,feat2]]
new_gem2 = scaler.transform(new_gem2)
predict=model.predict(new_gem2) 
```