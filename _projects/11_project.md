---
layout: page
title: 廣義基金比例框架下的投資組合決策應用
description: 驗證了Leibowitz提出的投資組合方法
img: assets/img/處置股_5.jpg
importance: 1
category: ETF
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        研究驗證了Martin L. Leibowitz提出的投資組合構建方法，在表現上顯著優於傳統的最大夏普比率組合。研究中觀察了多種變數對該方法的影響，並嘗試在投資組合中加入現金部位以減少經濟衰退期間的損失。
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <div class="characteristics" style="margin-left: 2em">
    本研究旨在測試並延伸Martin L. Leibowitz提出的「廣義基金比例框架下的投資組合決策方法」。Leibowitz在現代投資組合理論中加入了成功機率與目標報酬率的概念，但其研究中缺乏對投資組合實際結果的驗證，因此本研究重點在於實驗結果與延伸應用。
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>根據Leibowitz提出的公式構建成功組合（Success Portfolio）與保障組合（Assurance Portfolio）。</li>
        <li>使用Sector ETF作為資產池（包含XLE、XLF、XLK等），數據來源為Yahoo Finance，期間涵蓋1991年至2022年，並每月進行資產重新配置</li>
        <li>通過夏普比率（Sharpe Ratio）評估表現，考慮不同的目標報酬率、成功機率及滾動窗口天數對投資組合的影響。</li>
    </ul>
</div>

<div class="Statistics">
    <h3>統計結果</h3>
    <ul>
        <li>初始分析： </li>
        <ul><li>在初期設置中，成功組合與保障組合的表現（累積報酬率及夏普比率）均低於最大夏普比率組合。</li></ul>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/GFRF_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/GFRF_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>  
        <li>滾動窗口天數： </li>
        <ul><li>引入滾動天數改變歷史數據，並觀察目標報酬率及成功機率對夏普比率的影響。</li></ul>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/GFRF_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/GFRF_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <li>穩健性分析：</li>
        <ul><li>配對T檢驗顯示，成功組合及保障組合的夏普比率顯著高於最大夏普比率組合。</li></ul>
        <div class="row">
            <div class="col-sm mt-3 mt-md-0">
                {% include figure.liquid loading="eager" path="assets/img/GFRF_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
            </div>
            <div class="col-sm mt-3 mt-md-0">
                {% include figure.liquid loading="eager" path="assets/img/GFRF_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
            </div>
        </div>
        <li>現金部位：</li>
        <ul><li>為減少經濟衰退（如2008年金融危機）帶來的損失，加入現金部位後，投資組合的表現明顯提升。</li></ul>
            <div class="col-sm mt-3 mt-md-0">
                {% include figure.liquid loading="eager" path="assets/img/GFRF_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
            </div>
        </ul>
</div>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>當設定的成功機率較低時，夏普比率反而較高，這可能說明用過去的報酬率來預測未來的投資組合並不具前瞻性。</li>
                <li>加入現金部位後，投資組合的表現優於未加入現金部位的情況，這一改進值得進一步研究。</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>將研究擴展至其他資產類別及經濟場景，驗證其應用價值</li>
            </ul>
        </ul>
    </div>
</div>
