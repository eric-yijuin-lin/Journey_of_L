#TeacherSelection 
## Max Heap
### 特性/規範
* 是一個 complete tree
* 每個父節點，都要大於等於兩個子節點
	* 因此根結點的值一定最大
* 同級的左右，則沒有規範大小順序

### insert
1. 每次 insert 都要滿足 complete tree
2. 如果新的節點比父節點大，則需要進行 Heap Up (把新的點跟父節點互換)

### 走訪
- Heap 可以透過層序走訪（Level-order Traversal）還原成陣列。
- 層序走訪即廣度優先（BFS），由上到下，由左到右

### 應用
由於 Max Heap 有根結點一定是最大值的特性，因此適合用來實作與優先順序有關的程序，例如 priority queue, priority scheduling

### Min Heap
將父節點一定大於等於子節點的規則反向（小於等於）就會變成 Min Heap

### 例題
依序將 15, 40, 8, 25, 50, 30, 12 插入空的最大堆積(Max Heap),建構完成後,
數值 25 位於哪個索引位置(陣列表示,index 從 0 開始)?

建立步驟：
```
 Step 1: Insert 15      Step 2: Insert 40      Heap Up

        15                     15                 40
                              /          →       /
                             40                 15

 Step 3: Insert 8       Step 4: Insert 25      Heap Up

        40                     40                 40
       /  \                   /  \               /  \
      15   8                 15   8      →      25   8
                            /                  /
                           25                 15

 Step 5: Insert 50     Heap Up (1)     Heap Up (2)     Step 6: Insert 30

        40                  40              50                50
       /  \                /  \            /  \              /  \
      25   8       →      50   8     →    40   8            40   8
     /  \                /  \            /  \              /  \  /
    15  50              15  25          15  25            15  25 30
    
 Step 6: Heap Up        Step 7: Insert 12

        50                      50
       /  \                    /  \
      40   30                 40   30
     / \   /                 / \   / \
    15 25 8                 15 25 8  12
```

接著用 BFS 走訪還原陣列，得到：\[50, 40, 30, 15, 25, 8, 12\]
Ans: index = 4