---
title: sawtooth
parent: NMR
nav_order: 80
---
# Sawtoothを用いたロックシグナルの探索

重溶媒中の**重水素シグナル**を見失うと、ロックをかけることができない。

---

### 1. Sawtoothを開く

**Spectrometer Control**ウィンドウ中央付近にある**「Sawth」**ボタンをクリック。
- 右上にある再生ボタンを押す。


### 2. パラメータを設定する

- **Receiver gain：31**
- **Lock level：255**
- **Range：8**

<span style="color:red;">※Lock levelとReceiver gainの初期値は、後で元に戻すため必ず控えておく。</span>


### 3. ロックシグナルを探す

表示されたシグナルを確認し、**立ち上がりの位置をクリックして画面中央へ移動**させる。
<img width="303" height="236" alt="image" src="https://github.com/user-attachments/assets/47e4dbf9-96f2-4d3a-984f-f24d256c9ad1" />


### 4. Rangeを小さくして位置を調整する

シグナルを中央に合わせたら、**Range**を徐々に小さくして調整。

例
8 → 6 → 4 → 2

**Range = 4**でシグナルが確認できれば、通常はロックをかけることができる。
- 再生ボタンを止める。
- 調整が終わったら、**Lock level**と**Receiver gain**を元の値に戻す。


### 5. 測定を開始する

Sawtoothウィンドウを閉じる。
ロック画面の一番左のを押して自分でロックをかける。

---
