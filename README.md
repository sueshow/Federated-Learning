# 聯盟式學習 (Federated Learning)

* 介紹：資料不需要離開設備端各自在自己的設備訓練模型，並且通過特定的加密的機制在雲上建立一個共有的模型與進行模型的更新，用以改善產品設備的品質，透過這樣子的聯盟式學習的概念所有的訓練數據都仍然保留在原本的設備上。
* 個資：在 2018 年 5 月歐盟通過 General Data Protection Regulation (GDPR) 法案，法案明確指出所有與個人相關的信息都是個人數據，對數據的使用行為必須要有用戶的明確授權與同意。
* 目的：希望做到各個企業的自有的數據不出自己的公司各自訓練模型，並且通過加密的機制建立一個共有的模型與進行模型的更新，這不僅保護了隱私，還降低大量數據集中傳輸的成本。
* 型態：
  * 橫向聯盟式學習 (horizontal federated learning)：
    * 特性：架構簡單
    * 適用：於特徵重疊性高且樣本重疊少時的情境，如不同地區的醫院，他們的業務相似 (特徵相似)，但病患不同 (樣本不同)
    * 方法：每個參與方會得到同樣的模型定義，並且統一模型的初始化參數
  * 縱向聯盟式學習 (vertical federated learning)
  * 聯盟式遷移學習 (federated transfer learning)
  
* 參考資料：
  * https://medium.com/sherry-ai/%E8%81%AF%E7%9B%9F%E5%BC%8F%E5%AD%B8%E7%BF%92-federated-learning-b4cc5af7a9c0