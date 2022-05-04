# multi-baseline
本仓库主要基于emukit和cigp，包含了NAR，LAR，HF三种方法，在原有的五个数据集的基础上增加了10个双精度数据集，详见dataset.jpg

1.运行文件，例如LAR（下面均已LAR为例），运行LAR/cigp_lar.py文件，该文件中主要包含训练，测试，以及写入csv文件，在运行
  完之后会生成一个results文件夹，再运行data_process.py文件可将results汇总，可以修改data_process.py文件，仅统计需要的数据集。

2.改变高低精度样本个数，在LAR/Exp/exp_5functions_benchmark/benchmark_setting.py中进行修改

3.改变训练参数，例如随机数种子，数据集选择，一般建议舍弃tl2，tl3，tl4三个数据集，因为这三种方法在这个三个数据集测试误差特别小，在LAR/cigp_lar.py文件中修改

tips：(可以适当改变num_iters的大小影响最终的test error)
