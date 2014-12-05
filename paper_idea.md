---
title: Paper Proposal
author: Pengfei Zhang
mode : selfcontained
framework: revealjs
hitheme : zenburn
revealjs:
  theme: default
  transition: fade
  center: "true"
url: {lib: "."}
bootstrap:
  theme: amelia
---

## 研究点讨论

### Measurement Enhanced Cloud Network - Traffic Statistical Techiques


<small> Created by [张鹏飞](http://pengfei-zhang.com) @ [上海交通大学](http://omnilab.sjtu.edu.cn) </small>

---

## Outline

- Prediction
- Traffic Classification
- Abnormal Detection
- 思考

--- &vertical

## Prediction

概述： 流量预测的目的和重要性不言而喻，但最重要的矛盾时预测时长与准确度的矛盾

***


### Internet  vs   Cloud


- Cloud中的流量模式更明显区分为东西／南北
- Cloud运营者对用户组位置具有感知和控制能力


***

## Time Scale

### Short Term vs Long Term

- 短期预测较为成熟，侧重时间序列预测，主要关注准确度
- 长期预测较为困难，天然难以达到精准，侧重pattern, statistic

<small> [Long-Term Forecasting of Internet Backbone Traffic: Observations and Initial Models](./papers/backbone long term.pdf) </small>
***

## 预测方法

- AR,MA,ARMA,ARIMA

<small> [A Prediction Method of Network Traffic Using Time Series Models](http://link.springer.com/chapter/10.1007%2F11751595_26#page-1) </small>

- Neural Network

<small> [New Models for Long-Term Internet Traffic Forecasting Using Artificial Neural Networks and Flow Based Information](./papers/NN prediction.pdf) </small>

***

## 预测方面的思考

- 不拼准确度，算法
- 找准预测的目的 (控制对象)
- 针对云计算／SDN环境进行预测方式的改进 (Flow -- Matrix)

---

## Classification

目前的Traffic Classification多基于Flow特性进行App的分类识别,

<small> [A Survey of Techniques for Internet Traffic Classification using Machine Learning](./papers/classification survey.pdf) </small>


--- &vertical

## Abnormal Detection

- 异常检测与Classification是分不开的，可以说是分类的一种应用

- 主要应用是入侵检测，最常见的是DDOS



***

## 常用方法

- 统计PDF
- Flow 特征
- Neural Network

<small> [Network Intrusion and Fault Detection: A Statistical Anomaly Approach](./papers/statistical anomaly approach.pdf) </small>

***

## 异常检测思考

- 目前主要是攻击检测
- 可否做App Performance Abnormal Detection?
- 延伸一步，是否可做App Classification?


--- &vertical

## 关于Traffic Matrix

- 传统流量分析(分类，检测，预测)都以流为单位
- 矩阵能更好地反映集群的特性

***

## 矩阵处理

- 全网拓扑矩阵: 初始数据，规模大，但信息完整

<small> [Cicada](https://www.usenix.org/conference/hotcloud14/workshop-program/presentation/lacurts) </small>

- Per Tenant Matrix: 规模小，但仅能分析用户行为，应用特性

---

## 整体思考: 可以做的点

- Flow Monitoring -- Matrix Monitoring
- Time Series Prediction -- Statistical Prediction
- Flow Classification -- App Performance Analysis
- Flow Control -- Statistical based control (Near Time)


