# Spotify Top 50 – Globális Zenei Trendanalízis és Népszerűség Predikció

- Készítette: **Kovács Krisztián**

- Neptun Kód: **HRHA5F**

- Szak: **Mérnök Informatika**

- Kurzus: **Mesterséges Intelligencia**

  


Ez a projekt a Spotify Top 50 dalok zenei jellemzőit elemzi és gépi tanulási modellekkel megpróbálja előre jelezni a dalok népszerűségét.

Az elemzés Python és Jupyter Notebook segítségével készült, és a **CRISP-DM módszertant** követi.

A notebook:

- feltáró adatelemzést végez
- statisztikai összefüggéseket vizsgál
- vizualizációkat készít
- több regressziós modellt hasonlít össze

---

# Módszertani keretrendszer: **CRISP-DM**


1. Business understanding – projektcél meghatározása  
2. Data understanding – adatok feltérképezése  
3. Data preparation – adattisztítás és feature engineering  
4. Exploratory Data Analysis – mintázatok és korrelációk keresése  
5. Modeling – prediktív modellek építése  
6. Evaluation – modellek összehasonlítása  
7. Insights – következtetések levonása  

---

# Technológiai stack

A projekt az alábbi Python könyvtárakat használja:

- Python
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn
- kagglehub

---

# Projekt struktúra


spotify_analizis/
│

├── spotify_analizis.ipynb

├── requirements.txt

├── README.md

├── .gitignore

└── .gitattributes


---

# Adatforrás

A projekt a Spotify Top 50 dalok zenei jellemzőit tartalmazó adathalmazt használja.

Dataset:


**miquelneck/worlds-spotify-top-50-playlist-musicality-data**


A dataset többek között az alábbi jellemzőket tartalmazza:

- danceability
- energy
- loudness
- speechiness
- acousticness
- instrumentalness
- valence
- tempo
- popularity

---

# Adatbetöltés működése

A notebook automatikusan kezeli az adatok letöltését.

Az adatbetöltés logikája:

1. megpróbál helyi CSV fájlt találni
2. ha nincs, letölti a Kaggle datasetet
3. elmenti az `Adatok` mappába
4. onnan tölti be a pandas dataframe-et

A notebook több lehetséges fájlnevet is keres:


Adatok/Top-50-musicality-global.csv
Top-50-musicality-global.csv
spotify.csv
spotify_tracks.csv
dataset.csv


Ha egyik sincs jelen, akkor automatikusan letölti a Kaggle datasetet.

---

# Telepítés

A projekt futtatásához **Python 3.8 vagy újabb** szükséges.

Python verzió ellenőrzése:

```bash
python --version

vagy

python3 --version

Repository klónozása:

git clone https://github.com/kristian10036/spotify_project.git
cd spotify_project

Függőségek telepítése:

Virtuális környezet használata (ajánlott)

Windows:
(CMD)
python -m venv venv
venv\Scripts\activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt

Linux / macOS:

python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt

Telepítés virtuális környezet nélkül:

pip install --upgrade pip
pip install -r requirements.txt

Ha nincs requirements fájl:

pip install numpy pandas matplotlib seaborn scikit-learn scipy jupyter kagglehub

Notebook futtatása:

Indítsd el a Jupyter Notebookot:

python -m notebook

Ezután nyisd meg:

spotify_analizis.ipynb

Majd futtasd a notebook celláit sorrendben.

Feltáró adatelemzés

A notebook több vizsgálatot végez:

popularity eloszlása

zenei jellemzők eloszlása

numerikus változók korrelációja

popularity és zenei jellemzők kapcsolata

műfaj szerinti különbségek

szezonális mintázatok

Vizualizációk:

hisztogram

boxplot

scatter plot

correlation heatmap

Prediktív modellezés

A projekt több regressziós modellt hasonlít össze.

Használt modellek:

Linear Regression

Ridge Regression

Lasso Regression

Random Forest Regressor

Gradient Boosting Regressor

A modellek értékelése az alábbi metrikákkal történik:

MSE

RMSE

MAE

R²

cross-validation

Feature kiválasztás

A notebook a legfontosabb zenei jellemzőket is meghatározza.

Használt módszer:

SelectKBest

Ez rangsorolja a változókat a popularity predikció szempontjából.

Országonkénti népszerűségi tényezők

A notebook képes országonként elemezni, hogy mely zenei jellemzők befolyásolják leginkább a népszerűséget.

Az elemzés:

országonkénti átlagokat számol

korrelációkat vizsgál

meghatározza a domináns tényezőket

vizualizációkat készít

Eredmények

A notebook végén összefoglalás készül:

legjobb prediktív modell

legfontosabb jellemzők

főbb korrelációk

országonkénti trendek

Továbbfejlesztési lehetőségek

A projekt később tovább bővíthető például:

dalszöveg elemzéssel (NLP)

időbeli trendmodellezéssel

előadói ismertségi mutatókkal

deep learning modellekkel

több ország adatainak integrálásával






