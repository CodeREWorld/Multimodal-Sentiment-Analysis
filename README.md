# 基于tensorflow实现的多模态情感分析


## 多模态情感分析项目介绍

使用多模态模型来进行情感识别。输入有文本（包括emojis）、语音、图片和视频，根据这些内容，我们设计了一个分层方法，从一模态向量到双模态向量，再从双模态向量到三模态向量。最后我们用softmax layer把这些特征向量分成4种情感：喜、怒、哀和其他。与普通的情感分类不同的是，我们引入了更多的数据源，进行多模态识别。最后的情感分类与大众的正向、负向、中性不同，我们分成喜、怒、哀和其他，更好地进行用户分层和对标。


## 环境部署

python3.6+tensorflow1.7+cpu/gpu


## 数据集

-IEMOCAP数据集: 描述交互式情绪二元运动捕捉（iemocap）数据库是一个动作、多模式和多峰值的数据库，在南加州大学的Sail实验室收集。它包含大约12小时的视听数据，包括视频、语音、面部运动捕捉、文本转录。

6 classes: happy/sad/neutral/angry/excited/frustrated<br>
Raw Features: dataset/iemocap/raw/IEMOCAP_features_raw.pkl (Pickle files) <br>
The file contains:  
videoIDs[vid] = List of utterance IDs in this video in the order of occurance <br>
videoSpeakers[vid] = List of speaker turns. e.g. [M, M, F, M, F]. here M = Male, F = Female <br>
videoText[vid] = List of textual features for each utterance in video vid. <br>
videoAudio[vid] = List of audio features for each utterance in video vid. <br>
videoVisual[vid] = List of visual features for each utterance in video vid. <br>
videoLabels[vid] = List of label indices for each utterance in video vid. <br>
videoSentence[vid] = List of sentences for each utterance in video vid. <br>
trainVid =  List of videos (videos IDs) in train set. <br>
testVid =  List of videos (videos IDs) in test set. <br>

-MOSEI数据集: 由来自1000多个YouTube身份和200个主题的23500句话组成。

3 classes: positive/negative/neutral <br>
Raw Features: (Pickle files) <br>
Audio: dataset/mosei/raw/audio_3way.pickle <br>
Text: dataset/mosei/raw/text_3way.pickle <br>
Video: dataset/mosei/raw/video_3way.pickle <br>

-MOSI数据集:英文的多模态情感数据集，数据集中含有文本、语音和视频三种模态的信息，有2199个样本

2 classes: Positive/Negative <br>
Raw Features: (Pickle files) <br>
Audio: dataset/mosi/raw/audio_2way.pickle <br>
Text: dataset/mosi/raw/text_2way.pickle <br>
Video: dataset/mosi/raw/video_2way.pickle <br>


## Citation 
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
