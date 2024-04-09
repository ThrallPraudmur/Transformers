### Настройка собственного окружения в Anaconda Promt
```python
conda create --name your_name python=3.12
conda activate your_name
conda install python jupyter numpy pandas
conda install -n your_name --use-local название файла + расширение
conda remove -n your_name --all
```

### Содержимое файла .condarc
```python
channels:
- conda-forge
- defaults
proxy_servers:
  https:
  http:
restore_free_channel: True
ssl_verify: False
channel_priority: disabled
auto_update_conda: False
channels:
  - C:\Python39\Lib\site-packages
```

### Подключение pyodbc
```python
import pyodbc

cnxn = pyodbc.connect(
  driver = '{SQL Server}',
  server = 'wrp-sandbox-db',
  database = 'WHBA',
  username = 'username',
  password = 'password',
  trusted_connection = 'yes',
  autocommit = True)

cursor = cnxn.cursor()

zap = '''

'''
result = pd.read_sql_query(zap, cnxn)
display(result.head())

cursor.close()
cnxn.close()
```
