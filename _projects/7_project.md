---
layout: page
title: 日頻率波動度計算方法研究
description: 交易員輔助工具
img: assets/img/真實波動度_1.jpg
importance: 1
category: 真實波動度
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        採用 rogers-satchell 及 Parkinson 這兩種計算方法，波動度的變動程度較小
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <div class="characteristics" style="margin-left: 2em">
        期望解決：原先波動度過度敏感的問題
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>實作開高低收波動度</li>
    </ul>
    <div class = "row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>相較於原始方法，其餘波動度的變化程度下降</li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
    <ul>
        <li>以同樣取樣期間、同檔標的波動度計算其變異數</li>
        <ul><li>發現Rogers-Satchell 及 Parkinson 相對穩定</li></ul>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/真實波動度_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
</div>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>找到相對穩定的波動度</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>驗證在追求穩定波動度的同時，是否不影響敏感性</li>
                <li>K值的訂定</li>
            </ul>
        </ul>
    </div>
</div>

