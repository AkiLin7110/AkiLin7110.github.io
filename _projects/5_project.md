---
layout: page
title: 擁擠交易：臺灣股市類股輪動策略
description: 偵測市場動向以創造獲利
img: assets/img/Thesis_8.jpg
importance: 1
category: Thesis
---

<div class = "Abstract">
    <h3>摘要</h3>
    <div class="characteristics" style="margin-left: 2em">
    本研究旨在探討擁擠交易現象與資產價格泡沫化的關聯，並提供一種發現泡沫擴
    張及泡沫破裂階段的方法，使投資人能夠在價格上漲過程中獲利、在價格下降前出售。
    研究中採用了兩種方法來判斷資產價格的階段：資產中心度和相對價值。前者判斷資
    金是否流入或流出該資產，即資金在少數資產上流動的程度。當資產中心度高時，表
    示大量資金流入或流出該資產，推升其價格上漲或驟降之可能性。後者判斷價格是否
    已偏離其實際價值，當相對價值高於某一標準時，表示價格可能已偏離其實際價值，
    存在泡沫破裂風險。
    此外，本研究將這些方法結合 Black-Litterman 模型，利用此模型結合資產中心度
    和相對價值，進行動態的資產配置，從而達到優於其餘資產配置模型的效果。
    </div>
</div>

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
        本研究透過資產中心度與相對價值的方法，將產業所處的市場階段分為四類：無泡沫期間 A、無泡沫期間 B、泡沫擴張期與泡沫破裂期。結果顯示：處於泡沫擴張期的產業，其資產報酬顯著優於市場大盤，驗證了方法的有效性。
    </div>
</div>
<div class="Structure">
    <h3>研究架構</h3>
        <ul>
        <li>資產中心度的計算：運用主成分分析 (PCA) 評估產業之間的互動性及其對市場的影響。</li>
        <li>資產相對價值的評估：結合歷史股價淨值比，判斷資產價格是否偏離基本價值。</li>
        <li>利用上述方法將產業狀態分類為四種類型（無泡沫期間 A、無泡沫期間 B、泡沫擴張期與泡沫破裂期）。</li>
        </ul>
</div>
<div class="Statistics">
    <h3>統計結果</h3>
    <ul><li>臺股市場自 2012 年至 2019 年之吸收比率與臺灣加權股價指數，可以發現其在這期間二者呈現負相關。</li></ul>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Thesis_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <ul>
    <li>以2019年底，疫情爆發時之數位雲端業與運動休閒業為例</li>
    <ul><li>資產中心度急劇上升</li>
        <li>反映資金之大量流動</li></ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/Thesis_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/Thesis_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <ul><li>資產中心度</li>
        <ul><li>資產中心度之相對提高，以提取資金快速流入或流出之訊息</li>
        <li>對其作標準化，並按照由大到小排名</li></ul>
    </ul>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Thesis_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <ul><li>資產相對價值，採用股價淨值比，判斷價格是否過度反應</li>
        <ul>
            <li>為判斷資金之流入之原因為:</li>
            <ul><li>泡沫擴張階段</li>
                <li>基本面價值上升</li>
            </ul>
        </ul>
        <ul><li>為判斷資金之流出之原因為:</li>
            <ul><li>泡沫破裂階段</li>
                <li>基本面價值下降</li>
            </ul>
        </ul>
        <ul><li>為捕捉相對於其他產業及往日表現，將經過標準化後之產業股價淨值比，稱為資產相對價值，按照由大到小進行排名</li>
        </ul>
        </ul>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Thesis_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <ul>
    <li>各條件結果</li>
    <ul><li>各產業依照其資產中心度與相對估值之排名分類</li>
        <li>2012年至2019年各種產業階段的報酬率，可以看到泡沫擴張期的Sharpe Ratio 是最高的</li>
    </ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/Thesis_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/Thesis_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <ul>
        <li>統計檢定</li>
        <ul>
            <li>期望在泡沫擴張期間之報酬，能夠贏過市場大盤。</li>
            <ul>
                <li>𝐻_0：泡沫擴張期間之報酬無異於或小於市場大盤之報酬</li>
                <li>𝐻_1：泡沫擴張期間之報酬大於市場大盤之報酬</li>
            </ul>
            <li>對其進行Levene變異數檢定與獨立樣本 T 檢定，P-value 為0.02，拒絕虛無假設：泡沫擴張期間的報酬無異於或小於市場大盤的報酬</li>
        </ul>    
    </ul>
    <h3>交易策略</h3>
    <ul>
        <li>回測設定：</li>
        <ul>
            <li>訓練期間：2012年至2019年</li>
            <li>測試期間：2020年至2024年4月</li>
        </ul>
        <li>調整投資組合頻率：</li>
            <ul>
                <li>月，採用每個月第一交易日之權重，作為每月之調整權重</li>
            </ul>
        <li>費用：0.3%(稅)+0.1425%(手續費)</li>
        <li>濾網：</li>
            <ul>
                <li>只買賣各個產業市值前10%之股票</li>
            </ul>
    </ul>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Thesis_8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Thesis_9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
