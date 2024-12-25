---
layout: page
title: 雨天選擇權
description: 發行新衍生性商品
img: assets/img/rainy_days_1.jpg
importance: 1
category: 選擇權
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics" style="margin-left: 2em">
    雨量選擇權能在雨天數高於平均時補償農損，且在雨天數低於平均時提供投機者獲利機會
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <div class="characteristics" style="margin-left: 2em">
        台灣因地理位置的特殊性，常受颱風和梅雨季的影響，農業損害頻繁。為了幫助農民避險，開發雨量選擇權作為天氣衍生性商品，利用降雨量的波動特性進行避險或投機活動。
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>目標</li>
        <ul>
            <li>設計雨量選擇權並評價其價格</li>
            <li>幫助農民減少因雨量波動導致的損失</li>
        </ul>
        <li>方法</li>
        <ul>
            <li>使用歷史每日雨量數據（2009-2020年）</li>
            <li>假設每日降雨量服從Gamma分布，計算各地各月的α和β值</li>
            <li>模擬100,000次降雨量，並依此預測每月降雨量超過100mm的天數</li>
            <li>利用結果進行選擇權定價。</li>
        </ul>
        <li>定價公式</li>
        <ul>
            <li>price = mean of simulation × price multiplier × discount factor</li>
        </ul>
    </ul>
</div>

<div class="Statistics">
    <h3>研究結果</h3>
    <ul>
        <li>模擬結果與定價</li>
        <ul>
            <li>各地7至9月的α和β值差異明顯，顯示降雨量的地域性和季節性差異。</li>
            <li>定價結果顯示，8月和9月的商品價格較高，反映出颱風季的降雨量增加。</li>
        </ul>
        <li>模擬結果與定價</li>
            <ul>
                <li>以2020年8月屏東縣的木瓜農損為例，購買雨量選擇權後，農民能減少損失約899.95元，證明此商品具有減少農業損害的潛力。</li>
            </ul>
    </ul>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>研究採用「達標雨天數」為標的物，而非「降雨量」，降低了複雜性。</li>
                <li>該商品具有助農避險的實際應用價值。</li>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>擴展至其他氣候因子</li>
                <ul>
                    <li>除雨量外，可考慮設計基於其他氣候因素（如溫度、風速、日照時數等）的衍生性商品，提供更全面的農業避險方案。
                    </li>
                </ul>
            </ul>
        </ul>
    </div>
</div>

<div class = "More">
    <h3>更多資訊</h3>
    <a href="https://rainoption.weebly.com/final-project.html" target="_blank">查看完整研究專案</a>
    <h3>選擇權</h3>
    <a href="https://107071073hw.weebly.com/" target="_blank">MATLAB實作</a>
</div>
