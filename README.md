# 聯盟式學習 (Federated Learning)

* 介紹：
  * 資料不需要離開設備端各自在自己的設備訓練模型，並且通過特定的加密的機制在雲上建立一個共有的模型與進行模型的更新，用以改善產品設備的品質，透過這樣子的聯盟式學習的概念所有的訓練數據都仍然保留在原本的設備上
  * Federated Learning 是 Google 於 2017 年提出的模型訓練方式。基於保護用戶隱私的前提下，能進行機器學習模型訓練的雲架構，能共享訓練結果，以提供更好的用戶體驗
* 個資：在 2018 年 5 月歐盟通過 General Data Protection Regulation (GDPR) 法案，法案明確指出所有與個人相關的信息都是個人數據，對數據的使用行為必須要有用戶的明確授權與同意
* 目的：希望做到各個企業的自有的數據不出自己的公司各自訓練模型，並且通過加密的機制建立一個共有的模型與進行模型的更新，這不僅保護了隱私，還降低大量數據集中傳輸的成本
* 型態：
  * 橫向聯盟式學習 (horizontal federated learning)：
    * 特性：架構簡單，被運用的最為廣泛
    * 適用：於特徵重疊性高且樣本重疊少時的情境，如不同地區的醫院，他們的業務相似 (特徵相似)，但病患不同 (樣本不同)
    * 方法：每個參與方會得到同樣的模型定義，並且統一模型的初始化參數，不斷迭代步驟訓練模型
    * 應用：
      * Google 在 Android 的 Google Gboard 鍵盤：根據使用者打的單詞推薦下個可能打出來的單詞，來加快使用者的打字速度。導入在 Gboard 的聯盟式學習則會根據設備上的歷史記錄，在下一次迭代中改進模型的性能
    ![橫向聯盟式學習](https://github.com/sueshow/Python_Federated-Learning/blob/main/picture/%E6%A9%AB%E5%90%91%E5%BC%8F%E8%81%AF%E7%9B%9F%E5%AD%B8%E7%BF%92.png)

  * 縱向聯盟式學習 (vertical federated learning)
    * 特性：參與端越多流程架構就會越複雜，更難以執行
    * 適用：於樣本重疊多且特徵重疊少的情境，而其中某一方還擁有模型需要預測的標籤 (label)，共享相同樣本但特徵不同，如同一地區的醫院和藥局，他們接觸的病患都為該地區的居民 (樣本相同)，但業務不同 (特徵不同)
    * 方法：A 與 B 需要利用加密樣本對齊的技術 (Encrypted entity alignment) 確認雙方共有的客戶，之後再利用這些數據進行加密訓練
    ![縱向聯盟式學習](https://github.com/sueshow/Python_Federated-Learning/blob/main/picture/%E7%B8%B1%E5%90%91%E5%BC%8F%E8%81%AF%E7%9B%9F%E5%AD%B8%E7%BF%92.png)

  * 聯盟式遷移學習 (federated transfer learning)
    * 適用：於兩個數據集在樣本上而且在特徵空間上都不同的情況
    * 情境：當擁有數據者間的特徵和樣本重疊都很少時，則是可以使用聯盟式遷移學習，這種狀況就不會針對數據進行切割，而會引入遷移式學習 (transfer learning) 來克服資料與標籤不足的狀況
    * 差異：橫向聯盟式學習跟分散式機器學習最大的差別在於它的每個結點 (node) 都是獨立的參與端 (data owner)，因此在建模的過程中可能會因為參與端 (data owner) 的偏好而有動態的改變，並且整個學習過程都受到加密的保護
    ![比較](https://github.com/sueshow/Python_Federated-Learning/blob/main/picture/%E6%AF%94%E8%BC%83%E5%B7%AE%E7%95%B0.png)    
<br>

* 參考資料：
  * https://medium.com/sherry-ai/%E8%81%AF%E7%9B%9F%E5%BC%8F%E5%AD%B8%E7%BF%92-federated-learning-b4cc5af7a9c0
  * https://medium.com/%E5%AD%B8%E4%BB%A5%E5%BB%A3%E6%89%8D/%E8%81%AF%E7%9B%9F%E5%BC%8F%E5%AD%B8%E7%BF%92-federated-learning-9b195c8b4463
