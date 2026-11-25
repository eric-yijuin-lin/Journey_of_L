#TeacherSelection

## 樹的形容詞
* full binary tree 
	* 除了樹葉以外，每個節點都有兩個子節點。
	* 中譯完「滿」(full)
* complete binary tree 
	* 各層節點全滿，除了最後一層，最後一層節點全部靠左。
	* 中譯完「整」(complete)
* perfect binary tree 
	* 各層節點全滿。同時也是 full binary tree 和 complete binary tree 。
	* 中譯完美，不解釋

## 走訪
### 前序/中序/後序
以**根節點**為參考點而定的走訪順序，決定走訪的順序：
- 前序：根結點 -> 左子樹 -> 右子樹
- 中序：左子樹 -> 根結點 -> 右子樹
- 後序：左子樹 -> 右子樹 -> 根結點
### 以走訪順序回推結構
通常一個中序搭配一個前序或後序
1. 前/後序：判斷根節點
2. 中序：判斷左右子樹
3. 遞迴套用 1. 2. 到左右子樹

可參考：https://ithelp.ithome.com.tw/articles/10205571

### 廣度/深度


## 各種二元樹
### [[AVL Tree]]
### [[霍夫曼樹（編碼）]]
### [[運算樹]]

### [[Heap]]

