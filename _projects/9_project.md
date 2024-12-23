---
layout: page
title: 圖片分類
description: 加入對抗式攻擊，觀察準確率差異
img: assets/img/圖片分類_1.jpg
importance: 1
category: 其他
related_publications: False
---

<div class="Conclusion">
    <h3>結論</h3>
    <div class="characteristics">
        <ul>
            <li>Training 及 Testing accuracy 成果好</li>
            <li>Adversarial Training的效果不佳</li>
        </ul>
    </div>
</div>

<div class="Motivation">
    <h3>研究動機</h3>
    <div class="characteristics" style="margin-left: 2em">
        在現今的AI快速發展的過程中，我們經常會在不同應用場景中使用神經網絡來協助進行決策，但神經網絡是否穩固成了一個需要被檢視的問題，這裡以CNN為例，左邊這張圖我們能看到一隻老虎，將這張圖片餵入 model 後所得到的 output 也是老虎，但如果這張圖被被加入了中間的擾動，成了右邊這張圖，我們單從肉眼觀察時這張圖片仍然是一張老虎，但若再次餵入模型時，則會得到錯誤的 output 結果。這個擾動造成模型判斷錯誤的結果我們就稱之為對抗式攻擊，由此我們與也能得知這個模型是不夠穩健的。
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/圖片分類_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="Structure">
    <h3>研究架構</h3>
    <ul>
        <li>將放置在各個不同的資料夾的影像進行讀取</li>
        <li>將讀取之影像依其所屬之資料夾給予編碼</li>
        <li>將圖片resize成相同大小（150×150）</li>
        <li>將所有已讀取之影像進行打亂（shuffle）的動作，避免有 overfitting 的情形發生，也能避免同一個組合的 batch 反覆出現，使的模型記住這些順序</li>
        <li>加入FGSM(Fast Gradient Sign Method)攻擊，預期觀察到準確率下降之結果</li>
        <li>加入Adversarial Training訓練，預期準確率回升</li>
    </ul>
</div>

<div class="Statistics">
    <h3>實驗成果</h3>
    <ul>
        <li>使用深度學習模型（CNN）進行初步訓練</li>
        <ul><li>使用普通訓練數據集進行訓練，並記錄 訓練準確率 (99.42%) 和 測試準確率 (83.1%)，以評估模型在未受干擾數據上的效能</li></ul>
        <li>FGSM</li>
        <ul><li>對模型生成對抗樣本，通過在輸入數據上添加小幅度干擾來生成對抗樣本，使模型錯誤分類，在對抗樣本上測試模型性能，發現測試準確率急劇下降到 1.98%，表明模型對對抗攻擊極為脆弱</li></ul>
        <li>Adversarial Training</li>
        <ul>
            <li>在訓練過程中，將對抗樣本與普通數據混合用於訓練</li>
            <li>訓練完成後，模型在對抗樣本上的準確率提升至 3.54%，在普通測試數據上的準確率為 4%。</li>
        </ul>
    </ul>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/圖片分類_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/圖片分類_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/圖片分類_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    </div>

<div class="Future">
    <h3>未來展望</h3>
    <div class="CurrentResearch">
        <ul>
            <li>本次研究</li>
            <ul>
                <li>Training 及 Testing accuracy 成果好</li>
                <ul><li>圖片幾乎出自影片中截圖，未來可測試非官方原圖的辨識結果</li></ul>
            </ul>
            <ul>
                <li>Training 及 Testing accuracy 成果好</li>
                <ul><li>不同AI模型也會因模型複雜度與訓練資料種類不同，需要不同的對抗式訓練及對抗式偵測模組（Adversarial Detection Module）的訓練時間</li></ul>
            </ul>
        </ul>
    </div>
    <div class="FutureDirections">
        <ul>
            <li>後續研究方向</li>
            <ul>
                <li>使用數據增強技術，像是翻轉圖像、切割圖像、噪音擾動(noise)等方法增加數據量，提高模型的擬合能力</li>
                <li>資料集變大後再增加訓練次數</li>
            </ul>
        </ul>
    </div>
</div>
