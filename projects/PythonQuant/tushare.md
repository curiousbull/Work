安装
====

``` python
pip install tushare
```

获取行情
========

简单的获取行情
--------------

``` python
import tushare as ts

# 获取浦发银行的历史行情
ts.get_hist_data('600000')
```

获取指定日期的行情
------------------

``` python
import tushare as ts

# 获取从 2015-12-03 到 2016-12-03 浦发银行行情
ts.get_hist_data('600000',start='2015-12-03',end='2016-12-03')
```

获取复权历史数据
----------------

``` python
import tushare as ts

ts.get_h_data('600000') #前复权
ts.get_h_data('600000',autype='hfq') #后复权
ts.get_h_data('600000',autype=None) #不复权
ts.get_h_data('600000',start='2015-12-03',end='2016-12-03') #两个历史时期的前复权数据
ts.get_h_data('600000',start='2015-12-03',end='2016-12-03',autype='hfq') #两个历史时期的后复权数据
```

获取最近一个交易日所有股票数据
------------------------------

``` python
import tushare as ts

ts.get_today_all()
```

获取历史分笔数据
----------------

``` python
import tushare as ts

ts.get_tick_data('600000',date='2015-12-03')
```

获取实时交易数据
----------------

``` python
import tushare as ts

ts.get_realtime_quotes('600000')
```

如果需要一次获取多支股票 (最好不要一次超过三十支)

``` python
import tushare as ts

ts.get_realtime_quotes(['600000','600666','000333'])
```
