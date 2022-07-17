# RGCN 实践
RGCN主要分为 link prediction 和entity classification部分 
基本思想都是从邻居节点提取信息，但信息的使用方式在两个任务中有所不同
实体分类: assign types and categorical properties to entities 
实体分类是通过在实体(节点)的最后嵌入处附加softmax分类器来完成的。训练是通过标准交叉熵的损失函数进行的

链路预测：recover missing triples: (subject, relation,object) 
链路预测是通过使用参数化评分函数，使用自动编码器架构重建边缘来完成的。训练使用负采样。
