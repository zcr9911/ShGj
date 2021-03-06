# ShGj
1.本项目利用Hadoop处理高校无线定位大数据,有效地将位置信息应用于学生时空行为模式挖掘，建立基于精准位置信息的行为数据挖掘计算模型。 
2.基于Hadoop计算平台，并实现对大数据进行可视化分析的Web系统,采用ssm+mysql技术。 
3.利用一些合适的算法实现校园热点区域提取、学生异常轨迹探测、人流迁徙分析及学生时空行为相似性分析推测等功能。  
4.基于学校地图API和echarts插件可视化展现。

校园热点区域提取
采用基本的K-means算法，然后在校园地图上使用热力图形式呈现

学生异常轨迹探测
采用地理接口，筛选出不在建筑物范围内的定点。

人流迁徙分析
从wifi定点数据中根据用户特性、时间特性、建筑特性，归纳出有效完整轨迹，之后采用分段轨迹聚类算法，分析校内人员轨迹迁徙状况。
在地图上使用echarts插件里的迁徙图在校园地图上动态呈现校园人群迁徙分布。

学生时空行为相似性分析推测等功能
采用基本的Word2Vec的Skip-Gram模型用于计算人员的基于时空行为的相似人群，根据人员的脱敏信息，进行分析与预测。
使用该算法的主要工作就是基于WiFi定位数据构建自己的“语料库”。
为什么可以采用Word2Vec的Skip-Gram模型的原因：
                    解决用户时空行为相似问题
    一种行为的所有用户（学号） -> 分词处理后一段语言文字
              每个用户（学号）-> 每个关键词
           用户之间的亲密程度 -> 关键词相近概率
           
以上工作，在githup上只上传了可视化web端项目，具体的数据处理流程及逻辑可以联系我，细说。

特点：
1.实现了在自己指定的地图范围上使用echerts插件，实现热力图，迁徙图。
2.基于wifi定位数据，使用了K-means算法、Word2Vec算法、轨迹分段聚类算法。
3.基于真实数据的课题实践。
4.Hadoop分布式计算的应用。
