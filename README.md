# Briefing
This is a [Python notebook](https://github.com/CopernicusMarineInsitu/downloadFilesFromCSV/blob/master/downloadFilesFromCSV.ipynb) that illustrates how to download files from a CSV containing the ftp links/paths to the desired In Situ files. This CSV file can be generated manually trough the Dashboard (see below GIF) or by processing the index files available in a given In Situ product/dataset.

![](dashboardExport.gif)

## Packages
```python
import pandas as pd
import os
import ftputil
from urllib.parse import urlparse
```

## Usage
```bash
downloadFilesFromCSV(user,pasword,path2csv,column_name,output_dir)
```
where:
- **user** and **password** are the Copernicus Marine Service credentials for accessing the FTP server where data is hosted
- **path2csv** is the path to the CSV containing as many rows as files to be downloaded
- **column_name** is the name of the column in the CSV file containing the FTP path or link of each file
- **output_dir** is the path to the directory in your machine you want the files downloaded to endup in.