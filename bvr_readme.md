Create enviroment


```bash
    conda create -n winwq python=3.8 -y
    conda activate wineq

```


Create requirements.txt

```

touch requirements.txt

dvc
dvc[gdrive]
scikit-learn

pip install -r requirements.txt


```
python template.py

```

dpwnload winequality.csv from 
https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing 

mkdir data_given

copy winequality.csv to data_given folder

``
git init
dvc init
dvc add data_given/winequality.csv
git add .
git commit -m "first commit"

```

```

```
 6377  git commit -m "updated read me file"
 6378  git remote add origin https://github.com/AlkaBeniwal/mlops_nov2023.git
 6q379  git push -u origin main


 ```

 ```
 update params.yaml

 git add . && git commit -m "added params.yaml"
 git push -u origin main
 ```

 ```
create get_data.py
create load_data.py

```

update dvc.yaml

stages :
  load_data :
    cmd : python src/load_data.py --config=params.yaml
    deps :
      - src/get_data.py
      - src/load_data.py
      - data_given/winequality.csv
    outs :
      - data/raw/winequality.csv


dvc
dvc[gdrive]
scikit-learn

```get


```
pip install requirements.txt
```

```
If require run independant programs
python get_data.py ( make sure you remove commented syntax in the program to see result)
Note: if you run load_data.py it will create target.csv file in case dvc command will fail
so delete generated files before running below command

dvc repro
```


