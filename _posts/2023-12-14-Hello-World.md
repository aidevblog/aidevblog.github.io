---
layout: post
title: Mamba: the novel architecture that threatens Transformers
---

Mamba is a new state space model architecture that has shown promising performance on information-dense data such as language modeling, where previous subquadratic models fall short of Transformers. In this blog post, we will explore the key features of Mamba and its potential applications.

## Introduction
Mamba is a linear-time sequence modeling architecture that uses selective state spaces to achieve state-of-the-art performance across several modalities such as language, audio, and genomics. The architecture is designed to address the computational inefficiency of the Transformer architecture on long sequences. Mamba achieves fast inference (5 × higher throughput than Transformers) and linear scaling in sequence length, and its performance improves on real data up to million-length sequences.

## Background
The Transformer architecture and its core attention module are the foundation models that power most of the exciting applications in deep learning. However, many subquadratic-time architectures such as linear attention, gated convolution and recurrent models, and structured state space models (SSMs) have been developed to address Transformers' computational inefficiency on long sequences. These models have not performed as well as attention on important modalities such as language, however, which is what Mamba attempts to address.

## Key Features
Mamba's key features include:
- Selective state space models: Mamba uses selective state spaces to perform content-based reasoning. As the name suggests, these selective state space models "select" which information to propagate and which information to forget when infering the next token in the sequence. These models are part of the trainable parts of the Mamba model.
- Hardware-aware parallel algorithm: Mamba's selective SSMs are integrated into a simplified end-to-end neural network architecture without attention or even MLP blocks. The model enjoys fast inference and linear scaling in sequence length, and its performance improves on real data up to million-length sequences. 
- State-of-the-art performance: Mamba achieves state-of-the-art performance across several modalities such as language, audio, and genomics. On language modeling, our Mamba-3B model outperforms Transformers of the same size and matches Transformers twice its size, both in pretraining and downstream evaluation.

## Applications
You might be thinking: what is this architecture even good for? Mamba has several potential applications, including:
- Language modeling: Mamba's state-of-the-art performance on language modeling makes it an ideal choice for natural language processing tasks such as text classification, sentiment analysis, and machine translation.
- Audio processing: Mamba's ability to handle long sequences makes it a promising architecture for audio processing tasks such as speech recognition and music generation.
- Genomics: Mamba's ability to handle long sequences also makes it a promising architecture for genomics tasks such as DNA sequencing and protein folding.
