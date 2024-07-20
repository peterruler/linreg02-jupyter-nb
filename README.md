Demo: https://linreg.onrender.com
# installation
- `conda create --name tensorflow377 python=3.7.7`
- `conda info --envs`
- `conda activate tensorflow377`
- `conda install ipykernel`
- `python -m ipykernel install --user --name tensorflow377 --display-name "Python 3.7.7 (tensorflow)"`
# installation local for Jupyter Notebook
- `conda deactivate`
- `conda uninstall -y jupyter`

 # (Use pip if using legacy Python 2.)
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
# build 
- `pip install -r requirements.txt`

# save requiremenrts.txt
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