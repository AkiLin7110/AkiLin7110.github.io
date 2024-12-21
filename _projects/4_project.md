---
layout: page
title: ATR
description: 虛擬貨幣價差策略
img: assets/img/漲停打開_5.jpg
importance: 1
category: 虛擬貨幣
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
        本研究通過實證發現，三種策略的績效（以Sharpe比率衡量）皆顯著優於Buy and Hold策略。
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <ul>
        <li>鎖漲停標的若盤中突然打開，可能存在一些交易機會，期望能夠在漲停打開的瞬間去做空標的，以此賺取獲利</li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/漲停打開_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>   
    </ul>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>觀察漲停打開與敲開金額的關聯性</li>
        <li>獲利性及風險評估分析</li>
        <li>定義：</li>
        <ul>
            <li>鎖漲停：委買第一檔出現市價單( Bid1=0, BidQty1>0)</li>
            <li>漲停打開：鎖漲停後，成交價＜漲停價</li>
            <li>累計的金額及張數：以漲停打開的時間點往前10秒計算</li>
        </ul>
    </ul>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>獲利性:打開後之漲跌幅</li>
        <ul><li>若敲開金額越大，其平均跌幅便有可能越深</li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/漲停打開_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <ul>
        <li>風險評估:暫緩撮合後之漲跌幅</li>
        <ul><li>暫緩搓合觸發機制：超過五分鐘內的平均價格正負3.5%。</li></ul>
        <ul><li>若敲開金額越大，其暫緩撮合後的平均跌幅便有可能越深。</li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/漲停打開_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/漲停打開_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <ul>
        <li>風險評估:打開後收盤漲停機率</li>
        <ul><li>若敲開金額越大，其收盤漲停機率越低。</li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/漲停打開_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>確認漲停打開的收盤價位及收漲停，二者皆與敲開金額相關</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>發展成交易策略</li>
                <li>追查敲開金額來源分點，以追蹤特定倒貨行為</li>
            </ul>
        </ul>
    </div>
</div>
    