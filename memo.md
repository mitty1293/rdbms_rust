# 1章 RDBMSを作ろう
## Glossary
* ALTER TABLE  
作成済みのテーブル構造を変更することができるSQL文。  
カラムの追加と削除、制約の追加と削除、インデックスの追加と削除などテーブルに対して色々な変更を加えることが可能。
* セカンダリインデックス  
通常、主キーのノードに各データが紐づけられている。そのため主キーで検索すると目的のデータに迅速にアクセスできる。  
データとインデックスが別々に格納されているタイプのストレージエンジンでは、インデックスからデータの位置を読み取って、その後データファイルからデータをフェッチする。このように二段階の操作が必要である。  
後で書く。  
http://nippondanji.blogspot.com/2010/10/innodb.html
* JOIN  
複数のテーブルを連結させるSQL文。複数のテーブルから情報を取得する必要がある際に使用。
## 本文のメモ
* ミニRDBMSには、`構文解析機`、`クエリプランナ&実行計画`を実装しない。  
* つまり、ユーザ自身で構文を記述し実行計画を立てる必要がある。