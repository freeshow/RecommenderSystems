`fork from https://github.com/Lockvictor/MovieLens-RecSys.git`

基于Movielens-1M数据集实现的User Based Collaborative Filtering和Item Based Collaborative Filtering推荐算法

# 简介
项亮所著的《[推荐系统实践](https://book.douban.com/subject/10769749/)》一书是非常优秀的推荐系统入门书籍，但书中只描述了单步的计算如何实现，缺乏一个完整的示例来展示推荐系统从建立数据集到评估模型的整个过程，初学者学起来容易迷茫，因此我基于Movielens 1M数据集分别实现了User Based Collaborative Filtering（以下简称UserCF）和Item Based Collaborative Filtering（以下简称ItemCF）两个算法，包含“切分训练集与测试集-训练模型-推荐-评估”一整套流程，可以帮助初学者更快速地理解推荐系统中的协同过滤算法。

程序最终给出的是Precision、Recall、Coverage、Popularity四项衡量模型质量的指标，而具体的电影推荐结果并未保留，如果需要此部分数据可自行修改代码。

# 注意事项
UserCF算法中，由于用户数量多，生成的相似性矩阵也大，会占用比较多的内存，不过一般电脑都没问题。

ItemCF算法中，每次推荐都需要找出一个用户的所有电影，再为每一部电影找出最相似的电影，运算量比UserCF大，因此推荐的过程比较慢。