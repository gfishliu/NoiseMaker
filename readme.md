# About
《共享噪音》（Noise Maker）是我做的一个基于Tensorflow的自动生成儿歌的作品。

[点此试听Noise Maker生成的音乐](http://v.youku.com/v_show/id_XMzE1MTU3NTUzNg==.html?spm=a2hzp.8244740.0.0)

如果大家觉得我这个程序做的不错，就请多多star+关注+分享哦！

# 程序运行方法
* 安装依赖包
```
pip3 install -r whl_is_sb.txt
```
* 运行前的准备
```
cd code
mkdir log
mkdir log/sess
```
* 训练样本并生成一段测试音乐
```
python3 main.py
```
* ```settings.py```里面有一个变量```FLAG_IS_DEBUG```。这个变量为True时，训练时间在十分钟左右，但是有比较高的概率会生成一段很烂的音乐。当这个变量为False时，训练师间在一小时左右，但是生成的音乐质量会稍微高一些。
* 运行结束之后，会发现文件夹中多了一个output.mid，这个文件就是生成的音乐哦。

# 作品简述

* 生成音乐所使用到的主要算法是LSTM、HMM和K-Means。
* 目前的这个版本（0.94）可以生成一个带有主旋律，和弦，同时包含了鼓点、bass、钢琴、弦乐和加花五种音色的伴奏。
* 关于工程文件：code文件夹里面的是源代码，data.db是训练所用的数据（我把midi音乐按一定规则编码之后存到了sqlite3数据库文件中）。
* 关于数据：我从网上找了169首儿歌作为训练样本。因为儿歌的midi文件比较好下载到，而且儿歌的主旋律/和弦走向/鼓点等都相对比较简单，所以在这个版本中，我选择了儿歌作为训练样本。
* 这个东西接下来应该会有续作。对它有什么批评意见的话可以联系我，我还是很乐意听到改进意见的。

# Q/A

* 如果程序不能运行出bug怎么办？
    * 跟我反馈。
* 生成的音乐太难听无法忍受怎么办？
    * 当然是选择原谅它。
