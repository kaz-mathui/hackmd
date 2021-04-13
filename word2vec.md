# word2vec

ptpythonの後
- クリップボードにコピーするため
```
import pyperclip
```
- gensim　からword2vecをインポート
```
from gensim.models import word2vec
```
- modelを宣言
```
 model = word2vec.Word2Vec.load("jawiki-latest-pages-articles.model")
```
- 上位1000件近い順に表示（コピー）
- 足し引き算もできる
```
pyperclip.copy(str(model.wv.most_similar(positive=["使い方"],topn=1000)))
```
