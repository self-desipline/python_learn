```python

```


      Input In [1]
        type(‪C:\Users\LYR13\Desktop\666.txt)
             ^
    SyntaxError: invalid non-printable character U+202A
    



```python
!type examples/ex1.csv
```

    命令语法不正确。
    


```python
import pands as pd
```


    ---------------------------------------------------------------------------

    ModuleNotFoundError                       Traceback (most recent call last)

    Input In [3], in <cell line: 1>()
    ----> 1 import pands as pd
    

    ModuleNotFoundError: No module named 'pands'



```python
import pandas as pd
```


```python
pd.options.display.max_rows = 10
```


```python
result = pd.read_csv('D:\DownLoad\BaiDuWangPanDownload\新建文本文档.csv')
```


```python
result
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one       two     three      four key</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0     0.467976 -0.038649 -0.295344 -1.824726   L</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1    -0.358893  1.404453  0.704965 -0.200638   B</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2    -0.501840  0.659254 -0.421691 -0.057688   G</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3     0.204886  1.074134  1.388361 -0.982404   R</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4     0.354628 -0.133116  0.283763 -0.837063   Q</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>9996 -0.479893 -0.650419  0.745152 -0.646038   E</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9997  0.523331  0.787112  0.486066  1.093156   K</td>
    </tr>
    <tr>
      <th>9</th>
      <td>9998 -0.362559  0.598894 -1.843201  0.887292   G</td>
    </tr>
    <tr>
      <th>10</th>
      <td>9999 -0.096376 -1.012999 -0.657431 -0.573315   0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[10000 rows x 5 columns]</td>
    </tr>
  </tbody>
</table>
<p>12 rows × 1 columns</p>
</div>




```python
pd.read_csv('D:\DownLoad\BaiDuWangPanDownload\新建文本文档.csv',nrows=5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one       two     three      four key</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0     0.467976 -0.038649 -0.295344 -1.824726   L</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1    -0.358893  1.404453  0.704965 -0.200638   B</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2    -0.501840  0.659254 -0.421691 -0.057688   G</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3     0.204886  1.074134  1.388361 -0.982404   R</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4     0.354628 -0.133116  0.283763 -0.837063   Q</td>
    </tr>
  </tbody>
</table>
</div>




```python
chunker = pd.read_csv('D:\DownLoad\BaiDuWangPanDownload\新建文本文档.csv',chunksize=1000)
```


```python
chunker
```




    <pandas.io.parsers.readers.TextFileReader at 0x22c92cd4a60>




```python
with open('mydata.csv', 'w') as f:
    writer = csv.writer(f, dialect=my_dialect)
    writer.writerow(('one', 'two', 'three'))
    writer.writerow(('1', '2', '3'))
    writer.writerow(('4', '5', '6'))
    writer.writerow(('7', '8', '9'))    
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [13], in <cell line: 1>()
          1 with open('mydata.csv', 'w') as f:
    ----> 2     writer = csv.writer(f, dialect=my_dialect)
          3     writer.writerow(('one', 'two', 'three'))
          4     writer.writerow(('1', '2', '3'))
    

    NameError: name 'csv' is not defined



```python
import json
```


```python
result = json.loads(obj)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [15], in <cell line: 1>()
    ----> 1 result = json.loads(obj)
    

    NameError: name 'obj' is not defined



```python
result = {'name': 'Wes',
 'pet': None,
 'places_lived': ['United States', 'Spain', 'Germany'],
 'siblings': [{'age': 30, 'name': 'Scott', 'pets': ['Zeus', 'Zuko']},
  {'age': 38, 'name': 'Katie', 'pets': ['Sixes', 'Stache', 'Cisco']}]}
```


```python
result
```




    {'name': 'Wes',
     'pet': None,
     'places_lived': ['United States', 'Spain', 'Germany'],
     'siblings': [{'age': 30, 'name': 'Scott', 'pets': ['Zeus', 'Zuko']},
      {'age': 38, 'name': 'Katie', 'pets': ['Sixes', 'Stache', 'Cisco']}]}




```python
asjson = json.dumps(result)
```


```python
asjson
```




    '{"name": "Wes", "pet": null, "places_lived": ["United States", "Spain", "Germany"], "siblings": [{"age": 30, "name": "Scott", "pets": ["Zeus", "Zuko"]}, {"age": 38, "name": "Katie", "pets": ["Sixes", "Stache", "Cisco"]}]}'




```python
siblings = pd.DataFrame(result['siblings'], columns=['name', 'age'])

```


```python
siblings
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Scott</td>
      <td>30</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Katie</td>
      <td>38</td>
    </tr>
  </tbody>
</table>
</div>




```python
conda install lxml
```

    Solving environment: ...working... done
    
    ## Package Plan ##
    
      environment location: D:\Anaconda3\envs\pytorch
    
      added / updated specs: 
        - lxml
    
    
    The following packages will be downloaded:
    
        package                    |            build
        ---------------------------|-----------------
        certifi-2022.9.14          |  py310haa95532_0         159 KB  defaults
        libiconv-1.16              |       h2bbff1b_2         713 KB  defaults
        lxml-4.9.1                 |  py310h1985fb9_0         1.0 MB  defaults
        libxml2-2.9.14             |       h0ad7f3c_0         3.4 MB  defaults
        libxslt-1.1.35             |       h2bbff1b_0         512 KB  defaults
        ------------------------------------------------------------
                                               Total:         5.8 MB
    
    The following NEW packages will be INSTALLED:
    
        libiconv: 1.16-h2bbff1b_2           defaults
        libxml2:  2.9.14-h0ad7f3c_0         defaults
        libxslt:  1.1.35-h2bbff1b_0         defaults
        lxml:     4.9.1-py310h1985fb9_0     defaults
    
    The following packages will be UPDATED:
    
        certifi:  2022.6.15-py310haa95532_0 defaults --> 2022.9.14-py310haa95532_0 defaults
    
    
    Downloading and Extracting Packages
    Preparing transaction: ...working... done
    Verifying transaction: ...working... done
    Executing transaction: ...working... done
    
    Note: you may need to restart the kernel to use updated packages.
    

    
    
    ==> WARNING: A newer version of conda exists. <==
      current version: 4.5.11
      latest version: 22.9.0
    
    Please update conda by running
    
        $ conda update -n base -c defaults conda
    
    
    
    certifi-2022.9.14    | 159 KB    |            |   0% 
    certifi-2022.9.14    | 159 KB    | 7          |   8% 
    certifi-2022.9.14    | 159 KB    | ###        |  30% 
    certifi-2022.9.14    | 159 KB    | ######     |  60% 
    certifi-2022.9.14    | 159 KB    | ########## | 100% 
    
    libiconv-1.16        | 713 KB    |            |   0% 
    libiconv-1.16        | 713 KB    | 1          |   2% 
    libiconv-1.16        | 713 KB    | 3          |   3% 
    libiconv-1.16        | 713 KB    | #5         |  15% 
    libiconv-1.16        | 713 KB    | ###3       |  34% 
    libiconv-1.16        | 713 KB    | ####8      |  49% 
    libiconv-1.16        | 713 KB    | #####3     |  54% 
    libiconv-1.16        | 713 KB    | #####8     |  59% 
    libiconv-1.16        | 713 KB    | ######3    |  64% 
    libiconv-1.16        | 713 KB    | ######8    |  69% 
    libiconv-1.16        | 713 KB    | #######4   |  74% 
    libiconv-1.16        | 713 KB    | ########## | 100% 
    
    lxml-4.9.1           | 1.0 MB    |            |   0% 
    lxml-4.9.1           | 1.0 MB    | 1          |   1% 
    lxml-4.9.1           | 1.0 MB    | 4          |   5% 
    lxml-4.9.1           | 1.0 MB    | 7          |   8% 
    lxml-4.9.1           | 1.0 MB    | #1         |  11% 
    lxml-4.9.1           | 1.0 MB    | #3         |  14% 
    lxml-4.9.1           | 1.0 MB    | #7         |  17% 
    lxml-4.9.1           | 1.0 MB    | ###        |  31% 
    lxml-4.9.1           | 1.0 MB    | ###5       |  35% 
    lxml-4.9.1           | 1.0 MB    | ###8       |  39% 
    lxml-4.9.1           | 1.0 MB    | ####7      |  48% 
    lxml-4.9.1           | 1.0 MB    | #####2     |  52% 
    lxml-4.9.1           | 1.0 MB    | #######    |  70% 
    lxml-4.9.1           | 1.0 MB    | #######6   |  77% 
    lxml-4.9.1           | 1.0 MB    | #########  |  91% 
    lxml-4.9.1           | 1.0 MB    | ########## | 100% 
    
    libxml2-2.9.14       | 3.4 MB    |            |   0% 
    libxml2-2.9.14       | 3.4 MB    |            |   0% 
    libxml2-2.9.14       | 3.4 MB    | 2          |   3% 
    libxml2-2.9.14       | 3.4 MB    | 3          |   4% 
    libxml2-2.9.14       | 3.4 MB    | 5          |   5% 
    libxml2-2.9.14       | 3.4 MB    | 8          |   9% 
    libxml2-2.9.14       | 3.4 MB    | #          |  10% 
    libxml2-2.9.14       | 3.4 MB    | #1         |  12% 
    libxml2-2.9.14       | 3.4 MB    | #2         |  13% 
    libxml2-2.9.14       | 3.4 MB    | #3         |  14% 
    libxml2-2.9.14       | 3.4 MB    | #4         |  15% 
    libxml2-2.9.14       | 3.4 MB    | #8         |  18% 
    libxml2-2.9.14       | 3.4 MB    | #9         |  19% 
    libxml2-2.9.14       | 3.4 MB    | ##1        |  21% 
    libxml2-2.9.14       | 3.4 MB    | ##2        |  22% 
    libxml2-2.9.14       | 3.4 MB    | ##3        |  24% 
    libxml2-2.9.14       | 3.4 MB    | ##4        |  25% 
    libxml2-2.9.14       | 3.4 MB    | ##5        |  26% 
    libxml2-2.9.14       | 3.4 MB    | ##6        |  27% 
    libxml2-2.9.14       | 3.4 MB    | ##7        |  28% 
    libxml2-2.9.14       | 3.4 MB    | ##8        |  29% 
    libxml2-2.9.14       | 3.4 MB    | ###        |  30% 
    libxml2-2.9.14       | 3.4 MB    | ###1       |  31% 
    libxml2-2.9.14       | 3.4 MB    | ###3       |  33% 
    libxml2-2.9.14       | 3.4 MB    | ###5       |  35% 
    libxml2-2.9.14       | 3.4 MB    | ###8       |  39% 
    libxml2-2.9.14       | 3.4 MB    | ####       |  40% 
    libxml2-2.9.14       | 3.4 MB    | ####1      |  42% 
    libxml2-2.9.14       | 3.4 MB    | ####2      |  43% 
    libxml2-2.9.14       | 3.4 MB    | ####4      |  44% 
    libxml2-2.9.14       | 3.4 MB    | ####5      |  46% 
    libxml2-2.9.14       | 3.4 MB    | ####7      |  47% 
    libxml2-2.9.14       | 3.4 MB    | ####8      |  48% 
    libxml2-2.9.14       | 3.4 MB    | #####1     |  51% 
    libxml2-2.9.14       | 3.4 MB    | #####2     |  53% 
    libxml2-2.9.14       | 3.4 MB    | #####6     |  56% 
    libxml2-2.9.14       | 3.4 MB    | #####8     |  58% 
    libxml2-2.9.14       | 3.4 MB    | #####9     |  60% 
    libxml2-2.9.14       | 3.4 MB    | ######1    |  61% 
    libxml2-2.9.14       | 3.4 MB    | ######5    |  66% 
    libxml2-2.9.14       | 3.4 MB    | ######7    |  68% 
    libxml2-2.9.14       | 3.4 MB    | #######1   |  71% 
    libxml2-2.9.14       | 3.4 MB    | #######3   |  73% 
    libxml2-2.9.14       | 3.4 MB    | #######4   |  75% 
    libxml2-2.9.14       | 3.4 MB    | #######6   |  76% 
    libxml2-2.9.14       | 3.4 MB    | ########1  |  82% 
    libxml2-2.9.14       | 3.4 MB    | ########8  |  88% 
    libxml2-2.9.14       | 3.4 MB    | #########4 |  95% 
    libxml2-2.9.14       | 3.4 MB    | ########## | 100% 
    
    libxslt-1.1.35       | 512 KB    |            |   0% 
    libxslt-1.1.35       | 512 KB    | 2          |   2% 
    libxslt-1.1.35       | 512 KB    | 9          |   9% 
    libxslt-1.1.35       | 512 KB    | #8         |  19% 
    libxslt-1.1.35       | 512 KB    | ###7       |  37% 
    libxslt-1.1.35       | 512 KB    | ####4      |  45% 
    libxslt-1.1.35       | 512 KB    | #####3     |  54% 
    libxslt-1.1.35       | 512 KB    | ########## | 100% 
    


```python
pip install beautifulsoup4 html5lib
```

    Requirement already satisfied: beautifulsoup4 in d:\anaconda3\envs\pytorch\lib\site-packages (4.11.1)
    Collecting html5lib
      Downloading html5lib-1.1-py2.py3-none-any.whl (112 kB)
         ------------------------------------ 112.2/112.2 kB 362.8 kB/s eta 0:00:00
    Requirement already satisfied: soupsieve>1.2 in d:\anaconda3\envs\pytorch\lib\site-packages (from beautifulsoup4) (2.3.1)
    Requirement already satisfied: webencodings in d:\anaconda3\envs\pytorch\lib\site-packages (from html5lib) (0.5.1)
    Requirement already satisfied: six>=1.9 in d:\anaconda3\envs\pytorch\lib\site-packages (from html5lib) (1.16.0)
    Installing collected packages: html5lib
    Successfully installed html5lib-1.1
    Note: you may need to restart the kernel to use updated packages.
    


```python
 tables = pd.read_html('examples/fdic_failed_bank_list.html')
```

    D:\Anaconda3\envs\pytorch\lib\site-packages\bs4\__init__.py:435: MarkupResemblesLocatorWarning: The input looks more like a filename than markup. You may want to open this file and pass the filehandle into Beautiful Soup.
      warnings.warn(
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Input In [24], in <cell line: 1>()
    ----> 1 tables = pd.read_html('examples/fdic_failed_bank_list.html')
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\util\_decorators.py:311, in deprecate_nonkeyword_arguments.<locals>.decorate.<locals>.wrapper(*args, **kwargs)
        305 if len(args) > num_allow_args:
        306     warnings.warn(
        307         msg.format(arguments=arguments),
        308         FutureWarning,
        309         stacklevel=stacklevel,
        310     )
    --> 311 return func(*args, **kwargs)
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\io\html.py:1113, in read_html(io, match, flavor, header, index_col, skiprows, attrs, parse_dates, thousands, encoding, decimal, converters, na_values, keep_default_na, displayed_only)
       1109 validate_header_arg(header)
       1111 io = stringify_path(io)
    -> 1113 return _parse(
       1114     flavor=flavor,
       1115     io=io,
       1116     match=match,
       1117     header=header,
       1118     index_col=index_col,
       1119     skiprows=skiprows,
       1120     parse_dates=parse_dates,
       1121     thousands=thousands,
       1122     attrs=attrs,
       1123     encoding=encoding,
       1124     decimal=decimal,
       1125     converters=converters,
       1126     na_values=na_values,
       1127     keep_default_na=keep_default_na,
       1128     displayed_only=displayed_only,
       1129 )
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\io\html.py:939, in _parse(flavor, io, match, attrs, encoding, displayed_only, **kwargs)
        937 else:
        938     assert retained is not None  # for mypy
    --> 939     raise retained
        941 ret = []
        942 for table in tables:
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\io\html.py:919, in _parse(flavor, io, match, attrs, encoding, displayed_only, **kwargs)
        916 p = parser(io, compiled_match, attrs, encoding, displayed_only)
        918 try:
    --> 919     tables = p.parse_tables()
        920 except ValueError as caught:
        921     # if `io` is an io-like object, check if it's seekable
        922     # and try to rewind it before trying the next parser
        923     if hasattr(io, "seekable") and io.seekable():
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\io\html.py:239, in _HtmlFrameParser.parse_tables(self)
        231 def parse_tables(self):
        232     """
        233     Parse and return all tables from the DOM.
        234 
       (...)
        237     list of parsed (header, body, footer) tuples from tables.
        238     """
    --> 239     tables = self._parse_tables(self._build_doc(), self.match, self.attrs)
        240     return (self._parse_thead_tbody_tfoot(table) for table in tables)
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\io\html.py:569, in _BeautifulSoupHtml5LibFrameParser._parse_tables(self, doc, match, attrs)
        566 tables = doc.find_all(element_name, attrs=attrs)
        568 if not tables:
    --> 569     raise ValueError("No tables found")
        571 result = []
        572 unique_tables = set()
    

    ValueError: No tables found



```python
len(tables)
```


```python
1
```


```python
failures = tables[0]
```


```python
failures.head()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [25], in <cell line: 1>()
    ----> 1 failures.head()
    

    NameError: name 'failures' is not defined



```python
from lxml import objectify
```


```python
string_data = pd.Series(['aardvark', 'artichoke', np.nan, 'avocado'])
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [27], in <cell line: 1>()
    ----> 1 string_data = pd.Series(['aardvark', 'artichoke', np.nan, 'avocado'])
    

    NameError: name 'np' is not defined



```python
import numpy as np
```


```python
string_data = pd.Series(['aardvark', 'artichoke', np.nan, 'avocado'])
```


```python
string_data
```




    0     aardvark
    1    artichoke
    2          NaN
    3      avocado
    dtype: object




```python
string_data.isnull()
```




    0    False
    1    False
    2     True
    3    False
    dtype: bool




```python
string_data[0] = None
```


```python
string_data
```




    0         None
    1    artichoke
    2          NaN
    3      avocado
    dtype: object




```python
string_data.isnull()
```




    0     True
    1    False
    2     True
    3    False
    dtype: bool




```python
string_data.notnull()
```




    0    False
    1     True
    2    False
    3     True
    dtype: bool




```python
from numpy import nan as NA
```


```python
data = pd.Series([1, NA, 3.5, NA, 7])
```


```python
data
```




    0    1.0
    1    NaN
    2    3.5
    3    NaN
    4    7.0
    dtype: float64




```python
data.dropna()
```




    0    1.0
    2    3.5
    4    7.0
    dtype: float64




```python
data[data.notnull()]
```




    0    1.0
    2    3.5
    4    7.0
    dtype: float64




```python
data
```




    0    1.0
    1    NaN
    2    3.5
    3    NaN
    4    7.0
    dtype: float64




```python
data = pd.DataFrame([[1., 6.5, 3.], [1., NA, NA],
   ....:                      [NA, NA, NA], [NA, 6.5, 3.]])
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
cleaned = data.dropna()
```


```python
cleaned
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.dropna(how='all')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data[4] = NA
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.dropna(axis=1,how='all')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.dropna(how='all')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.dropna(axis=1,how='all')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.dropna(how='all',axis=1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>6.5</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data[4,axis=0] = NA
```


      Input In [57]
        data[4,axis=0] = NA
               ^
    SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
    



```python

```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [58], in <cell line: 1>()
    ----> 1 data[4,axis==0] = NA
    

    NameError: name 'axis' is not defined



```python
df = pd.DataFrame(np.random.randn(7, 3))
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>-0.952629</td>
      <td>0.221395</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>-1.733650</td>
      <td>-0.436068</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>-0.103175</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>-0.240706</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.iloc[:4,1] = NA
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>0.221395</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>-0.436068</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.iloc[:2,2] = NA
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=4)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=4)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.dropna(thresh=3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.fillna(0)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>0.000000</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>0.000000</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.fillna({1:9,2:8})
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>9.000000</td>
      <td>8.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>9.000000</td>
      <td>8.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>9.000000</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>9.000000</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>NaN</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>NaN</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
_ = df.fillna(0, inplace=True)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>0.000000</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>0.000000</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.451988</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.427007</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.827662</td>
      <td>0.000000</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.401042</td>
      <td>0.000000</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.096760</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.283095</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-1.701024</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
df[0] = NA
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>NaN</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>0.000000</td>
      <td>1.274000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>0.000000</td>
      <td>-0.599811</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>0.447152</td>
      <td>1.217018</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NaN</td>
      <td>2.936495</td>
      <td>-0.338795</td>
    </tr>
    <tr>
      <th>6</th>
      <td>NaN</td>
      <td>0.123040</td>
      <td>0.846300</td>
    </tr>
  </tbody>
</table>
</div>




```python
_ = df.dropna(inplace = True)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df = pd.DataFrame(np.random.randn(6,3))
```


```python
df.iloc[2:,1] = NA
```


```python
df.iloc[4:,2] = NA
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-1.540472</td>
      <td>-1.907663</td>
      <td>0.245070</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.203660</td>
      <td>0.087430</td>
      <td>-0.158976</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.173370</td>
      <td>NaN</td>
      <td>0.319334</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.350083</td>
      <td>NaN</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.010889</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>-0.488589</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.fillna(method='ffill')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-1.540472</td>
      <td>-1.907663</td>
      <td>0.245070</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.203660</td>
      <td>0.087430</td>
      <td>-0.158976</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.173370</td>
      <td>0.087430</td>
      <td>0.319334</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.350083</td>
      <td>0.087430</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.010889</td>
      <td>0.087430</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>5</th>
      <td>-0.488589</td>
      <td>0.087430</td>
      <td>-0.543169</td>
    </tr>
  </tbody>
</table>
</div>




```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-1.540472</td>
      <td>-1.907663</td>
      <td>0.245070</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.203660</td>
      <td>0.087430</td>
      <td>-0.158976</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.173370</td>
      <td>NaN</td>
      <td>0.319334</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.350083</td>
      <td>NaN</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.010889</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>-0.488589</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.fillna(method='ffill',limit=2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-1.540472</td>
      <td>-1.907663</td>
      <td>0.245070</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.203660</td>
      <td>0.087430</td>
      <td>-0.158976</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.173370</td>
      <td>0.087430</td>
      <td>0.319334</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.350083</td>
      <td>0.087430</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.010889</td>
      <td>NaN</td>
      <td>-0.543169</td>
    </tr>
    <tr>
      <th>5</th>
      <td>-0.488589</td>
      <td>NaN</td>
      <td>-0.543169</td>
    </tr>
  </tbody>
</table>
</div>




```python
 data = pd.Series([1., NA, 3.5, NA, 7])
```


```python
data
```




    0    1.0
    1    NaN
    2    3.5
    3    NaN
    4    7.0
    dtype: float64




```python
data.fillna(data.mean())
```




    0    1.000000
    1    3.833333
    2    3.500000
    3    3.833333
    4    7.000000
    dtype: float64




```python
data = pd.DataFrame({'k1': ['one', 'two'] * 3 + ['two'],
   ....:                      'k2': [1, 1, 2, 3, 3, 4, 4]})
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>one</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>two</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>one</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>two</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>two</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.duplicated()
```




    0    False
    1    False
    2    False
    3    False
    4    False
    5    False
    6     True
    dtype: bool




```python
data['v1'] = range(7)
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>one</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>two</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>one</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>two</td>
      <td>4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>two</td>
      <td>4</td>
      <td>6</td>
    </tr>
  </tbody>
</table>
</div>




```python
data['v2'] = np.random(8)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [105], in <cell line: 1>()
    ----> 1 data['v2'] = np.random(8)
    

    TypeError: 'module' object is not callable



```python
data['v2'] = np.random(7)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [106], in <cell line: 1>()
    ----> 1 data['v2'] = np.random(7)
    

    TypeError: 'module' object is not callable



```python
data['v2'] = np.random.randn(7)
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
      <th>v2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
      <td>0.627183</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
      <td>-0.425835</td>
    </tr>
    <tr>
      <th>2</th>
      <td>one</td>
      <td>2</td>
      <td>2</td>
      <td>-0.256180</td>
    </tr>
    <tr>
      <th>3</th>
      <td>two</td>
      <td>3</td>
      <td>3</td>
      <td>-1.305495</td>
    </tr>
    <tr>
      <th>4</th>
      <td>one</td>
      <td>3</td>
      <td>4</td>
      <td>-0.144300</td>
    </tr>
    <tr>
      <th>5</th>
      <td>two</td>
      <td>4</td>
      <td>5</td>
      <td>0.846278</td>
    </tr>
    <tr>
      <th>6</th>
      <td>two</td>
      <td>4</td>
      <td>6</td>
      <td>0.640688</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.drop_duplicates(['k1'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
      <th>v2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
      <td>0.627183</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
      <td>-0.425835</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.drop_duplicates(['k1','k2'],keep='last')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
      <th>v2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
      <td>0.627183</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
      <td>-0.425835</td>
    </tr>
    <tr>
      <th>2</th>
      <td>one</td>
      <td>2</td>
      <td>2</td>
      <td>-0.256180</td>
    </tr>
    <tr>
      <th>3</th>
      <td>two</td>
      <td>3</td>
      <td>3</td>
      <td>-1.305495</td>
    </tr>
    <tr>
      <th>4</th>
      <td>one</td>
      <td>3</td>
      <td>4</td>
      <td>-0.144300</td>
    </tr>
    <tr>
      <th>6</th>
      <td>two</td>
      <td>4</td>
      <td>6</td>
      <td>0.640688</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.duplicated(k1)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [111], in <cell line: 1>()
    ----> 1 data.duplicated(k1)
    

    NameError: name 'k1' is not defined



```python
data.drop_duplicates()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
      <th>v2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
      <td>0.627183</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
      <td>-0.425835</td>
    </tr>
    <tr>
      <th>2</th>
      <td>one</td>
      <td>2</td>
      <td>2</td>
      <td>-0.256180</td>
    </tr>
    <tr>
      <th>3</th>
      <td>two</td>
      <td>3</td>
      <td>3</td>
      <td>-1.305495</td>
    </tr>
    <tr>
      <th>4</th>
      <td>one</td>
      <td>3</td>
      <td>4</td>
      <td>-0.144300</td>
    </tr>
    <tr>
      <th>5</th>
      <td>two</td>
      <td>4</td>
      <td>5</td>
      <td>0.846278</td>
    </tr>
    <tr>
      <th>6</th>
      <td>two</td>
      <td>4</td>
      <td>6</td>
      <td>0.640688</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.drop_duplicates(subset='k1')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>k1</th>
      <th>k2</th>
      <th>v1</th>
      <th>v2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>one</td>
      <td>1</td>
      <td>0</td>
      <td>0.627183</td>
    </tr>
    <tr>
      <th>1</th>
      <td>two</td>
      <td>1</td>
      <td>1</td>
      <td>-0.425835</td>
    </tr>
  </tbody>
</table>
</div>




```python
data = pd.DataFrame({'food': ['bacon', 'pulled pork', 'bacon',
   ....:                               'Pastrami', 'corned beef', 'Bacon',
   ....:                               'pastrami', 'honey ham', 'nova lox'],
   ....:                      'ounces': [4, 3, 12, 6, 7.5, 8, 3, 5, 6]})
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>food</th>
      <th>ounces</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>bacon</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>pulled pork</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>bacon</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Pastrami</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>corned beef</td>
      <td>7.5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bacon</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>pastrami</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>honey ham</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>nova lox</td>
      <td>6.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
meat_to_animal = {
    'bacon': 'pig',
    'pulled pork': 'pig',
    'pastrami': 'cow',
    'corned beef': 'cow',
    'honey ham': 'pig',
    'nova lox': 'salmon'
}
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>food</th>
      <th>ounces</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>bacon</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>pulled pork</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>bacon</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Pastrami</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>corned beef</td>
      <td>7.5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bacon</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>pastrami</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>honey ham</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>nova lox</td>
      <td>6.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
meat_to_animal = {
    'bacon': 'pig',
    'pulled pork': 'pig',
    'pastrami': 'cow',
    'corned beef': 'cow',
    'honey ham': 'pig',
    'nova lox': 'salmon'
}
```


```python
lowercased = data['food'].str.lower()
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>food</th>
      <th>ounces</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>bacon</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>pulled pork</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>bacon</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Pastrami</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>corned beef</td>
      <td>7.5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bacon</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>pastrami</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>honey ham</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>nova lox</td>
      <td>6.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
 lowercased = data['food'].str.lower()
```


```python
lowercased
```




    0          bacon
    1    pulled pork
    2          bacon
    3       pastrami
    4    corned beef
    5          bacon
    6       pastrami
    7      honey ham
    8       nova lox
    Name: food, dtype: object




```python
data['animal'] = lowercased.map(meat_to_animal)
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>food</th>
      <th>ounces</th>
      <th>animal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>bacon</td>
      <td>4.0</td>
      <td>pig</td>
    </tr>
    <tr>
      <th>1</th>
      <td>pulled pork</td>
      <td>3.0</td>
      <td>pig</td>
    </tr>
    <tr>
      <th>2</th>
      <td>bacon</td>
      <td>12.0</td>
      <td>pig</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Pastrami</td>
      <td>6.0</td>
      <td>cow</td>
    </tr>
    <tr>
      <th>4</th>
      <td>corned beef</td>
      <td>7.5</td>
      <td>cow</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bacon</td>
      <td>8.0</td>
      <td>pig</td>
    </tr>
    <tr>
      <th>6</th>
      <td>pastrami</td>
      <td>3.0</td>
      <td>cow</td>
    </tr>
    <tr>
      <th>7</th>
      <td>honey ham</td>
      <td>5.0</td>
      <td>pig</td>
    </tr>
    <tr>
      <th>8</th>
      <td>nova lox</td>
      <td>6.0</td>
      <td>salmon</td>
    </tr>
  </tbody>
</table>
</div>




```python
hah = lowercased.map(meat_to_animal)
```


```python
hah
```




    0       pig
    1       pig
    2       pig
    3       cow
    4       cow
    5       pig
    6       cow
    7       pig
    8    salmon
    Name: food, dtype: object




```python
data['food'].map(lambda x:meat_to_animal[x.lower()])
```




    0       pig
    1       pig
    2       pig
    3       cow
    4       cow
    5       pig
    6       cow
    7       pig
    8    salmon
    Name: food, dtype: object




```python
data = pd.Series([1.,-999.,2.,-999.,-1000.,3.])
```


```python
data
```




    0       1.0
    1    -999.0
    2       2.0
    3    -999.0
    4   -1000.0
    5       3.0
    dtype: float64




```python
data.replace(-999,np.nan)
```




    0       1.0
    1       NaN
    2       2.0
    3       NaN
    4   -1000.0
    5       3.0
    dtype: float64




```python
data.replace([-999,-1000],np.nan)
```




    0    1.0
    1    NaN
    2    2.0
    3    NaN
    4    NaN
    5    3.0
    dtype: float64




```python
data.replace([-999,-1000],[np.nan,0])
```




    0    1.0
    1    NaN
    2    2.0
    3    NaN
    4    0.0
    5    3.0
    dtype: float64




```python
data
```




    0       1.0
    1    -999.0
    2       2.0
    3    -999.0
    4   -1000.0
    5       3.0
    dtype: float64




```python
data.replace([-999,-1000],[np.nan,0])
```




    0    1.0
    1    NaN
    2    2.0
    3    NaN
    4    0.0
    5    3.0
    dtype: float64




```python
data.replace({-999:np.nan,-1000:0})
```




    0    1.0
    1    NaN
    2    2.0
    3    NaN
    4    0.0
    5    3.0
    dtype: float64




```python
data = pd.DataFrame(np.arange(12),reshape(3,4)),
                    index=['ohio','colorado','New York'],
                    columns=['one','two','three','four'])
```


      Input In [137]
        index=['ohio','colorado','New York'],
        ^
    IndentationError: unexpected indent
    



```python
data = pd.DataFrame(np.arange(12).reshape((3, 4)),
   ....:                     index=['Ohio', 'Colorado', 'New York'],
   ....:                     columns=['one', 'two', 'three', 'four'])
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
 transform = lambda x: x[:4].upper()
```


```python
transform
```




    <function __main__.<lambda>(x)>




```python
data.index.map(transform)
```




    Index(['OHIO', 'COLO', 'NEW '], dtype='object')




```python
data.rename(index=str.title,columns=str.upper)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ONE</th>
      <th>TWO</th>
      <th>THREE</th>
      <th>FOUR</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.rename(index={index={'OHIO':'INDIANA'},
                  columns={'three':'peekaboo'}})
```


      Input In [144]
        data.rename(index={index={'OHIO':'INDIANA'},
                           ^
    SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
    



```python
 data.rename(index={'OHIO': 'INDIANA'},
   ....:             columns={'three': 'peekaboo'})
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>peekaboo</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
 data.rename(index={'OHIO': 'INDIANA'}, inplace=True)
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
 data.rename(index={'OHIO': 'INDIANA'}, inplace=True)
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.rename(index={'OHIO': 'INDIANA'},
   ....:             columns={'three': 'peekaboo'})
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
      <th>peekaboo</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>New York</th>
      <td>8</td>
      <td>9</td>
      <td>10</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.rename(index={'OHIO': 'INDIANA'}, inplace=True)
```


```python
ages = [20,22,25,27,21,23,37,31,61,45,41,32]
```


```python
bins = [18,25,35,60,100]
```


```python
cats = pd.cut(ages,bins)
```


```python
cats
```




    [(18, 25], (18, 25], (18, 25], (25, 35], (18, 25], ..., (25, 35], (60, 100], (35, 60], (35, 60], (25, 35]]
    Length: 12
    Categories (4, interval[int64, right]): [(18, 25] < (25, 35] < (35, 60] < (60, 100]]




```python
cats.codes
```




    array([0, 0, 0, 1, 0, 0, 2, 1, 3, 2, 2, 1], dtype=int8)




```python
cats.categories
```




    IntervalIndex([(18, 25], (25, 35], (35, 60], (60, 100]], dtype='interval[int64, right]')




```python
pd.value_counts(cats)
```




    (18, 25]     5
    (25, 35]     3
    (35, 60]     3
    (60, 100]    1
    dtype: int64




```python
pd.cut(ages,[18,26,36,61,100],right=False)
```




    [[18, 26), [18, 26), [18, 26), [26, 36), [18, 26), ..., [26, 36), [61, 100), [36, 61), [36, 61), [26, 36)]
    Length: 12
    Categories (4, interval[int64, left]): [[18, 26) < [26, 36) < [36, 61) < [61, 100)]




```python
pd.cut(ages,[18,26,61,100],right=True)
```




    [(18, 26], (18, 26], (18, 26], (26, 61], (18, 26], ..., (26, 61], (26, 61], (26, 61], (26, 61], (26, 61]]
    Length: 12
    Categories (3, interval[int64, right]): [(18, 26] < (26, 61] < (61, 100]]




```python
group_names = ['Youth','YougAdult','MiddleAged','Senior']
```


```python
pd.cut(ages,binss,labels=group_names)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [162], in <cell line: 1>()
    ----> 1 pd.cut(ages,binss,labels=group_names)
    

    NameError: name 'binss' is not defined



```python
pd.cut(ages,bins,labels=group_names)
```




    ['Youth', 'Youth', 'Youth', 'YougAdult', 'Youth', ..., 'YougAdult', 'Senior', 'MiddleAged', 'MiddleAged', 'YougAdult']
    Length: 12
    Categories (4, object): ['Youth' < 'YougAdult' < 'MiddleAged' < 'Senior']




```python
data = np.random.rand(20)
```


```python
data
```




    array([0.55721049, 0.53811612, 0.47031233, 0.10362822, 0.11045115,
           0.54325825, 0.06957537, 0.67701274, 0.40255899, 0.85489466,
           0.84740773, 0.1551859 , 0.75025424, 0.25080181, 0.92504855,
           0.54237128, 0.90552698, 0.71897299, 0.39960122, 0.44983875])




```python
pd.cut(data,4,precision=2)
```




    [(0.5, 0.71], (0.5, 0.71], (0.28, 0.5], (0.069, 0.28], (0.069, 0.28], ..., (0.5, 0.71], (0.71, 0.93], (0.71, 0.93], (0.28, 0.5], (0.28, 0.5]]
    Length: 20
    Categories (4, interval[float64, right]): [(0.069, 0.28] < (0.28, 0.5] < (0.5, 0.71] < (0.71, 0.93]]




```python
pd.cut(data,3,precision=2)
```




    [(0.35, 0.64], (0.35, 0.64], (0.35, 0.64], (0.069, 0.35], (0.069, 0.35], ..., (0.35, 0.64], (0.64, 0.93], (0.64, 0.93], (0.35, 0.64], (0.35, 0.64]]
    Length: 20
    Categories (3, interval[float64, right]): [(0.069, 0.35] < (0.35, 0.64] < (0.64, 0.93]]




```python
data = np.random.randn(10)
```


```python
data
```




    array([-0.00417715,  1.13554074, -0.27054801,  2.06853709, -0.23270768,
           -0.46507721, -0.75096285,  0.23377226, -1.1371205 ,  0.54457195])




```python
pd.cut(data,4,precision=2)
```




    [(-0.34, 0.47], (0.47, 1.27], (-0.34, 0.47], (1.27, 2.07], (-0.34, 0.47], (-1.14, -0.34], (-1.14, -0.34], (-0.34, 0.47], (-1.14, -0.34], (0.47, 1.27]]
    Categories (4, interval[float64, right]): [(-1.14, -0.34] < (-0.34, 0.47] < (0.47, 1.27] < (1.27, 2.07]]




```python
pd.cut(data,2,precision=1)
```




    [(-1.1, 0.5], (0.5, 2.1], (-1.1, 0.5], (0.5, 2.1], (-1.1, 0.5], (-1.1, 0.5], (-1.1, 0.5], (-1.1, 0.5], (-1.1, 0.5], (0.5, 2.1]]
    Categories (2, interval[float64, right]): [(-1.1, 0.5] < (0.5, 2.1]]




```python
data = np.random.randn(1000)
```


```python
data
```




    array([-2.53084922e-01,  8.91024501e-01, -2.76868814e-01,  4.55797006e-01,
           -5.69119014e-01, -5.46704164e-02,  3.81969132e-01,  8.51957588e-02,
            1.85405382e+00,  1.73515046e-01, -5.42915365e-01,  7.01841672e-01,
            4.38594449e-01, -6.06391152e-01, -6.33243548e-01, -1.40922347e+00,
            1.45775052e+00,  1.88632004e-01, -5.73184763e-02, -2.07341602e-01,
           -2.09297844e+00, -1.32412259e+00, -1.32099990e+00, -7.02895202e-02,
           -4.66020823e-01, -8.70185283e-01,  4.04678442e-01, -3.42884840e-01,
            3.06927552e-01, -5.27335545e-01, -1.59481553e-01,  1.35084981e+00,
           -7.14692764e-01,  7.37126404e-03, -9.78872599e-01, -1.59474519e+00,
            4.07116024e-01, -1.79207505e+00,  1.10103306e+00, -1.52031926e+00,
           -9.46237724e-01, -2.72968829e-01,  5.53572935e-02,  1.52896292e+00,
           -1.14626888e+00,  2.07413023e-01, -1.63161807e+00, -1.08051509e+00,
            4.52469235e-01,  6.35365474e-01,  1.52851870e+00,  8.98868246e-02,
           -1.54365418e+00,  3.15230297e-01, -6.96250873e-01, -7.88865458e-01,
           -9.03762312e-01, -2.12454942e+00, -3.03101093e-01, -6.26307191e-02,
            1.44319380e+00, -1.10967451e+00,  8.13474539e-01, -1.39437434e-02,
            9.99040488e-01,  1.85115152e-01, -1.71642673e+00, -1.93654332e+00,
            1.74032960e+00,  5.56595115e-01,  6.43598111e-01,  3.10736659e-01,
           -5.02330897e-01, -6.92775970e-02, -9.13196965e-01, -4.70965688e-01,
            1.00676677e+00, -2.22273884e+00, -1.75500004e-01, -2.18003430e+00,
           -7.45009456e-01,  6.14355807e-01, -2.28139647e-01,  1.42918594e+00,
           -9.84875966e-01,  1.09965747e+00,  7.02624299e-01, -4.23536482e-01,
           -5.28665181e-02, -1.93226114e-01,  1.83661558e+00, -1.83521717e-01,
            4.80097821e-01,  1.59215231e+00,  9.77278093e-02,  3.80439317e-01,
           -2.63545008e-01,  1.77471144e-02, -5.16432840e-01, -8.65364124e-01,
            7.04419377e-01,  4.22814231e-01,  4.23596594e-01, -1.37897625e+00,
           -3.39795167e-01, -3.20247905e-01,  2.25397578e+00, -1.38849139e+00,
            9.10455745e-01, -3.14589733e-01,  1.25025376e+00, -1.16416796e+00,
            4.80081902e-01,  4.11038352e-01, -6.04697482e-01,  3.53148071e-01,
           -1.62176429e+00,  9.99895734e-01, -2.70683495e-01, -1.54783246e+00,
           -3.16725330e-01,  3.05790304e-01, -3.45743712e-01,  7.31100540e-01,
            6.70808729e-01, -1.12645606e+00,  3.12721816e-01,  3.78895486e-01,
           -7.94756366e-01, -1.57708216e+00,  1.59688921e-01, -4.00473271e-01,
            1.82660614e-02, -1.27946411e+00, -1.45122747e+00, -5.30286734e-01,
           -1.57698173e+00, -1.83094469e+00,  1.41929841e+00,  7.29936481e-01,
           -1.49102627e-01,  1.87927389e+00, -9.79422232e-01,  2.87112361e-01,
            1.23257154e+00, -7.68697814e-01,  1.08196673e-01, -2.59342673e-01,
            1.76003306e-01, -6.80494698e-01, -4.83014215e-01,  7.92607936e-01,
            2.04340545e+00,  4.17758730e-01,  1.95500747e-01,  6.43094045e-01,
            2.13011272e-02,  7.68298148e-01,  2.10651987e+00, -9.20142452e-01,
            1.90947972e+00,  5.38694321e-01,  3.60806607e-01, -1.02892143e+00,
            8.61156593e-01, -1.05529020e+00, -5.70910339e-02,  2.17024497e-01,
            5.51035928e-01,  1.56045682e+00,  5.68865470e-01, -2.90690338e+00,
           -4.04950111e-01, -1.60770895e-01,  4.40946574e-01,  1.19018617e+00,
            9.48085974e-01, -3.88032123e-01,  1.50568058e+00, -6.16885488e-01,
           -3.53408381e-01, -1.48499794e+00,  1.07596335e+00,  2.17103985e-01,
           -4.92403324e-01,  6.74614552e-01,  3.35859887e-02,  2.18794683e+00,
            7.93432326e-01,  4.35186841e-01, -8.18592198e-01,  1.47146166e+00,
           -9.54976470e-01,  3.06332990e-01,  3.72146976e-01, -8.76793405e-01,
           -9.91943469e-01, -4.84667218e-01, -6.11019644e-01,  2.34453239e-03,
           -4.51602932e-01, -6.28768677e-01, -9.60193960e-01,  1.81103695e-01,
            2.32184377e+00,  4.24399507e-01, -1.44284240e+00,  8.36460129e-01,
           -2.68882883e-01,  1.92314317e+00,  1.57104170e+00, -2.91897325e-01,
           -2.31303897e+00, -2.67076723e-01, -1.09907454e+00,  1.26437988e+00,
           -3.19568538e-01,  6.93665860e-01,  5.10048877e-01,  9.90183830e-01,
           -1.69220970e+00, -3.32593354e-01,  1.38937875e+00, -9.61149388e-01,
           -9.50285598e-01, -1.68141826e+00,  1.14630064e+00,  1.81375144e+00,
            4.75118002e-01, -4.86198560e-01,  1.64675991e+00, -3.85311389e-01,
           -7.28817589e-01,  2.28411706e-01, -7.46680988e-01, -8.71946473e-01,
           -3.55012775e-01,  3.99104624e-01, -5.36891115e-01,  2.74996538e+00,
            1.12364938e-01,  1.39756230e+00,  3.79315679e-01,  3.11929752e-01,
           -1.54313902e+00,  3.27298388e-01, -7.01834041e-01, -4.95808353e-02,
           -2.41453664e-01,  1.37920350e+00, -1.00936654e+00,  1.03323785e+00,
            1.81393661e+00,  8.90405818e-01, -5.10498438e-02, -3.13214672e-01,
            2.76482446e+00, -2.51683398e-01, -4.06975322e-01,  1.48538387e+00,
           -6.25284742e-01, -3.96859904e-01,  7.81956444e-02, -1.10338726e+00,
            1.11339177e+00, -3.10414805e-01,  4.58957589e-01,  6.67087964e-01,
            4.93389561e-01,  7.53244112e-01, -3.56359665e-02, -8.67705986e-01,
            2.04537660e+00, -6.04290206e-01,  6.58252856e-01,  6.62359152e-01,
            1.84302256e-01,  1.71373455e-01,  1.30751054e+00, -2.60930050e-01,
           -1.52409950e+00,  9.03258528e-01, -1.00541705e+00,  7.75515075e-01,
           -1.80770746e-01,  1.54376480e-01, -6.16815929e-01,  3.58283414e-02,
            2.34675107e-01, -7.87053725e-01,  1.34275431e+00,  4.60709876e-02,
            1.11283247e-01, -6.43708939e-01,  1.39907676e+00,  5.29905502e-01,
            7.24446737e-01, -4.91573816e-01, -1.22246233e+00, -3.31882231e-02,
           -8.29274037e-01,  4.02561619e-01, -1.23015695e-02,  2.50734669e+00,
           -1.06579618e+00, -1.28775048e+00,  3.92094492e-01,  1.61952837e-01,
           -2.34370168e-01,  2.02032207e+00, -4.32040686e-01,  6.72889668e-01,
           -3.34378615e-01, -1.54059130e+00, -1.90656962e+00,  2.97806944e-01,
            1.38297095e-01, -1.01206154e+00, -1.58141716e+00,  2.73704106e+00,
            1.86105478e-01, -3.13537327e-01, -6.48282919e-01, -7.70836664e-01,
           -3.38803850e-01, -2.82024025e-01,  1.08131918e+00, -4.87298458e-01,
           -1.48699636e+00, -1.92130499e+00, -6.95952994e-01,  1.34045543e+00,
            6.84288533e-01, -6.92714302e-01,  5.97656683e-01, -1.25724282e-01,
            5.50884651e-01, -1.68009914e+00, -1.18522812e+00,  8.04372657e-01,
           -6.31682463e-01, -6.51858768e-01,  5.74870414e-01,  6.61650748e-01,
            1.28067564e+00, -1.79504534e+00, -1.95168306e+00,  1.01062941e+00,
            2.69464937e+00,  2.92823051e+00,  8.78878484e-01,  1.16356086e-01,
            2.39224875e+00, -2.22137464e+00, -1.19035040e+00,  4.12779973e-01,
           -1.48721360e-01,  9.87522911e-01,  2.49795603e-01, -4.47551995e-01,
            8.36231903e-01,  6.90335337e-01,  2.00457768e-01, -1.53583745e-01,
           -1.58157963e-01,  5.74373795e-02,  2.14150297e-01, -3.98308846e-01,
            8.55433512e-01,  2.32752883e+00, -6.18515938e-01, -1.00561433e+00,
            8.05380184e-01,  9.50149427e-01,  1.13344187e-01,  1.33446049e+00,
            1.10230961e+00, -4.70918007e-01, -4.05416488e-01, -1.09645657e+00,
           -6.14121936e-01,  3.44214353e-01,  6.45446045e-01, -8.33189108e-02,
           -2.47066610e+00, -8.24313365e-01, -6.13297154e-01, -4.64630397e-01,
           -1.05749604e+00,  7.20941104e-01, -4.96231202e-01, -3.21410948e-01,
           -4.23112479e-02, -8.86932660e-01, -2.08669085e+00, -1.03675049e+00,
            7.21092620e-01, -3.18439756e-01, -1.82907160e+00,  2.72386230e-01,
           -1.87807760e+00,  1.51801763e+00,  1.07499794e-01,  9.17026834e-01,
           -2.08621755e+00, -1.80513120e+00,  5.80834326e-01, -1.16597304e+00,
            1.05956958e-01, -4.52030626e-02,  1.76077441e-02, -6.73878558e-01,
            7.79888825e-01, -1.47231853e+00,  5.02018179e-01,  7.90973065e-01,
            2.44345960e-01, -3.97675338e-01,  1.18572218e+00,  1.73045720e-01,
            2.58610669e+00, -6.64600444e-01,  2.05432219e+00,  8.47820581e-01,
            2.18330204e-01, -2.05118713e+00,  1.52356502e+00,  6.18002174e-03,
           -3.49846654e-01,  3.88936671e-01,  4.76834450e-01,  1.16995828e+00,
            7.65207230e-02, -1.53678867e+00, -8.85312782e-01, -9.81158590e-02,
            6.45847459e-01, -2.56846602e-01,  3.76254445e-01,  2.08494284e+00,
            1.05732497e+00, -5.10395982e-01, -1.74762980e+00, -4.56314954e-01,
           -9.65749883e-01,  4.60581206e-01,  2.07946807e-01,  4.00489421e-01,
            1.59519074e+00,  1.90455930e-01,  7.50510804e-01, -1.29078007e+00,
           -1.15998551e+00, -5.95350820e-02, -8.18968978e-01, -8.68149180e-01,
            1.15764754e+00, -5.00774863e-01, -1.55787520e+00, -1.11857586e+00,
            3.49144482e-01, -2.02810908e-02,  4.72152661e-01, -2.64414086e-01,
            3.14467399e-01,  6.55147445e-02, -9.24706451e-01, -4.23956565e-01,
            5.75271122e-01,  9.61170558e-02,  3.32515606e-02, -8.40217789e-02,
            9.20900030e-01, -6.55342406e-01, -4.91853538e-01, -5.80813950e-02,
           -4.21986287e-01, -9.34498486e-01, -5.87276871e-01, -7.39069131e-01,
           -3.86594421e-01, -2.00290919e-01, -7.13224932e-01, -1.17891815e+00,
            7.62371462e-01,  3.66780342e-01,  2.40645084e-01, -7.31516966e-01,
           -7.78207110e-01, -2.11038088e-01, -2.85914983e-01,  1.45899101e+00,
            3.10169192e-01, -8.41444562e-01, -7.11922096e-01, -4.30778171e-01,
            1.58564252e-01,  1.01264108e-01, -1.16620715e+00,  4.69809202e-02,
           -2.96042719e+00,  1.10913149e+00, -7.71141133e-01,  5.62750360e-01,
           -1.99848009e+00, -1.06146400e+00,  1.12642965e+00, -3.37559640e-01,
            9.72383754e-01, -5.79258468e-01,  3.23701190e-01, -1.00968421e+00,
            2.12877043e+00, -1.23562894e+00,  6.82031285e-01,  4.23908238e-01,
            8.95424440e-01,  1.95742688e-02, -1.22229238e+00, -1.23240497e+00,
            1.94184741e+00,  1.32006690e+00,  6.62248271e-01,  1.29549650e-01,
            7.31111450e-01, -1.62780290e+00,  8.69165447e-01,  4.94008332e-01,
            5.18722273e-01, -2.50364069e+00, -5.95920886e-02,  5.64443492e-01,
           -8.15300573e-01, -1.29063607e-01,  1.35983335e+00,  1.56037079e+00,
            9.27068755e-02,  7.05508322e-01, -8.91355298e-01, -5.79117010e-01,
           -7.42262597e-01, -8.44782706e-01, -1.45220515e+00,  5.17371329e-01,
            3.60146145e-01,  1.34401803e+00,  1.50111413e+00, -2.83096820e-01,
           -4.23254913e-01,  6.13243331e-01, -9.56404047e-01, -1.37355427e+00,
           -6.74617369e-01, -8.20016946e-01, -7.40612629e-01,  4.83978357e-01,
            1.39018687e+00, -9.43050139e-01,  2.48456482e-01, -1.76272322e+00,
           -1.03313351e+00,  6.69294311e-01, -3.52933780e-01, -2.01103407e-01,
            1.58774528e+00, -1.20861723e+00,  6.67664029e-01, -5.17913230e-01,
           -1.03522395e+00,  6.45869299e-01, -2.01165787e+00, -3.58008663e-01,
           -2.41071566e+00,  1.01471191e+00, -1.59604379e+00, -4.62483072e-01,
           -1.58754760e-01,  7.45255699e-01,  6.29610352e-01,  8.73031633e-01,
            7.06296683e-01,  1.48904793e+00,  8.42640335e-01,  2.18934920e-01,
           -7.09099152e-01,  5.60567606e-01, -9.41402118e-02,  1.00796381e+00,
            2.58292362e-01, -4.71238522e-01,  3.13195277e-01, -1.56611391e+00,
            1.65734092e+00,  1.20283914e+00,  7.85850692e-01,  7.79147042e-01,
            2.49696382e-01,  9.79996398e-01,  1.02865038e+00, -1.33190530e+00,
            1.65314953e-01, -1.93126654e+00, -6.12412199e-02, -1.16794479e+00,
           -1.23623155e+00, -4.22335558e-02,  9.64960507e-02, -3.23601771e-02,
            5.25210842e-01,  6.05806080e-01,  4.58580657e-01, -4.47502343e-01,
           -8.51346671e-02,  1.08484207e+00,  8.88226264e-01,  1.10057847e-02,
           -2.84908908e-02,  1.52954739e+00,  1.68181447e+00,  6.22362007e-01,
           -6.76216202e-01,  9.69610082e-01, -1.11753508e+00,  8.59536174e-02,
            4.80702782e-01, -5.58346044e-01,  3.31310739e-01, -9.63773385e-02,
            2.06523149e+00,  9.96109030e-02, -6.47201262e-01,  1.83228735e+00,
            3.08506652e-01,  7.66852654e-01,  1.33428590e+00,  5.99831383e-01,
            6.06308997e-01,  6.29050223e-01,  2.29399578e-02,  1.06407566e+00,
           -1.61156547e+00, -1.48747913e+00, -9.68233274e-01,  3.82570472e-01,
           -1.60796652e-01, -4.72057735e-01,  7.89467803e-01, -1.11281206e-02,
            1.34898527e-01, -2.53608826e-01, -4.39364666e-01, -1.18416528e+00,
           -1.01276695e-01, -1.32810390e+00, -6.16089431e-02, -1.74014012e+00,
           -3.42586800e-01, -6.98654387e-01,  6.80241650e-01, -8.24915525e-01,
           -2.00005504e+00,  2.22263703e+00, -2.82085970e-01,  1.90634540e-01,
           -9.25951402e-01,  8.86815267e-03,  7.03326188e-01,  1.07985977e+00,
           -1.27697973e+00, -1.14256258e+00, -4.76758839e-01, -1.00521995e+00,
            1.55132231e+00,  2.40812847e+00, -1.90596452e+00, -3.73305779e-01,
           -3.98665958e-01,  3.12381777e-01, -1.62316311e+00,  1.63532155e+00,
           -9.38026597e-01,  5.45482035e-01,  1.01818668e+00, -9.99399399e-01,
           -1.30252033e+00, -1.43240121e+00, -8.89398297e-01,  5.84428319e-01,
            1.22843786e+00, -4.80777144e-01,  4.98782813e-01, -6.33493538e-01,
            1.79074104e+00, -5.06999068e-01, -5.16666616e-01,  2.50809417e-02,
            3.15332470e-01, -2.73796175e-01,  1.01316894e-01, -2.37173569e-01,
            9.07690388e-01, -5.59378702e-01,  5.74982932e-01, -1.59445463e-01,
            3.60036121e-01,  1.21036731e+00, -1.16069410e+00, -6.99254639e-01,
           -3.18001194e-01, -1.13283838e+00,  6.52661025e-01,  1.20606075e+00,
            3.18484665e-02,  3.73938601e-01, -4.56601706e-01, -1.81586755e-01,
            1.71890033e-01, -1.67897150e-01, -1.11331647e+00,  2.04097467e-01,
           -7.43641302e-01,  1.43477145e+00,  9.99947278e-01,  5.87290943e-01,
           -3.39909705e-02, -2.60046760e+00, -1.01666456e+00, -7.74845754e-01,
            1.32906245e+00, -1.15696240e+00, -6.61223927e-01,  7.09745290e-01,
            1.09562186e+00, -6.44528697e-01, -1.82069028e-01, -6.28905370e-01,
           -2.45566314e+00, -4.00404981e-01, -9.26297739e-01, -8.32601263e-01,
            4.08718695e-02,  3.84862575e-01,  6.91685452e-01,  2.19676366e+00,
            1.79728199e+00,  6.76622272e-01,  4.32499213e-02, -1.80413810e-01,
           -3.27535184e-01,  1.67939266e-01,  1.37333417e+00, -1.32244052e+00,
           -1.25582853e+00,  1.69972716e+00, -9.25812587e-01,  1.78858417e-01,
            6.25758247e-02, -1.81287534e-02,  1.65872252e+00,  1.11373983e+00,
           -7.96851911e-01, -9.27833831e-01, -1.60665879e+00,  1.96821911e+00,
           -3.01842556e-01,  5.47311579e-01,  2.50923047e-01,  2.58119188e+00,
            4.70271001e-01, -3.12164833e-02,  2.10833439e+00, -1.03174991e+00,
            1.35818547e+00,  1.17221409e+00, -7.59686161e-01,  2.46770541e-01,
           -5.39227187e-01, -1.44682555e+00,  2.18513949e-01,  1.54437669e+00,
           -3.02334708e-01, -2.13393605e+00,  1.11998788e+00, -1.98278529e-01,
           -5.32506439e-01, -2.88929462e-01, -6.46759483e-02, -4.23078963e-01,
           -8.34173836e-01,  4.66232327e-01, -3.64475877e-01,  8.73219202e-01,
           -5.80585247e-01, -2.13794458e+00, -7.35604607e-01,  8.51324413e-01,
           -2.04919166e+00,  4.59675633e-01,  7.74648662e-01, -2.01350564e+00,
            2.83655190e-01,  7.41334438e-01, -1.04286109e+00,  8.95547758e-01,
            5.42627109e-01, -1.53293221e+00,  2.74962963e-01, -5.24438784e-02,
           -3.75046468e-01,  7.15744963e-01,  6.95418080e-01, -7.83545717e-01,
            8.66081190e-01,  9.26901651e-01, -8.75466916e-01,  1.31281915e+00,
            3.81478540e-01, -1.69424711e-02, -8.70984083e-01,  7.88080804e-01,
           -3.19066206e-01,  2.58879740e-01, -4.59053849e-01, -5.28352395e-01,
            3.84670999e-01, -1.24394616e-02, -2.01729582e-01, -2.96814685e-01,
            3.14338078e-01,  1.55290597e+00, -2.78057931e-01,  1.40170504e+00,
            5.50244418e-01, -8.39156358e-01,  1.25693050e+00, -3.05984519e-01,
            2.10365126e+00,  1.17893034e+00, -6.72108296e-01,  7.25630864e-01,
            4.07991000e-02,  7.28003352e-02,  1.25842038e+00,  1.39711784e+00,
           -6.43757726e-01,  1.01156321e+00, -5.45175654e-01,  5.69294499e-01,
            9.28372180e-01,  4.63982587e-01, -4.41014164e-01,  3.73699694e-01,
           -6.84262921e-01, -9.87170068e-01,  5.69543235e-01, -1.82836471e+00,
            7.97893768e-01, -3.41735521e-01, -4.19660031e-01, -2.15901716e+00,
            4.05847282e-01, -2.36841809e-01,  6.68078354e-01,  9.98752630e-01,
           -5.16916296e-01, -6.07481067e-01,  5.09905345e-01, -4.79430818e-01,
            2.95743417e-01, -3.83309966e-01, -1.33705886e+00,  1.87214844e-01,
           -2.42348101e-01, -2.46055376e-01, -5.54932608e-01, -8.81045929e-02,
           -8.88232720e-01, -1.49949571e+00, -7.65609622e-01, -2.86689182e-01,
            6.16637720e-01,  5.06002831e-01, -1.52079574e+00, -1.63844515e+00,
           -1.03574134e+00,  1.30397990e+00, -1.67203245e-01, -1.32639714e-01,
            5.77913971e-01,  1.84290684e+00,  1.21069876e+00, -1.84053871e-02,
            5.93416717e-01,  2.19676895e+00, -1.32622257e-01,  5.02120521e-01,
           -6.60344725e-02,  1.54305943e-01, -4.43391645e-01,  6.02592682e-01,
            3.00049679e-01, -2.08073811e-01,  1.14317327e+00, -3.04100282e-02,
           -4.21463791e-01,  9.21199813e-01,  2.43329184e+00,  7.34281812e-01,
           -1.02393859e+00,  3.98931423e-01, -2.40990234e-01,  3.98625261e-01,
           -4.56680223e-01, -8.15313763e-01, -3.02801085e+00,  1.58812325e-01,
           -1.81186496e+00, -1.70284550e+00,  1.07978599e+00, -7.62883614e-01,
            7.60781157e-01,  1.01509645e+00, -1.76766728e+00, -9.55427093e-01,
           -8.56184178e-01, -9.34960413e-01,  1.70741286e+00, -3.61080820e-01,
           -8.53051459e-02,  9.48934911e-01,  6.75218872e-01,  3.18068097e-01,
           -1.13969535e+00,  1.08117830e+00, -2.66616917e-01,  1.28477001e+00,
           -1.03185181e+00,  1.46781042e+00,  7.68597605e-01,  7.05457974e-01,
           -6.07831397e-01,  1.88543008e+00, -1.91448793e-01, -1.63848205e+00,
            1.16217296e-01, -5.37156619e-01, -4.95315198e-01,  5.58649334e-01,
           -4.07425762e-01,  5.37573114e-01, -2.08334077e+00,  4.26754101e-01,
            9.20232153e-02,  1.46194466e+00, -7.97808779e-01, -5.48215245e-01,
            1.29974044e-01,  2.10775829e+00,  1.19107983e+00,  1.26575182e+00,
           -3.40195888e-01,  1.21018850e+00, -4.93333216e-01, -1.06875569e+00,
           -1.29589921e+00,  4.61362833e-01,  1.31927752e+00, -9.91028307e-01,
            1.06951921e-01,  4.44119143e-01, -3.43846659e-01,  2.27398343e-01,
            1.14119237e+00, -1.73834363e-01, -5.63045387e-01, -4.99352970e-01,
           -3.17405624e-01, -6.21089571e-01,  1.20241172e-01, -2.27903080e+00,
           -5.82242509e-01,  7.93208620e-01, -1.25204198e+00,  1.39515847e+00,
            5.08447690e-03,  1.80056901e+00,  2.41848384e-01,  1.16358839e-01,
           -7.29011047e-01, -6.16949700e-01, -1.22291296e+00,  6.04217644e-01,
            8.64994088e-01,  3.69541554e-01, -2.09416802e-01,  3.11833949e-01,
           -9.77445884e-01, -1.43308923e-01,  4.17697690e-01,  1.77526762e-01])




```python
cats = pd.qcut(data,4)
```


```python
cats
```




    [(-0.666, -0.0183], (0.659, 2.928], (-0.666, -0.0183], (-0.0183, 0.659], (-0.666, -0.0183], ..., (-0.0183, 0.659], (-3.029, -0.666], (-0.666, -0.0183], (-0.0183, 0.659], (-0.0183, 0.659]]
    Length: 1000
    Categories (4, interval[float64, right]): [(-3.029, -0.666] < (-0.666, -0.0183] < (-0.0183, 0.659] < (0.659, 2.928]]




```python
pd.value_counts(cats)
```




    (-3.029, -0.666]     250
    (-0.666, -0.0183]    250
    (-0.0183, 0.659]     250
    (0.659, 2.928]       250
    dtype: int64




```python
pd.qcut(data,[0,0.1,0.5,0.9,1.])
```




    [(-1.258, -0.0183], (-0.0183, 1.308], (-1.258, -0.0183], (-0.0183, 1.308], (-1.258, -0.0183], ..., (-0.0183, 1.308], (-1.258, -0.0183], (-1.258, -0.0183], (-0.0183, 1.308], (-0.0183, 1.308]]
    Length: 1000
    Categories (4, interval[float64, right]): [(-3.029, -1.258] < (-1.258, -0.0183] < (-0.0183, 1.308] < (1.308, 2.928]]




```python
data = pd.DataFrame(np.random.randn(1000,4))
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>-0.091367</td>
      <td>-0.490732</td>
      <td>0.583050</td>
      <td>-0.904303</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.182414</td>
      <td>1.247075</td>
      <td>-0.313419</td>
      <td>-1.585639</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.815042</td>
      <td>-0.244059</td>
      <td>-0.045383</td>
      <td>0.544301</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.431199</td>
      <td>-0.067098</td>
      <td>-0.771752</td>
      <td>0.179053</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1.453512</td>
      <td>-1.168323</td>
      <td>0.485646</td>
      <td>0.735551</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>995</th>
      <td>0.777125</td>
      <td>-0.248208</td>
      <td>-0.210640</td>
      <td>1.126688</td>
    </tr>
    <tr>
      <th>996</th>
      <td>-0.324432</td>
      <td>-0.309285</td>
      <td>0.583729</td>
      <td>0.232719</td>
    </tr>
    <tr>
      <th>997</th>
      <td>1.096304</td>
      <td>0.770054</td>
      <td>-0.000008</td>
      <td>1.177936</td>
    </tr>
    <tr>
      <th>998</th>
      <td>-1.630431</td>
      <td>-0.958190</td>
      <td>-0.093315</td>
      <td>-0.383618</td>
    </tr>
    <tr>
      <th>999</th>
      <td>-1.077638</td>
      <td>-0.986645</td>
      <td>-1.188236</td>
      <td>-0.210087</td>
    </tr>
  </tbody>
</table>
<p>1000 rows × 4 columns</p>
</div>




```python
data.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>1000.000000</td>
      <td>1000.000000</td>
      <td>1000.000000</td>
      <td>1000.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.008143</td>
      <td>-0.008926</td>
      <td>-0.014264</td>
      <td>0.001452</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.010098</td>
      <td>1.013174</td>
      <td>1.013407</td>
      <td>1.018677</td>
    </tr>
    <tr>
      <th>min</th>
      <td>-3.354612</td>
      <td>-3.519365</td>
      <td>-2.848090</td>
      <td>-2.869848</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>-0.713990</td>
      <td>-0.684854</td>
      <td>-0.725146</td>
      <td>-0.683503</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>-0.020314</td>
      <td>-0.039448</td>
      <td>-0.001628</td>
      <td>0.033012</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.676281</td>
      <td>0.680638</td>
      <td>0.648558</td>
      <td>0.690318</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2.943606</td>
      <td>3.086161</td>
      <td>2.932002</td>
      <td>3.079780</td>
    </tr>
  </tbody>
</table>
</div>




```python
col =data[2]
```


```python
col[np.abs(col>3)]
```




    Series([], Name: 2, dtype: float64)




```python
col[np.abs(col) > 3]

```




    Series([], Name: 2, dtype: float64)




```python
 col[np.abs(col) > 2]
```




    6      2.198019
    20     2.607792
    32    -2.197895
    52    -2.187703
    55     2.118065
             ...   
    926    2.003344
    947    2.152865
    948   -2.076216
    964   -2.104567
    990    2.675640
    Name: 2, Length: 52, dtype: float64




```python
data[(np.abs(data)>3).any(1)]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10</th>
      <td>0.917395</td>
      <td>-1.943511</td>
      <td>0.203883</td>
      <td>3.079780</td>
    </tr>
    <tr>
      <th>84</th>
      <td>-3.354612</td>
      <td>0.746286</td>
      <td>-1.192985</td>
      <td>-0.050977</td>
    </tr>
    <tr>
      <th>114</th>
      <td>-0.715959</td>
      <td>3.075408</td>
      <td>-0.149131</td>
      <td>-1.168391</td>
    </tr>
    <tr>
      <th>117</th>
      <td>1.082416</td>
      <td>-3.519365</td>
      <td>0.230001</td>
      <td>-0.398592</td>
    </tr>
    <tr>
      <th>487</th>
      <td>-0.349598</td>
      <td>3.086161</td>
      <td>-1.156030</td>
      <td>0.607975</td>
    </tr>
  </tbody>
</table>
</div>




```python
data = pd.Series(np.random.randn(9),
                index=[['a','a','a','b','b','c','c','d','d'],
                      [1,2,3,1,3,1,2,2,3]])
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [1], in <cell line: 1>()
    ----> 1 data = pd.Series(np.random.randn(9),
          2                 index=[['a','a','a','b','b','c','c','d','d'],
          3                       [1,2,3,1,3,1,2,2,3]])
    

    NameError: name 'pd' is not defined



```python
import importlib
```


```python
importlib.reroad(numpy)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    Input In [3], in <cell line: 1>()
    ----> 1 importlib.reroad(numpy)
    

    AttributeError: module 'importlib' has no attribute 'reroad'



```python
importlib.reload(numpy)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [4], in <cell line: 1>()
    ----> 1 importlib.reload(numpy)
    

    NameError: name 'numpy' is not defined



```python
import numpy as np
```


```python
import pandas as pd
```


```python
importlib.reload(np)
```

    D:\Anaconda3\envs\pytorch\lib\importlib\__init__.py:169: UserWarning: The NumPy module was reloaded (imported a second time). This can in some cases result in small but subtle issues and is discouraged.
      _bootstrap._exec(spec, module)
    




    <module 'numpy' from 'D:\\Anaconda3\\envs\\pytorch\\lib\\site-packages\\numpy\\__init__.py'>




```python
importlib.reload(numpy)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [8], in <cell line: 1>()
    ----> 1 importlib.reload(numpy)
    

    NameError: name 'numpy' is not defined



```python
data
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [9], in <cell line: 1>()
    ----> 1 data
    

    NameError: name 'data' is not defined



```python
data
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [10], in <cell line: 1>()
    ----> 1 data
    

    NameError: name 'data' is not defined



```python
import numpy as np
```


```python
import pandas as pd
```


```python
data = pd.Series(np.random.randn(9),
   ...:                  index=[['a', 'a', 'a', 'b', 'b', 'c', 'c', 'd', 'd'],
   ...:                         [1, 2, 3, 1, 3, 1, 2, 2, 3]])
```


```python
data
```




    a  1   -1.793849
       2    0.169913
       3    1.243042
    b  1    0.688077
       3   -0.513150
    c  1   -1.051628
       2    0.011543
    d  2   -0.238163
       3   -1.905288
    dtype: float64




```python
data.index
```




    MultiIndex([('a', 1),
                ('a', 2),
                ('a', 3),
                ('b', 1),
                ('b', 3),
                ('c', 1),
                ('c', 2),
                ('d', 2),
                ('d', 3)],
               )




```python
data['b']
```




    1    0.688077
    3   -0.513150
    dtype: float64




```python
data['a']
```




    1   -1.793849
    2    0.169913
    3    1.243042
    dtype: float64




```python
data.loc[['b','d']]
```




    b  1    0.688077
       3   -0.513150
    d  2   -0.238163
       3   -1.905288
    dtype: float64




```python
data.oc[:,2]
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    Input In [19], in <cell line: 1>()
    ----> 1 data.oc[:,2]
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\core\generic.py:5575, in NDFrame.__getattr__(self, name)
       5568 if (
       5569     name not in self._internal_names_set
       5570     and name not in self._metadata
       5571     and name not in self._accessors
       5572     and self._info_axis._can_hold_identifiers_and_holds_name(name)
       5573 ):
       5574     return self[name]
    -> 5575 return object.__getattribute__(self, name)
    

    AttributeError: 'Series' object has no attribute 'oc'



```python
data.loc[:,2]
```




    a    0.169913
    c    0.011543
    d   -0.238163
    dtype: float64




```python
data.unstack()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>-1.793849</td>
      <td>0.169913</td>
      <td>1.243042</td>
    </tr>
    <tr>
      <th>b</th>
      <td>0.688077</td>
      <td>NaN</td>
      <td>-0.513150</td>
    </tr>
    <tr>
      <th>c</th>
      <td>-1.051628</td>
      <td>0.011543</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>d</th>
      <td>NaN</td>
      <td>-0.238163</td>
      <td>-1.905288</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.unstack().stack()
```




    a  1   -1.793849
       2    0.169913
       3    1.243042
    b  1    0.688077
       3   -0.513150
    c  1   -1.051628
       2    0.011543
    d  2   -0.238163
       3   -1.905288
    dtype: float64




```python
data = pd.DataFrame(np.arange(6).reshape((2, 3)),
   .....:                     index=pd.Index(['Ohio','Colorado'], name='state'),
   .....:                     columns=pd.Index(['one', 'two', 'three'],
   .....:                     name='number'))
```


```python
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>number</th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
    </tr>
    <tr>
      <th>state</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
result = data.stack()
```


```python
result
```




    state     number
    Ohio      one       0
              two       1
              three     2
    Colorado  one       3
              two       4
              three     5
    dtype: int32




```python
result.unstack()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>number</th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
    </tr>
    <tr>
      <th>state</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
reuslut.unstack(0)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Input In [28], in <cell line: 1>()
    ----> 1 reuslut.unstack(0)
    

    NameError: name 'reuslut' is not defined



```python
result.unstack(0)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>state</th>
      <th>Ohio</th>
      <th>Colorado</th>
    </tr>
    <tr>
      <th>number</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>one</th>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>two</th>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>three</th>
      <td>2</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
result.unstack(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>number</th>
      <th>one</th>
      <th>two</th>
      <th>three</th>
    </tr>
    <tr>
      <th>state</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ohio</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Colorado</th>
      <td>3</td>
      <td>4</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
df = pd.DataFrame({'key': ['foo', 'bar', 'baz'],
   .....:                    'A': [1, 2, 3],
   .....:                    'B': [4, 5, 6],
   .....:                    'C': [7, 8, 9]})
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>foo</td>
      <td>1</td>
      <td>4</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>bar</td>
      <td>2</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>2</th>
      <td>baz</td>
      <td>3</td>
      <td>6</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
melted = pd.melt(df, ['key'])
```


```python
melted
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>variable</th>
      <th>value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>foo</td>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>bar</td>
      <td>A</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>baz</td>
      <td>A</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>foo</td>
      <td>B</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>bar</td>
      <td>B</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>baz</td>
      <td>B</td>
      <td>6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>foo</td>
      <td>C</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>bar</td>
      <td>C</td>
      <td>8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>baz</td>
      <td>C</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
melted2 = pd.melt(df, ['value'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Input In [35], in <cell line: 1>()
    ----> 1 melted2 = pd.melt(df, ['value'])
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\core\reshape\melt.py:77, in melt(frame, id_vars, value_vars, var_name, value_name, col_level, ignore_index)
         75         missing = Index(com.flatten(id_vars)).difference(cols)
         76         if not missing.empty:
    ---> 77             raise KeyError(
         78                 "The following 'id_vars' are not present "
         79                 f"in the DataFrame: {list(missing)}"
         80             )
         81 else:
         82     id_vars = []
    

    KeyError: "The following 'id_vars' are not present in the DataFrame: ['value']"



```python
melted2 = pd.melt(df, ['variable'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Input In [36], in <cell line: 1>()
    ----> 1 melted2 = pd.melt(df, ['variable'])
    

    File D:\Anaconda3\envs\pytorch\lib\site-packages\pandas\core\reshape\melt.py:77, in melt(frame, id_vars, value_vars, var_name, value_name, col_level, ignore_index)
         75         missing = Index(com.flatten(id_vars)).difference(cols)
         76         if not missing.empty:
    ---> 77             raise KeyError(
         78                 "The following 'id_vars' are not present "
         79                 f"in the DataFrame: {list(missing)}"
         80             )
         81 else:
         82     id_vars = []
    

    KeyError: "The following 'id_vars' are not present in the DataFrame: ['variable']"



```python
reshaped = melted.pivot('key', 'variable', 'value')

```


```python
reshaped
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>variable</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
    <tr>
      <th>key</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>bar</th>
      <td>2</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>baz</th>
      <td>3</td>
      <td>6</td>
      <td>9</td>
    </tr>
    <tr>
      <th>foo</th>
      <td>1</td>
      <td>4</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>




```python
reshaped.reset_index()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>variable</th>
      <th>key</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>bar</td>
      <td>2</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>1</th>
      <td>baz</td>
      <td>3</td>
      <td>6</td>
      <td>9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>foo</td>
      <td>1</td>
      <td>4</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.melt(df, id_vars=['key'], value_vars=['A', 'B'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>key</th>
      <th>variable</th>
      <th>value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>foo</td>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>bar</td>
      <td>A</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>baz</td>
      <td>A</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>foo</td>
      <td>B</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>bar</td>
      <td>B</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>baz</td>
      <td>B</td>
      <td>6</td>
    </tr>
  </tbody>
</table>
</div>




```python
pand
```
