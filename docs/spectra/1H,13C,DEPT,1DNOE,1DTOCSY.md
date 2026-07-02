---
title: 1H,13C,DEPT,1DNOE,1DTOCSY
nav_order: 40
parent: スペクトル関連
---

# 1次元NMR 測定方法

> 最終更新 : 2026-06-30
> 最終編集者 : 原

 ## プロトンNMR（¹H NMR）の測定方法

Job 左下の「Proton」をクリック。
右側に表示される設定画面で、以下の項目を設定する。

autogainにチェック<br>
Scans に希望する積算回数を入力。<br>
Relaxation Delayを4秒 → 2秒に変更<br>
「測定登録」をクリック。


## カーボンNMR（13C NMR）の測定方法

Job 左下の「carbon」をクリック。
右側に表示される設定画面で、以下の項目を設定する。

autogainにチェック<br>
Scans に希望する積算回数を入力。<br>
「測定登録」をクリック。


## DEPTの測定方法

**Job 左下のDEPTは押さない。カーボンも測定されてしまうため。**　<br>
パルスシーケンス -> 1d -> DEPT

### Header
auto gain にチェック (recvr gain に値を入れるならチェックしない）、force tune にチェック（最初だけ） <br>
### Instrument
auto gain にチェックを入れないなら、 Gain Value Established の値を入れる。こっちの方が早い。　<br>
### Acquisition (ex.0~7ppmを測定したい時)
基本的にscanをいじるだけ。　<br>
測定開始　<br>


## 1DNOE,1DTOCSYの測定方法
まずプロトンを測定し、SIMが合っているかを確認する。<br>
パルスシーケンス -> All files > noe(tocsy)_1d_dpfgse 

### Header
auto gain にチェック 、force tune にチェック（最初だけ） <br>
### Instrument
**spin_state -> spin off**　<br>
### Acquisition (ex.0~7ppmを測定したい時)
X_off_setに照射したい ppm を入力。（x.xxx...まで全て）<br>
x_points -> 32768 (16384*2)<br>
積算は多めに。16 の倍数。<br>
測定開始　<br>

・シグナルの出が悪い時は mixing time を変更する。

### DPFGSEの利点と欠点
・利点<br>
・subtraction のプロセスがないので、消え残りを心配しなくていよい。<br>
・一度のスキャンが短い。<br>
・測定が手軽<br>
・以上の理由より、S/N の良いデータが取れるので、より長距離な NOE の観測に向く。<br><br>

・欠点(1D NOEが優れている点)<br>
・定量性に乏しく、XX％のように数値化するのに適さない。<br>
・選択励起が苦手





