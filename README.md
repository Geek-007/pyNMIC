# pyRS
用python处理遥感数据

可能又是个坑

慢慢挖慢慢填

## [FY-4A计算云顶亮温](./FY-4A/FY4A_Tbb.py)<br>
国家卫星气象中心官网上提供的经纬度查找表有问题（至少4km的有问题）：
- `FY-4A数据行列号和经纬度的互相转换方法`中的`查表方法`教程pdf中说`高字节在前`其实是在后即小端存储格式；`前8字节为经度值，后8字节为纬度值`也说反了
- .gz文件应该不是标准的.gz格式，导致用gzip包无法直接打开，用7z手动解压也会提示`有效数据外包含额外数据`