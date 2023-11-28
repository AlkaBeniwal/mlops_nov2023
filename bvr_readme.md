Create enviroment


```bash
    conda create -n winwq python=3.8 -y
    conda activate wineq

```


Create requirements.rxt
    touch requirements.txt
    pip install -r requirements.txt
```


```

mkdir data_given

copy winequality.csv to data_given folder

``
git init
dvc init
dvc add data_given/winequality.csv
git add .
git commit -m "first commit"
