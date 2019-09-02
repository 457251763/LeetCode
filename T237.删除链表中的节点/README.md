请编写一个函数，使其可以删除某个链表中给定的（非末尾）节点，你将只被给定要求被删除的节点。

现有一个链表 -- head = [4,5,1,9]，它可以表示为:<br>
![](https://assets.leetcode-cn.com/aliyun-lc-upload/uploads/2019/01/19/237_example.png)<br>
示例 1:

输入: head = [4,5,1,9], node = 5
输出: [4,1,9]
解释: 给定你链表中值为 5 的第二个节点，那么在调用了你的函数之后，该链表应变为 4 -> 1 -> 9.
示例 2:

输入: head = [4,5,1,9], node = 1
输出: [4,5,9]
解释: 给定你链表中值为 1 的第三个节点，那么在调用了你的函数之后，该链表应变为 4 -> 5 -> 9.
 

说明:

链表至少包含两个节点。
链表中所有节点的值都是唯一的。
给定的节点为非末尾节点并且一定是链表中的一个有效节点。
不要从你的函数中返回任何结果。

<br>
题解：

![](https://github.com/457251763/LeetCode/blob/master/image/T237.png)
如图，既然无法访问给定节点的父节点，那么就把之后的节点前移覆盖掉给定的节点，可以完成链表的删除。
Code：<br>
>class Solution {<br>public:    <br>void deleteNode(ListNode* node) {        <br>node->val=node->next->val;        <br>node->next = node->next->next;    <br>}<br>};



