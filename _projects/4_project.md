---
layout: page
title: 共整合配對交易
description: 加密貨幣價差策略
img: assets/img/配對交易_加密貨幣_1.jpg
importance: 1
category: 加密貨幣
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics">
        <ul>
            <li>基於ADF共整合策略，結合速度濾網與ATR波動濾網進行分析</li>
            <li>加入濾網後，能有效提升策略樣本外的績效，如勝率與報酬率</li>
            <li>ATR波動濾網的選擇符合單調性，高百分位數濾網效果更佳</li>
        </ul>
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <ul>
        <li>期望在加密貨幣市場中，透過統計套利來獲取穩定報酬率。</li>
    </ul>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>使用回歸分析交易對的報酬率，並利用殘差值設定進場與出場點</li>
        <li>策略包括:</li>
        <ul>
            <li>純共整合策略</li>
            <li>加速度濾網的共整合策略</li>
            <li>結合ATR波動濾網與加速度濾網的共整合策略</li>
        </ul>
        <li>設定不同停利、停損與手續費進行回測</li>
    </ul>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>ATR濾網的加入能顯著提升策略效能，尤其是選用高百分位數濾網時</li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="row">
            <div class="col-sm mt-3 mt-md-0">
                {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
            </div>
            <div class="col-sm mt-3 mt-md-0">
                {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
            </div>
        </div>
    </ul>
    <div class="row">
</div> 

<div class="Strategy">
    <h3>交易策略</h3>
    <ul>
        <li>進場條件：</li>
        <ul>
            <li>大於 3 倍標準差或小於 -3 倍標準差</li>
        </ul>
        <li>出場條件：</li>
        <ul>
            <li>大於 1.5 倍標準差或 -1.5 倍標準差</li>
            <li>超最多交易期：12*24 = 288 (五分鐘)</li>
            <li>停利 大於 2%</li>
            <li>停損 小於 -1.5% (會額外多扣1BP當作滑價成本)</li>
        </ul>
        <li>手續費：</li>
        <ul>
            <li>單邊0.05%，來回0.1%。</li>
        </ul>
        <li>回測方法：</li>
        <ul>
            <li>7天訓練期，4天Rolling動態算上下界，每次交易最多持有一天。</li>
            <li>每一天Rolling重新估計新的對沖係數和殘差上下界。</li>
        </ul>
        <li>策略包括:</li>
        <ul>
            <li>純共整合策略</li>
            <li>加速度濾網的共整合策略</li>
            <li>結合ATR波動濾網與加速度濾網的共整合策略</li>
        </ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/配對交易_加密貨幣_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
        