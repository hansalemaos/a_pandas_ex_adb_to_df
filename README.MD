# Use the power of pandas to manage the files on your Android device

```python
pip install a-pandas-ex-adb-to-df
```

```python
#first way
from a_pandas_ex_adb_to_df import pd_add_adb_to_df, connect_to_adb
import pandas as pd
pd_add_adb_to_df()
device = connect_to_adb(
    serialnumber="XXXXXXXXXXXXXXXXXXXXXX", adb_path=r"C:\ProgramData\adb\adb.exe"
)
df = pd.Q_adb_to_df(device=device)

#second way
from a_pandas_ex_adb_to_df import pd_add_adb_to_df
import pandas as pd
pd_add_adb_to_df()
df = pd.Q_adb_to_df(device="XXXXXXXXXXXXXXXXXXXXXX", adb_path=r"C:\ProgramData\adb\adb.exe")


print(df.loc[df.aa_fullpath.str.contains(r'download.*_.*\.mp4',na=False,regex=True, flags=re.IGNORECASE)][:5].to_string())

                                          aa_filename                    aa_folder                                                                aa_fullpath   aa_id  aa_index   aa_rights  aa_links aa_owner  aa_group  aa_size             aa_date
634994                               von_haus_aus.mp4  storage/emulated/0/Download                               storage/emulated/0/Download/von_haus_aus.mp4  140306      5428  -rwxrwx---         1  u0_a219  media_rw  5552768 2022-03-21 17:31:00
634995                            ins_haus_stehen.mp4  storage/emulated/0/Download                            storage/emulated/0/Download/ins_haus_stehen.mp4  186233      6328  -rwxrwx---         1  u0_a219  media_rw  6471958 2022-03-21 17:31:00
634996                            aufs_haus_gehen.mp4  storage/emulated/0/Download                            storage/emulated/0/Download/aufs_haus_gehen.mp4  126498      6588  -rwxrwx---         1  u0_a219  media_rw  6738374 2022-03-21 17:31:00
634997               mit_der_tuer_ins_haus_fallen.mp4  storage/emulated/0/Download               storage/emulated/0/Download/mit_der_tuer_ins_haus_fallen.mp4  130773      6832  -rwxrwx---         1  u0_a219  media_rw  6989353 2022-03-21 17:31:00
635004  Alfredo_stiftete_seinen_Lieferwagen_final.mp4  storage/emulated/0/Download  storage/emulated/0/Download/Alfredo_stiftete_seinen_Lieferwagen_final.mp4  136706      5104  -rw-rw----         1  u0_a219  media_rw  5219973 2022-06-01 22:58:00



```