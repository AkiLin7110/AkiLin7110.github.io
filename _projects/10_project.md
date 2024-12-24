---
layout: page
title: 產業ETF輪動策略
description: 利用10年期公債與BAA公司債之利差，發展資產配置策略
img: assets/img/sector_1.jpg
importance: 1
category: ETF
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        <h4>績效表現</h4>
        <ul>
            <li>回測期間自2007年至2024年，策略累積報酬率為693.55%，CAGR為12.23%</li>
            <li>同樣期間，SPY累積報酬率為285.82%，CAGR為7.81%</li>
        </ul>
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <ul>
        <li>以總經指標作為信號，將市場切為四個週期：Decline、Recovery、Early、Late，發展資產配置策略</li>
        <li>市場現象：
            <ul>
                <li>觀察在各循環週期Sector ETF中，持有歷史績效相對較佳之ETF</li>
            </ul>
        </li>
    </ul>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sector_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="Statistics">
    <h3>研究架構</h3>
    <ul>
        <li>於FRED上獲取：10年期公債與BAA等級公司債之利差與平均作為信號依據</li>
        <li>依照期利差之高於平均及低於平均、放大及縮小，發展資產配置策略</li>
    </ul>
</div>

<div class="Statistics">
    <h3>研究結果</h3>
    <ul>
        <li>優於大盤之績效表現</li>
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sector_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <li>歷年資產配置概況：（黃：Decline, 紫：Recovery, 紅：Early, 綠：Late）</li>
        <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sector_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
</div>



<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>雖獲得優於大盤之績效表現，但其於.com泡沫與疫情之DD仍相當巨大</li>
                <li>若能再加入現金或債券部位會更佳</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>加入停利及停損機制</li>
                <li>發展成日頻策略及Long Short 避免鉅額虧損</li>
            </ul>
        </ul>
    </div>
</div>
