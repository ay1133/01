# 1:初始化鏈表
定義節點結構:指針域pre、next和數據域data

為方便操作添加了head和tail節點,初始化時head.next->tail,tail.pre->next

# 2:獲取鏈表長度
起始head，每有一個節點，length＋1

# 3:追加節點
因為有tail 節點，所以找到tail.pre 節點就好了

# 4:獲取節點
獲取節點要判斷index正負值

# 5:設定節點
找到當前節點賦值即可

# 6:插入節點
插入節點需要找到插入節點的前一個節點pre_node和後一個節點next_node（索引index的正負，前一節點不同，需要判斷一下），

然後將pre_node.next–>node,node.pre->pre_node;next_node.pre–>node,node.next–>next_node

# 7:刪除節點
刪除節點，也要區分一下索引的正負。找到當前節點的前一個節點pre_node和後一個節點next_node，將pre_node.nex–>next_node即可

# 8:反轉鏈表
反轉鏈表的實現有多種方式，比較簡單的就是生成一個新的鏈表－－》可以用數組存儲所有節點讓後倒序生成新的鏈表

在這里用下面這種方式生產：

可能有點繞

1.node.next –> node.pre；node.pre –> node.next（遞歸）

2.head.next –> None；tail.pre –> None

3.head–>tail；tail–>head

# 9:清空鏈表
類似初始化
