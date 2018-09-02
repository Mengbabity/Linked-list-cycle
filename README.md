# Linked-list-cycle
1.怎样判断链表循环
定义两个指针，slow和fast，slow走一步，fast走两步，相等即存在循环。

2.找到开始循环的点
公式推导：head到开始点的距离为L1，开始点到相遇点的距离为L2，循环长度为c,fast的循环圈数为n
         slow走的距离L1+L2，fast走的距离L1+L2+n*c
         则有：2*(L1+L2)=L1+L2+n*c，即L1=(N-1)*C+(C-L2)
         即entry走的步数=slow转圈圈，相等点为开始点。（画图就明白了）
