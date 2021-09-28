# temp
Temporary stuff that worth saving

## electron_clouds
用于绘制氢原子各个原子轨道的电子云图。

采用蒙特卡洛方法取10000个点，因此每个数据都是10000行。每一行的前三个数分别为电子的x, y, z坐标，最后一个数表示轨道波函数在(x, y, z)处的符号——1为正，-1为负。

采样在有限空间内进行，即r=sqrt(x^2+y^2+z^2)有上限。而且由于绘图窗口大小限制，三坐标均按一定比例缩小。采样时所用的参数为：

| 主量子数 | r上限 | 缩小比例  |
| ------  | ----- | -------- |
| 1       | 10    | 1/2      |
| 2       | 15    | 1/3      |
| 3       | 30    | 1/6      |
| 4       | 50    | 1/10     |
