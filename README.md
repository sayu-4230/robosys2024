# kansuuenzanコマンド
ロボットシステム学授業用

## 概要
- 入力された角度に応じて三角関数の値を出力します。

## 必要なソフトウェア
- Python 
    テスト済みバージョン:3.7~3.10

## テスト環境
- Ubuntu20.04 LTS

## インストール方法
以下の手順でプロジェクトをローカル環境にインストールしてください。

リポジトリをクローン
```
$ git clone https://github.com/sayu-4230/robosys2024.git
```
ディレクトリに移動
```
$ cd robosys2024
```
kansuuenzanスクリプトに権限を与えます
```
$ chmod +x kansuuenzan
```
## 使い方

実行する
```
$ echo <角度> | ./kansuuenzan
```

###　実行例
- 実行例１
```
$ echo 45 | ./kansuuenzan
```
- 実行結果
```
45.0度の三角関数:
sin(45.0°) = 0.7071067811865475
cos(45.0°) = 0.7071067811865476
tan(45.0°) = 0.9999999999999999
```
- 実行例２
```
$ echo 30 | ./kansuuenzan
```
- 実行結果
```
30.0度の三角関数:
sin(30.0°) = 0.49999999999999994
cos(30.0°) = 0.8660254037844387
tan(30.0°) = 0.5773502691896257
```
- 実行例３
```
$ echo 65 | ./kansuuenzan
```
- 実行結果
```
65.0度の三角関数:
sin(65.0°) = 0.9063077870366499
cos(65.0°) = 0.42261826174069944
tan(65.0°) = 2.1445069205095586
```

## サンプルプログラム
```
#!/usr/bin/python3
import math
import sys

degree = float(sys.stdin.readline().strip())


radian = math.radians(degree)

sine = math.sin(radian)
cosine = math.cos(radian)
tangent = math.tan(radian)
    
print(f"{degree}度の三角関数:")
print(f"sin({degree}°) = {sine}")
print(f"cos({degree}°) = {cosine}")
print(f"tan({degree}°) = {tangent}")
```

## ライセンス
- このソフトウェアパッケージは、第３条項BSDライセンスの下、再頒布および使用が許可されます。
- ©　2024　Yuki Nishijima
