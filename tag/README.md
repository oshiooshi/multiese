各ファイルについてメモ

## タグ付け前
### hagemashi_corpus_Multiese.txt  
ー励まし文  
ー入力文  
形式の励ましコーパス。

### error_advice.txt
エラーコーパス。未完成。

## タグ付け後
### hagemashi_tag.tsv  
hagemashi_corpus_Multiese.txtにencourageタグをつけたコーパス。  
ーencourage: 入力文 \t 励まし文  

`python3 multiese.py --without-reorder --task encourage tag/hagemashi_corpus_Multiese.txt > tag/hagemashi_tag.tsv` にて作成。

### python_tag.tsv
`pandas.txt`に`python`タグをつけたコーパス。  
ーpython: 入力文 \t コード文  

`python3 multiese.py --task python rule_DS/pandas.txt > tag/python_tag.tsv`にて作成。

### ph_tag.tsv
`hagemashi_tag.tsv`と`python_tag.tsv`を結合したコーパス。  
ーencourage: 入力文 \t 励まし文  
ーpython: 入力文 \t コード文  


### hagemashi_tag_oi.tsv  
hagemashi_tag.tsvのoutputとinputを逆にしたコーパス。  
ーencourage: 励まし分 \t 入力文  
  
### ph_tag_oi.tsv  
ph_tag.tsvのoutputとinputを逆にしたコーパス。  
ーencourage: 励まし分 \t 入力文  
ーpython: コード文 \t 入力文   
