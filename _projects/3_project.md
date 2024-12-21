---
layout: page
title: 最大概似估計法估計配對交易訊號與分位數訊號之績效表現比較
description: 美股價差策略
img: assets/img/配對交易_美股_1.jpg
importance: 3
category: 股票
related_publications: True
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        本研究通過實證發現，三種策略的績效（以Sharpe比率衡量）皆顯著優於Buy and Hold策略。
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <div class="characteristics" style="margin-left: 2em">
        實作論文{% cite chen2017pair %}，配對交易（Pair Trading）是一種採用統計套利以追求絕對報酬的交易策略。本研究選擇34檔股票，利用最小平方距離（Minimum Square Distance, MSD）挑選出10組相關性較高的股票配對，結合異質平滑函數及最大概似估計法建立模型，
        生成進出場訊號。目的是評估這些模型及策略的績效表現。
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul><li>模型分為三類：</li>
        <ul><li>模型一：使用ST-GARCH模型透過最大概似估計法生成上下界作為交易訊號。</li></ul>
        <ul><li>模型二與模型三：根據樣本分布的分位數（80%/20%及90%/10% VaR）計算上下界。</li></ul>
        <li>實驗數據：</li>
        <ul><li>選取2006年至2013年的歷史股價數據進行模型訓練，並使用2014年的數據進行回測。</li></ul>
    <li>策略評估：</li>
        <ul><li>三種策略的表現與Buy and Hold策略進行比較。</li></ul>
    </ul>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>Wald Test</li>
        <ul><li>三種策略之Sharpe ratio在95%信心水準下皆顯著大於Buy and hold策略 之Sharpe ratio，故使用這三種策略投資額外承受的每一單位風險所獲得的額外收益是 優於Buy and hold策略。
        </li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_美股_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <h3>交易策略</h3>
    <ul>
        <li>策略一：</li>
        <ul><li>
            根據ST-GARCH模型估計上下界。
        </li></ul>
        <li>策略二與三：</li>
        <ul><li>
            透過分位數VaR設定上下界，降低進出場頻率。
        </li></ul>
        <li>設定</li>
        <ul>
            <li>當兩檔股票的報酬價差高於上界，則放空A股票並買入B股票；</li>
            <li>當報酬價差低於下界，則買入A股票並放空B股票；</li>
            <li>當報酬價差位於上下界之間，不進行交易</li>
        </ul>
    </ul>
        <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_美股_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <h3>未來展望</h3>
    <div>
        <ul>
            <ul><li>從圖二中可以發現：策略一至三，在2014年之初期皆有較大虧損及週期性出現虧損之現象，因此能夠進一步用滾動的方式，計算該策略對於使用不同時間點之上下 界之敏感度，作為後續改善方向。</li></ul>
            <ul><li>在此研究中，所提及之Portfolio為每一天進行 Equally Weighted，但實際上因每一時間點之倉位數量不同，將使資金無法達到最有效之運用。</li></ul>
        </ul>
    </div>

