



#  CNN+遷移學習(Vision Transformer)應用於影像辨識肺炎X光分類

- 本專案結合卷積神經網路（CNN）與 **Vision Transformer**（ViT-B-16)深度遷移學習架構，用於肺炎影像的二分類（YES/NO）辨識。與傳統 CNN 相比，ViT 具有**Global Attention**，能更有效捕捉影像中病灶可能出現的任意位置，因此特別適合腫瘤判讀這類高度變異、位置不固定的醫療影像任務。

 
### A. 數據 (Dataset & DataLoader)

#### 1. 資料來源
[https://www.kaggle.com/competitions/pneumonia-sai3/data]


#### 2. 資料規模

訓練集：4172 張。


驗證集:  1044張。

測試集:  624張。

---

### B. 模型 (Model)

#### 1. 使用深度遷移學習 (Deep Transfer Learning)
使用**ViT-B/16**影像分類模型架構，使用預設參數

*這裡使用 ViT 模型是因為病灶可能出現在圖像的任何位置，比 CNN 的局部感受野更具優勢，提升了特徵表徵的能力。

---

### C. 訓練與優化 (Training)

#### 1. 損失函數
`CrossEntropyLoss`

#### 2. 優化器
Adam（學習率：`1e-4`）

---

### D. Kaggle成績
1. Kaggle Public Score : 0.94739

`------ Advanced Baseline ----- 0.93631`

`------ baseline -------------- 0.90510`





