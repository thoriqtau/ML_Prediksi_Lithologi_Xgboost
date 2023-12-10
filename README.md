# Machine Learning Model Menggunakan Model Xgboost Classifier
# Cara Konversi Format .las
## Step 1: Import library
```
import os
import glob
import lasio
import pandas
```
## Step 2: Source Code
```
paths = sorted(glob.glob(os.path.join("Add Path Your File .las", "*.las")))

well_df = [0]*4
for i in range(len(paths)):
  well = lasio.read(paths[i])
  df = well.df()
  well_df[i] = df.reset_index()
well1, well2, well3, well4 = well_df
```
- Jangan lupa mengubah link path sesuaikan dengan lokasi file di komputer anda
