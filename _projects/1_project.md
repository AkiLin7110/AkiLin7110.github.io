---
layout: page
title: 處置股
description: 
img: assets/img/12.jpg
importance: 1
category: 股票
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        <h4>處置股特性</h4>
        <ul>
            <li>聽牌的股票有近 90% 的機率會進入處置。</li>
            <li>其中，因第一款條件進入處置的股票數量佔多數，約 80%。</li>
        </ul>
    </div>

    <div class="statistics" style="margin-left: 2em">
        <h4>統計結果</h4>
        <ul>
            <li>若在上漲的情況下確定進入處置，該股票在處置當天有很高機率上漲，甚至可能衝到漲停。</li>
            <li>相反地，若在上漲的情況下不確定是否進入處置，該股票在處置當天則不一定會上漲。</li>
        </ul>
    </div>

    <div class="strategies" style="margin-left: 2em">
        <h4>交易策略</h4>
        <ul>
            <li>若採用中價進行回測，其特性為：大賺小賠，且績效表現不錯。</li>
            <li>但若考量流動性問題，其特性為：大賺大賠，績效表現較差。</li>
        </ul>
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <ul>
        <li>股票進入處置等同於不能進行交易，因此希望了解聽牌後真正進入處置的機率。</li>
        <li>市場現象：
            <ul>
                <li>觀察到部分股票在聽牌日當天漲幅很大，但最終反轉，未進入處置，而收盤價接近進入處置的價位。</li>
            </ul>
        </li>
        <li>推測原因：處置後流動性下降，可能導致投資人提早出場的需求，進而啟發收斂策略的可能性。</li>
    </ul>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>透過證交所與櫃買中心所公告的注意資訊，計算股票的累積注意次數，當其符合一定條件時，認定為聽牌或處置，進而計算聽牌是否能預測處置，以及處置後是否能穩定市場。</li>
        <li>利用注意資訊計算各股票的處置價，並觀察公告處置當日是否有高機率回到處置價。</li>
        <li>基於此發展收斂交易策略。</li>
    </ul>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>限縮在第一款處置的情況下：</li>
        <ul><li>累計漲幅為正的樣本佔了近 9 成。</li></ul>
        <ul><li>公告處置當天，高機率收盤收在聽牌當天所計算出的處置價位。</li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
        <ul>
            <li>在聽牌累計前 5 日漲跌幅＞０ 且不確定會不會進處置的情況下，公告處置當天有約 7 成的聽牌標的不會收在漲停的位子，推測可能存在交易機會。
            </li>
        </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    </div>

<div class="Strategy">
    <h3>交易策略</h3>
    <ul>
        <li>濾網
            <ul>
                <li>考量流動性風險，排除處置中的股票。</li>
                <li>因肯定被處置的股票有高機率收漲停，排除肯定被處置的股票。</li>
            </ul>
        </li>
        <li>設定
            <ul>
                <li>若價格曾高於 8%，接著回落到 8～7% 之間時執行做空，且其 7% 的價格需大於處置價位才進場。</li>
                <li>停損：價格漲回 9.5%。</li>
                <li>部位限制：最多 100 萬。</li>
                <li>成本：0.15%。</li>
            </ul>
        </li>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/處置股_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
</div>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>在聽牌條件一的情況下，採用收斂之交易策略進行回測。</li>
                <li>聽牌的股票有近 90% 的機率會進入處置。</li>
                <li>其中因第一款條件進入處置的股票數量佔多數，約 80%。</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>在航運股飆漲時，陽明、長榮容易收盤於關鍵價位。</li>
                <li>其因處置條件二進入處置，但需更深入探討注意的款項。</li>
                <li>探討處置股是否與特定大戶的進場行為相關：
                    <ul>
                        <li>需分析分點的進場情況。</li>
                    </ul>
                </li>
            </ul>
        </ul>
    </div>
</div>
