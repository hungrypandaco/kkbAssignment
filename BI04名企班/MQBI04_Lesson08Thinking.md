# Q1 为什么股票预测问题容易出现过拟合，也就是在训练时结果很好，在真实环境中结果没那么好?

## A1 

因为我们所使用的深度学习模型是基于历史数据进行拟合的**归纳法**，而市场在变、规律在变，比如：政策的改变等突发的异常情况，会导致未来的天、周、月的规律和历史不一定相同，也就是模型无法考虑到突变情况，所以在真实环境中的结果并不一定会那么好。

# Q2 Prophet与ARMA/ARIMA相比，优势在哪些地方?
## A2

1. Prophet既可以处理线性关系，也可以处理非线性关系，它可以精准的拟合非线性的周期趋势，而ARMA/ARIMA只能处理线性关系；

2. ARMA要求时序数据是稳定的，ARIMA可以处理不稳定数据，但它要求数据点的间隔等长，如果有数据缺失，必须使用线性差值等方法填充缺失值，这将导致引入噪音，但Prophet可以直接对缺失数据进行预测，不需要提前填充缺失值，可以避免引入噪音；

3. 除了yearly、weekly、daily的周期性使用非线性拟合外，Prophet还添加了holidays，可以让模型很好的对节假日带来的活跃数据的突变进行预测；

4. 可以人工指定模型在拟合时考虑多少异常数据点。

   





