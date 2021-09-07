## 基于深度学习的电影推荐系统 

`Author: YUAN Yanzhe`

该repo是香港科技大学(HKUST) MSBD5001 Data Analysis的Term Project: *[Deep Learning Methods for Movie Recommendation](https://github.com/Jackthebighead/Movie-Recommendation-System-Based-on-Deep-Learning/blob/master/docs/report.pdf)*

本项目使用MovieLens1M数据集，将两类深度学习模型融入传统推荐模型思想中（基于邻域的模型：e.g. user-based CF，基于隐变量的模型：e.g. SVD）实现电影推荐，提升效果。

- 基于Auto Encoder (AE)，Variational Auto Encoder (VAE)的模型。对评分矩阵进行预测填补。

- 基于TextCNN和BERT处理文本信息，与经NN处理的meta data结合进行预测。

本项目[数据集zip](https://github.com/Jackthebighead/Movie-Recommendation-System-Based-on-Deep-Learning/tree/master/data)，
本项目的[文档](https://github.com/Jackthebighead/Movie-Recommendation-System-Based-on-Deep-Learning/tree/master/docs)，
本项目大部分在**Google Colab**环境下运行，少部分在Macbook Pro的CPU上运行，代码中的目录请根据自己的实际目录进行修改。  

## **Models:**

#### Auto Encoder

<img src="assets/auto%20encoder.png" width="400" height="300">

#### Variational Auto Encoder

<img src="assets/variational%20auto%20encoder.png" width="400" height="300">

#### BERT-based

<img src="assets/bert-based.PNG" width="600" height="300">



## **Experimental Results:**

- **Auto Encoder: training loss and validation loss (MSE)**

<img src="assets/auto%20encoder%20result.png" width="460" height="280">

- **VAE: training loss and validation loss (MSE)**

<img src="assets/variational%20auto%20encoder%20result.png" width="450" height="280">

- **BERT-based: training loss and validation loss (MSE)**

<img src="assets/bert-based%20result.png" width="800" height="300">

- **Comparison**

 Model | test MSE loss  
 ---- | -----  
 Item-based* | 3.4010 
 User-based* | 3.1431 
 SVD* | 2.4416 
 Auto Encoder | 1.0837 
 Variational Auto Encoder | 0.9956 
 TextCNN-based | 0.7521 
 **BERT-based** | **0.7507** 

注：* 代表从[https://www.cnblogs.com/lqerio/p/11193471.html](https://www.cnblogs.com/lqerio/p/11193471.html) 获得

