---
title: COSY,HMQC,HSQC,HMBC,NOESY,ROESY,TOCSY
nav_order: 50
parent: スペクトル関連
---

# 2次元NMR (COSY,HMQC,HSQC,HMBC,NOESY,ROESY,TOCSY) 測定方法

> 最終更新 : 2026-06-30
> 最終編集者 : 原


**パルスシーケンスの中身は公にはいじってはいけないことになっている。** <br> <br>
まずプロトンを測定し、SIMが合っているかを確認する。<br>
パルスシーケンス -> 2d -> 測定したいNMRを選んでダブルクリック<br>
### Header
auto gain にチェック (recvr gain に値を入れるならチェックしない）、force tune にチェック（最初だけ） <br>
### Instrument
auto gain にチェックを入れないなら、 Gain Value Established の値を入れる。こっちの方が早い。　<br>
### Acquisition (ex.0~7ppmを測定したい時)
x_offset 測定したい範囲の中央値 (3.5) <br>
x_sweep 測定したい範囲の値 (7) <br>
offset, sweepをセットした後に nus を入れる。
**(NOESY,ROESY,TOCSYは nus を入れてはいけない。)**
パラメーター追加 -> y_nuslist -> パラメータ追加 -> 完了 -> 追加された y_nuslist をクリック -> (warning みたいなのが出てきたら、閉じるを押す) 
-> schedule -> 完了<br>
scan で測定時間をいじる。何の倍数にすればいいかは scans にカーソルを持っていけばわかる。　<br>
測定開始　<br>　<br>
## ポイント : 同時に複数の2次元NMR をとる場合<br>
x軸プロトン/y軸カーボン(HMBCやHMQCなど)は続けて測定するとよい（force tune を最初だけに入れれば良いため、時間が削減できる）。<br>
ex) COSY, HMQC, HMBC を1終夜で測定したい時<br>
1H -> HMQC -> HMBC -> COSY の順で測定すると良い。（force tuneは HMQC だけに入れる）
