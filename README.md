# Multimodal-Sentiment-Analysis
多模态融合情感分析

我们使用多模态模型来进行情感识别。输入有文本（包括emojis）、语音、图片和视频，根据这些内容，我们设计了一个分层方法，从一模态向量到双模态向量，再从双模态向量到三模态向量。最后我们用softmax layer把这些特征向量分成4种情感：喜、怒、哀和其他。与普通的情感分类不同的是，我们引入了更多的数据源，进行多模态识别。对每一种数据源使用RNN进行序列化数据处理。最后的情感分类与大众的正向、负向、中性不同，我们分成喜、怒、哀和其他，更好地进行用户分层和对标。

### Citation 
```
@inproceedings{soujanyaacl17,
  title={Context-dependent sentiment analysis in user-generated videos},
  author={Poria, Soujanya  and Cambria, Erik and Hazarika, Devamanyu and Mazumder, Navonil and Zadeh, Amir and Morency, Louis-Philippe},
  booktitle={Association for Computational Linguistics},
  year={2017}
}

@inproceedings{poriaicdm17, 
author={S. Poria and E. Cambria and D. Hazarika and N. Mazumder and A. Zadeh and L. P. Morency}, 
booktitle={2017 IEEE International Conference on Data Mining (ICDM)}, 
title={Multi-level Multiple Attentions for Contextual Multimodal Sentiment Analysis}, 
year={2017},  
pages={1033-1038}, 
keywords={data mining;feature extraction;image classification;image fusion;learning (artificial intelligence);sentiment analysis;attention-based networks;context learning;contextual information;contextual multimodal sentiment;dynamic feature fusion;multilevel multiple attentions;multimodal sentiment analysis;recurrent model;utterances;videos;Context modeling;Feature extraction;Fuses;Sentiment analysis;Social network services;Videos;Visualization}, 
doi={10.1109/ICDM.2017.134}, 
month={Nov},}
```
