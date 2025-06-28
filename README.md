<p align="center">
  <h1 align="center">Chat Rwkv Language Model</h1>
  <p align="center">
    <strong>English</strong> | <a href="README_ZH.md">简体中文</a>
  </p>
</p>

## Table of Contents

- [Repository Introduction](#project-introduction)
- [Prerequisites](#prerequisites)
- [Image Description](#image-description)
- [Getting Help](#getting-help)
- [How to Contribute](#how-to-contribute)

## Project Introduction
[chatrwkv](https://github.com/BlinkDL/ChatRWKV) ChatRWKV is an open-source large language model based on an innovative architecture. Its core feature is the combination of the efficient inference of recurrent neural networks (RNNs) and the parallel training advantages of Transformers, offering performance comparable to mainstream Transformer models.

**Core Architecture and Technical Features:**
1. It adopts a 100% pure RNN architecture, achieving **linear computational complexity**, which significantly reduces memory usage and time consumption during inference. The model has a constant memory footprint when processing long sequences, with the computational volume increasing linearly, thus solving the long-context processing bottleneck of Transformers.
2. Through the **Time Mixer** and **Channel Mixer** modules, it integrates a mechanism similar to attention (RWKV vectors), supporting parallel processing during the training phase and breaking through the limitation that traditional RNNs cannot be trained efficiently.
3. Its inference speed is 40% faster than that of Transformers optimized with Flash Attention, with 40% less video memory usage and only half the energy consumption of Transformer models of the same scale (e.g., LLaMA).
4. It supports **ultra-long context processing** (e.g., over 20K tokens) and maintains state coherence in multi-round conversations.

The open-source image product provided by this project, [**`RWKV Large Language Model`**](https://marketplace.huaweicloud.com/intl/hidden/contents/ac451ac5-9ae2-40b0-b8c9-81351789b96d)  has the RWKV-4-Pile-1B5-EngChn-test4-20230115.pth model and its related operating environment pre-installed, and also provides a deployment template. Come and follow the usage guide to easily start an "out-of-the-box" and efficient experience!

> **System requirements are as follows:**
> - CPU: 4vCPUs or higher
> - RAM: 16GB or larger
> - Disk: At least 40GB

## Prerequisites
[Register a Huawei account and activate Huawei Cloud](https://support.huaweicloud.com/usermanual-account/account_id_001.html)

## Image Description

| Image Specification | Feature Description | Remarks |
| --- | --- | --- |
| [RWKV-4-Pile-1B5-kunpeng-HCE](https://github.com/HuaweiCloudDeveloper/chatRWKV-image/tree/RWKV-4-Pile-1B5-kunpeng) | Installed and deployed based on Kunpeng servers + Huawei Cloud EulerOS 2.0 64-bit |  |

## Getting Help
- For more questions, you can contact us through [issues](https://github.com/HuaweiCloudDeveloper/chatRWKV-image/issues) or the service support of the specified product in the Huawei Cloud Marketplace.
- For other open-source images, please refer to [open-source-image-repos](https://github.com/HuaweiCloudDeveloper/open-source-image-repos).

## How to Contribute
- Fork this repository and submit a merge request.
- Update README.md synchronously based on your open-source image information.