# Twitter数据爬取，清洗与分析

## 项目背景

本项目将要整理 (以及分析和可视化) 的数据集是推特用户 @dog_rates 的档案, 推特昵称为 WeRateDogs。WeRateDogs 是一个推特主，他以诙谐幽默的方式对人们的宠物狗评分。这些评分通常以 10 作为分母。但是分子则一般大于 10：11/10、12/10、13/10 等等。WeRateDogs 拥有四百多万关注者，曾受到国际媒体的报道。

WeRateDogs 下载了他们的推特档案，专门为本项目使用。这个档案是基本的推特数据（推特 ID、时间戳、推特文本等），包含了截止到 2017 年 4 月 1 日的 5000 多条推特。

## 项目目标

我们在这个项目中的任务如下：

- WeRateDogs数据整理，其中包括： 收集数据 评估数据 清洗数据
- 对清洗过的数据进行储存、分析和可视化 
- 形成书面报告 1) 数据整理工作 和 2) 数据分析和可视化

## 项目步骤


#### 1. 收集以下三份数据，为三种不同的文件类型：

- WeRateDogs 的推特档案。这个数据文件是直接提供的，文件名为`twitter_archive_enhanced.csv`
- 推特图像的预测数据，即根据神经网络CNN，对出现在每个推特中狗的品种（或其他物体、动物等）进行预测的结果。这个文件需要使用 Python 的 Requests 库和以下提供的 [URL](https://raw.githubusercontent.com/udacity/new-dand-advanced-china/master/%E6%95%B0%E6%8D%AE%E6%B8%85%E6%B4%97/WeRateDogs%E9%A1%B9%E7%9B%AE/image-predictions.tsv) 来进行编程下载.
- 每条推特的额外附加数据，至少要包含转发数（`retweet_count`）和喜欢数（`favorite_count`），还可以收集任何觉得有趣的字段。使用 WeRateDogs 推特档案中的推特 ID，使用 Python [Tweepy 库](http://www.tweepy.org/)查询 API 中每个推特的 JSON 数据，把所有 JSON 数据存储到一个名为 `tweet_json.txt` 的文件中。

#### 2. 对项目数据进行评估

收集上述三个数据集之后，使用目测评估和编程评估的方式，对数据进行质量和清洁度的评估。在 `wrangle_act.ipynb`中记录评估过程和结果，最终列出至少 8 个质量问题 和 2 个清洁度问题。

#### 3. 对项目数据进行清洗

对在评估时列出的每个问题进行清洗。在 `wrangle_act.ipynb` 展示清洗的过程。结果应该为一个优质干净整洁的主数据集（pandas DataFrame 类型） （如果都是以推特 ID 为观察对象的一些特征列，则清理最终只能有一个主数据集，如果有其他观察对象及其对应的特征字段，可以创建其他的数据集，同样需要清理）。

#### 4. 对项目数据进行存储、分析和可视化

将清理后的数据集存储到 CSV 文件中，命名为` twitter_archive_master.csv`。

在 `wrangle_act.ipynb`中对清洗后的数据进行分析和可视化。必须生成至少 3 个结论和 1 个可视化。

### 软件的安装
- pandas
- numpy
- requests
- tweepy
- json
- os

###文件描述

- wrange_act.ipynb: 完整的数据爬取，清洗及分析代码文件
- wrangle_report.pdf: 关于数据爬取，清洗与分析的报告（不包含代码）
- act_report.pdf: 对整理后的数据的可视化分析报告（不包含代码）
- twitter-archive-enhanced.csv：推特档案数据集，包含了截止到 2017 年 4 月 1 日的 5000 多条推特
- image-predictions.tsv：针对推特图像的预测数据，即根据神经网络CNN，对出现在每个推特中狗的品种进行预测的数据集
- tweet_json.txt: 推特的额外附加数据集，包含转发数和喜欢数列
- README.md

