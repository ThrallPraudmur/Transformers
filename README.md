### Настройка собственного окружения в Anaconda Promt
```python
conda create --name your_name
conda activate your_name
conda install python jupyter numpy pandas
conda install -n your_name --use-local название файла + расширение
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
