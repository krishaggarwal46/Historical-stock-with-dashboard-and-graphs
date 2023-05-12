# Historical-stock-with-dashboard-and-graphs
-----------------------------------------
!pip install yfinance
--------------------------------
Collecting yfinance
  Downloading yfinance-0.2.18-py2.py3-none-any.whl (60 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 60.3/60.3 kB 8.0 MB/s eta 0:00:00
Requirement already satisfied: pandas>=1.3.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.3.5)
Requirement already satisfied: numpy>=1.16.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.21.6)
Requirement already satisfied: requests>=2.26 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (2.29.0)
Collecting multitasking>=0.0.7 (from yfinance)
  Downloading multitasking-0.0.11-py3-none-any.whl (8.5 kB)
Requirement already satisfied: lxml>=4.9.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (4.9.2)
Collecting appdirs>=1.4.4 (from yfinance)
  Downloading appdirs-1.4.4-py2.py3-none-any.whl (9.6 kB)
Requirement already satisfied: pytz>=2022.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (2023.3)
Collecting frozendict>=2.3.4 (from yfinance)
  Downloading frozendict-2.3.8-cp37-cp37m-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (101 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 101.7/101.7 kB 5.5 MB/s eta 0:00:00
Requirement already satisfied: cryptography>=3.3.2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (38.0.2)
Requirement already satisfied: beautifulsoup4>=4.11.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (4.11.1)
Collecting html5lib>=1.1 (from yfinance)
  Downloading html5lib-1.1-py2.py3-none-any.whl (112 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 112.2/112.2 kB 17.0 MB/s eta 0:00:00
Requirement already satisfied: soupsieve>1.2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from beautifulsoup4>=4.11.1->yfinance) (2.3.2.post1)
Requirement already satisfied: cffi>=1.12 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from cryptography>=3.3.2->yfinance) (1.15.1)
Requirement already satisfied: six>=1.9 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from html5lib>=1.1->yfinance) (1.16.0)
Requirement already satisfied: webencodings in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from html5lib>=1.1->yfinance) (0.5.1)
Requirement already satisfied: python-dateutil>=2.7.3 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from pandas>=1.3.0->yfinance) (2.8.2)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (3.1.0)
Requirement already satisfied: idna<4,>=2.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (3.4)
Requirement already satisfied: urllib3<1.27,>=1.21.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (1.26.15)
Requirement already satisfied: certifi>=2017.4.17 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (2022.12.7)
Requirement already satisfied: pycparser in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from cffi>=1.12->cryptography>=3.3.2->yfinance) (2.21)
Installing collected packages: multitasking, appdirs, html5lib, frozendict, yfinance
Successfully installed appdirs-1.4.4 frozendict-2.3.8 html5lib-1.1 multitasking-0.0.11 yfinance-0.2.18

----------------------------------------------
import yfinance as yf
import pandas as pd
import yfinance as yf
import pandas as pd
tesla_data = yf.download('TSLA', start='2018-01-01', end='2023-05-13')
[*********************100%***********************]  1 of 1 completed
tesla_data = tesla_data.reset_index()
tesla_data.to_csv('tesla_stock_data.csv', index=False)
print(tesla_data.head())

-------------------------------

import pandas as pd
import pandas as pd
url = 'https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue'
tesla_revenue = pd.read_html(url)[0]
print(tesla_revenue.tail())

---------------------------------------

!pip install yfinance

Requirement already satisfied: yfinance in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (0.2.18)
Requirement already satisfied: pandas>=1.3.0 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.3.5)
Requirement already satisfied: numpy>=1.16.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.21.6)
Requirement already satisfied: requests>=2.26 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (2.29.0)
Requirement already satisfied: multitasking>=0.0.7 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (0.0.11)
Requirement already satisfied: lxml>=4.9.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (4.9.2)
Requirement already satisfied: appdirs>=1.4.4 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.4.4)
Requirement already satisfied: pytz>=2022.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (2023.3)
Requirement already satisfied: frozendict>=2.3.4 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (2.3.8)
Requirement already satisfied: cryptography>=3.3.2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (38.0.2)
Requirement already satisfied: beautifulsoup4>=4.11.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (4.11.1)
Requirement already satisfied: html5lib>=1.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from yfinance) (1.1)
Requirement already satisfied: soupsieve>1.2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from beautifulsoup4>=4.11.1->yfinance) (2.3.2.post1)
Requirement already satisfied: cffi>=1.12 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from cryptography>=3.3.2->yfinance) (1.15.1)
Requirement already satisfied: six>=1.9 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from html5lib>=1.1->yfinance) (1.16.0)
Requirement already satisfied: webencodings in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from html5lib>=1.1->yfinance) (0.5.1)
Requirement already satisfied: python-dateutil>=2.7.3 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from pandas>=1.3.0->yfinance) (2.8.2)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (3.1.0)
Requirement already satisfied: idna<4,>=2.5 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (3.4)
Requirement already satisfied: urllib3<1.27,>=1.21.1 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (1.26.15)
Requirement already satisfied: certifi>=2017.4.17 in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from requests>=2.26->yfinance) (2022.12.7)
Requirement already satisfied: pycparser in /home/jupyterlab/conda/envs/python/lib/python3.7/site-packages (from cffi>=1.12->cryptography>=3.3.2->yfinance) (2.21)
---------------------------------------
import yfinance as yf
import pandas as pd
import yfinance as yf
import pandas as pd
gme_data = yf.download('GME', start='2018-01-01', end='2023-05-13')
[*********************100%***********************]  1 of 1 completed
gme_data = gme_data.reset_index()
gme_data.to_csv('gme_stock_data.csv', index=False)
print(gme_data.head())

------------------------------------------------


import matplotlib.pyplot as plt
def make_graph(data, title):
    plt.figure(figsize=(10, 6))
    plt.plot(data['Date'], data['Close'])
    plt.title(title)
    plt.xlabel('Date')
    plt.ylabel('Closing Price')
    plt.xticks(rotation=45)
    plt.grid(True)
    plt.show()
make_graph(tesla_data, 'Tesla Stock Data')
----------------------------------------------------

import matplotlib.pyplot as plt
def make_graph(data, title):
    plt.figure(figsize=(10, 6))
    plt.plot(data['Date'], data['Close'])
    plt.title(title)
    plt.xlabel('Date')
    plt.ylabel('Closing Price')
    plt.xticks(rotation=45)
    plt.grid(True)
    plt.show()
    make_graph(gme_data, 'GameStop Stock Data')
    ---------------------------------------------------------
