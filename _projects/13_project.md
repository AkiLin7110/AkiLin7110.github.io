---
layout: page
title: LIBOR IRS 到 SOFR OIS 的風險分析
description: 協助交易員進行影響性分析，評估其對交易部位的潛在衝擊
img: assets/img/風險分析_1.jpg
importance: 1
category: 風險分析
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics">
        <ul><li>在DV01方面，LIBOR IRS的DV01變動幅度較SOFR OIS大，這可能是因為LIBOR IRS每3個月鎖定利率，而SOFR OIS則每日複利計息，每年付息。因此，由於LIBOR IRS的計息間隔較長，其利率變動對未來現金流的影響更大，從而導致其DV01的變動幅度較大。</li>
        <li>在Roll-Dow方面：LIBOR IRS的浮動端與固定端不對稱，導致已實現收益呈現鋸齒狀跳動；而SOFR OIS由於支付期間對稱，因此已實現損益較為穩定。</li>
        </ul>
    </div>
</div>

<div class="Motivation">
    <h3>背景與動機</h3>
    <div class="characteristics" style="margin-left: 2em">
    在2023年6月底的時候 ， LIBOR指標正式退場，LIBOR包含五種幣別（英鎊、美元、歐元、瑞士法朗、日圓）及七種期限（隔夜、七天、一個月、兩個月、三個月、六個月、十二個月），其中最常被使用的是「三個月美元LIBOR」。原來的美元  LIBOR，指的是倫敦銀行間進行拆放款的實際利率，包括債券、房貸、銀行聯貸或是各種衍生性金融商品的定價都與它，美元LIBOR有關，它是國際金融市場中浮動利率的基礎，但它的報價是由BBA英國銀行家協會所選定的具有代表性的銀行，當交易量不夠時，銀行往往被迫採用插值等方式處理，或基於主觀經驗而生出報價，故LIBOR無法準確反映市場資金的利率水準。那同時也因為利益衝突問題，多家銀行聯合操縱利率使其投資績效比較好，因此便提出了替代利率的建議，那在美元LIBOR方面，所採取的替代利率為SOFR，隔夜公債附買回利率，取決於美國國債回購的交易數據，因為他是基於真實交易而生的利率，能夠去真實反映金融市場的資金情況及克服LIBOR人為操縱的問題。
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/風險分析_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <div class="characteristics" style="margin-left: 2em">
    以部門經常承做的利率交換去進行從LIBOR IRS到SOFR OIS所面臨的風險樣態比較，那給定Market Curve可能為正斜率或負斜率這兩種狀況去進行分析，所採用的風險分析工具是 DV01 Bucket 及 Roll-Down 兩者，前者去分析不同期限報價對於承作商品價值的影響性，後者去分析在假設Ｍarket Cure不變的情況下，承作商品的市值變化。
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/風險分析_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="Statistics">
    <h3>研究結果</h3>
    <ul>
        <li>那針對前面所提到LIBOR IRS與SOFR OIS，其現金流與計息方式都不太一樣，那利率交換有浮動端及固定端兩隻腳，首先LIBOR IRS是每3個月去鎖定他下一期3個月過後需支付之利息，浮動端的支付頻率是每3個月一次，固定端則是每半年付息一次，所以他的兩隻腳是不對稱的。那SOFR OIS是每日去鎖定利率，採取每日複利，在每年付息時支付這一年期間的複利金額。那可以單從浮動端鎖定利率及計息方式，便能夠看出SOFR較不容易受到人為操縱，要操縱一天的3 Ｍo LIBOR遠比365天的SOFR來得容易。</li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
    <ul>
        <li>首先以承作日當下的DV01為例，那這裡同樣以3YR到期的利率交換為例，可以看到與商品到期日相同之期限報價，因其直接反應利率交換所帶來之現金流，所以其所帶來之影響幅度會最大。那因為SOFR OIS 採取每日複利計息，每年付息，所以會受到相關期限報價之影響比如1D及1 W及貼近付息日之11m及12Ｍ。LIBOR IRS 採取每3個月鎖定利率去計息，每3個月付息，因此在兩個鎖定期之間的利率變動不會直接影響到其現金流，因此報價對其影響相對較小。
        </li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
    <ul>
        <li>在LIBOR IRS方面，因為在每3個月利率鎖定後，IRS的未來現金流會按照新鎖定的利率計算，因此總DV01以3個月為跳動頻率逐漸減少，變動1bp所能夠帶給商品價值之影響漸漸減少。那一年之後，３年期之利率交換將剩下２年期，因此2YR的期限報價重要性提升; 那再過一年，2年期之利率交換，僅剩下１年，因此１YR的期限報價跟著提升。同時也可以發現受到已實現金額3Y所能夠帶來之影響最大
        </li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <li>在SOFR OIS方面，因為採取每日鎖定浮動利率，因此隨著時間變動，DV01於年間微幅下降；因每年付息一次，因此總DV01以年為跳動頻率下降。那同樣的因商品剩餘之到期日逐漸減少，1YR 過後 2YR期限報價達到所能夠帶來之影響達到頂峰，之後遞減 這樣的現象，那與LIBOR IRS較為不同的是，SOFR OIS在payment 期間其DV01有微幅波動，而並非只是線性。
        </li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
    <ul>
        <li>正斜率下的：Roll-Down MTM
        <ul><li>
        在假設隨著時間推移，Market Curve不變之假設下，採取Roll-Down之策略持有較長天期之IRS或OIS，皆能夠獲得正報酬。
        </li></ul>
        </li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <li>負斜率下的：Roll-Down MTM
        <ul>
            <li>在假設隨著時間推移，Market Curve不變之假設下，若採取Roll-Down之策略持有較長天期之IRS或OIS，將會承受損失。</li>
            <li>在Market Curve為負的情況下，不適合採取Roll-Down。</li>
        </ul>
        </li>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/風險分析_10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </ul>
</div>

<div class="Future">
    <h3>總結</h3>
    <div class="CurrentResearch">
        <ul>
            <li>從DV01中發現：</li>
            <ul>
                <li>商品到期日相同之市場報價對商品價值影響最大</li>
                <li>其他期限報價，仍會以較小規模影響商品價值</li>
            </ul>
            <li>從DV01 Bucket中發現：</li>
            <ul>
                <li>隨時間經過，每一次浮動利率指標定價完之 DV01</li>
                <li>動幅度LIBOR IRS的幅度會較SOFR OIS 的幅度還大</li>
            </ul>
            <li>從LIBOR IRS與SOFR OIS之Roll-Down：</li>
            <ul>
                <li>由其付息的方式可以發現：LIBOR IRS的浮動端與固定端是不對稱的，導致已實現現金流會呈現鋸齒狀跳動；SOFR OIS因支付期間對稱，因此已實現現金流穩定</li>
                <li>在Market Curve為負之情況下，不適合採用Roll-Down</li>
            </ul>
        </ul>
    </div>
</div>