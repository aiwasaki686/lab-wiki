---
title: Conflex配座探索
nav_order: 20
parent: 計算化学関連
---

# Conflex 配座探索

> 最終更新：2026-07-02  
> 最終編集者：藤木

---
### 手順
1. Chem Drawで立体も含めた構造を書き、Chem Drawファイルで保存。
2. ワークステーションに自分のフォルダ、計算する化合物のフォルダを作成し、以降そのフォルダ内に保存していく。
3. SpartanでChem Drawファイルを開き、立体が正しく反映されているか確認。違っていたら立体表記のまま変える。変更する際に平面にしないことに注意。sdfファイルで保存。
4. Conflexでsdfファイルを開く。ここで立体が合っているか再度確認。
5. molファイルが出てくるため、それを開く。
6. 画面左上のCalculationからConflexを選び、Geometry Optimizationでsubmit。計算が終わっているか、まだ計算しているかは画面下のfinished or runningで判断する。
   ![Calculation→Conflex](/images/Conflex1.png)
   ![Geometry Optimization](/images/Conflex2.png)
7. 6の計算が終わるとフォルダ内にF.molファイルが出現しているのでそれを開く。
8. 画面左上のCalculationからConflexを選び、Detail Settings。左上のボックスのうち、Calculation TypeをConformation Searchに、右下のボックスのSeach Limitを5 kcal/molに、それより下のParallel Search per Nodeを#16に変更し、submit。
 ![Conformation Search](/images/Conflex3.png)
 ![Search Limit](/images/Conflex4.png)
 ![Parallel Search per Node](/images/Conflex5.png)
9. 計算が終わるとF.sdfファイルが出現しているはず。そのファイルを使ってSpartanで計算を進める。

Spartan→Conflex、Conflex→Spartanなどの際には必ず立体が正しいか確認する。
<br>計算が上手くいかない場合や新しいファイルが出現しない場合、計算しているファイル名が原因の可能性がある。スペースや-はダメ、_はOK。
