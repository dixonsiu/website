---
id: version-1.7.21-personium_tests
title: Personiumのテスト
sidebar_label: Personiumのテスト
---

## 概要

Personiumの自動テストは大別してユニットテストとインテグレーションテストに分かれます。

|種別|概要|
|:--|:--|
|Unit Test|各クラス・メソッドの動作を確認します|
|Integration Test|HTTP APIの動作を確認します|


## Unit Test

各クラス・メソッドの動作を確認します。
モックなどを使ってなるべくコンパクトな処理に留めます。
ElasticSearchやActiveMQなどの外部プログラムとの通信は行いません。


### パッケージ/クラス/メソッドの命名規約

|対象|命名規約|備考|
|:--|:--|:--|
|パッケージ|対象クラスと同じ|io.personium.core.*となる|
|クラス名|{テスト対象クラス名}Test.java| |
|メソッド名|{テスト対象メソッド名}_{条件}_{結果}| |

すべて英語を使うものとします。

## Integration Test

io.personium.testパッケージ以下にあるテストです。

ElasticSearchやActiveMQなどの外部プログラムとの通信も行いながら
各APIの動作を確認します。

### 準備

Setup#reset()を実行してテスト用のデータをつくってから実行します。


