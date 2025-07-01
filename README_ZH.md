<p align="center">
  <h1 align="center">Chat Rwkv语言模型</h1>
  <p align="center">
    <a href="README.md"><strong>English</strong></a> | <strong>简体中文</strong>
  </p>
</p>

## 目录

- [仓库简介](#项目介绍)
- [前置条件](#前置条件)
- [镜像说明](#镜像说明)
- [获取帮助](#获取帮助)
- [如何贡献](#如何贡献)

## 项目介绍
‌[chatrwkv‌](https://github.com/BlinkDL/ChatRWKV) ChatRWKV是一种基于创新架构的开源大语言模型，其核心特点是将循环神经网络（RNN）的高效推理与Transformer的并行训练优势相结合，提供了媲美主流Transformer模型的性能。

**核心架构与技术特点：**
1. 采用100%纯RNN架构，实现了‌线性计算复杂度‌，显著降低了推理时的内存占用和时间消耗。模型在处理长序列时内存占用恒定，计算量线性增长，解决了Transformer的长上下文处理瓶颈。
2. 通过‌时间混合模块（Time Mixer）‌ 和‌通道混合模块（Channel Mixer）‌ ，整合类似注意力的机制（RWKV向量），支持训练阶段的并行化处理，突破了传统RNN无法高效训练的局限。
3. 推理速度比Flash Attention优化后的Transformer快40%，显存占用减少40%，能耗仅为同规模Transformer模型（如LLaMA）的一半。
4. 支持‌超长上下文处理‌（如20K tokens以上），且在多轮对话中保持状态连贯性。

本项目提供的开源镜像商品 [**`RWKV大语言模型`**](https://marketplace.huaweicloud.com/contents/99586bca-3cb8-43c3-b086-ef355db52e67#productid=OFFI1121280235914113024) 已预先安装RWKV-4-Pile-1B5-EngChn-test4-20230115.pth模型及其相关运行环境，并提供部署模板。快来参照使用指南，轻松开启“开箱即用”的高效体验吧。



> **系统要求如下：**
> - CPU: 4vCPUs 或更高
> - RAM: 16GB 或更大
> - Disk: 至少 40GB

## 前置条件
[注册华为账号并开通华为云](https://support.huaweicloud.com/usermanual-account/account_id_001.html)

## 镜像说明

| 镜像规格                                                                                                                          | 特性说明 | 备注 |
|-------------------------------------------------------------------------------------------------------------------------------| --- | --- |
| [RWKV-4-Pile-1B5-kunpeng](https://github.com/HuaweiCloudDeveloper/chatRWKV-image/tree/RWKV-4-Pile-1B5-kunpeng) | 基于鲲鹏服务器 + Huawei Cloud EulerOS 2.0 64bit 安装部署 |  |

## 获取帮助
- 更多问题可通过 [issue](https://github.com/HuaweiCloudDeveloper/chatRWKV-image/issues) 或 华为云云商店指定商品的服务支持 与我们取得联系
- 其他开源镜像可看 [open-source-image-repos](https://github.com/HuaweiCloudDeveloper/open-source-image-repos)

## 如何贡献
- Fork 此存储库并提交合并请求
- 基于您的开源镜像信息同步更新 README.md