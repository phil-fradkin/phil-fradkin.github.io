---
layout: default
title: CONCERTO publication
---

## A Graph Neural Network Approach to Molecule Carcinogenicity Prediction

Watch video explainer of CONCERTO here:

<div class="large-image">
    <a href="https://www.youtube.com/watch?app=desktop&v=7krei9z02n4">
        <img src="../images/thumbnail.jpg?raw=tru" alt="Image Alt Text" class="large-image">
    </a>
</div>


<div class="link-container">
    <span class="link-symbol">🔗</span>
    <a href="https://academic.oup.com/bioinformatics/article/38/Supplement_1/i84/6617525">
        <h3>Link To Paper</h3>
        <p></p>
    </a>
</div>

<div class="link-container">
    <span class="link-symbol">🔗</span>
    <a href="https://github.com/bowang-lab/CONCERTO">
        <h3>Link To Code Base</h3>
        <p></p>
    </a>
</div>


### Motivation

Molecular carcinogenicity is a preventable cause of cancer, but systematically identifying carcinogenic compounds, which involves performing experiments on animal models, is expensive, time consuming and low throughput. As a result, carcinogenicity information is limited and building data-driven models with good prediction accuracy remains a major challenge.

### Results

In this work, we propose CONCERTO, a deep learning model that uses a graph transformer in conjunction with a molecular fingerprint representation for carcinogenicity prediction from molecular structure. Special efforts have been made to overcome the data size constraint, such as multi-round pre-training on related but lower quality mutagenicity data, and transfer learning from a large self-supervised model. Extensive experiments demonstrate that our model performs well and can generalize to external validation sets. CONCERTO could be useful for guiding future carcinogenicity experiments and provide insight into the molecular basis of carcinogenicity.
Availability and implementation
