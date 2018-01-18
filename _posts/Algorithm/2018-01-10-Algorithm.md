---
layout: post
title: "算法（Algorithm）"
date: 2018-01-10
tag: "Java"
detail: 算法的分类以及经典算法题的代码实现，修炼内功
img: 
---

* content
{:toc}


## 二叉树



```

    int count = 0;
	
    public  Tree buildTree(int[] a, int s1, int e1,int[] b, int s2, int e2){

        if(s1>e1||s2>e2){
            return null;
        }
        Tree tree = new Tree();
         tree.value = a[count];
        int index = getIndex(b, a[count]);
        count++;
        tree.left = buildTree(a, count, s1+index, b, s2, index-1);
        tree.right = buildTree(a, count, s1+e2-index, b, index+1, e2);

        return tree;
    }
    private int getIndex(int[] b,int value){
        int count = 0;
        for(int tmp:b){
            if(tmp==value){
                return count;
            }
            count++;
        }
        return 0;
    }

    public void printPre(Tree tree){
        if(tree != null){
            System.out.print(tree.value);
        }
        if(tree.left != null){
            printPre(tree.left);
        }
        if(tree.right != null){
            printPre(tree.right);
        }

    }
    public void printMid(Tree tree){
        if(tree.left != null){
            printMid(tree.left);
        }
        if (tree != null){
            System.out.print(tree.value);
        }
        if(tree.right != null){
            printMid(tree.right);
        }

    }
    public void printLast(Tree tree){
        if(tree.left != null){
            printLast(tree.left);
        }
        if(tree.right != null){
            printLast(tree.right);
        }
        if (tree != null){
            System.out.print(tree.value);
        }

    }

```





## 链表 

1. 链表逆序（不可使用其他空间）
 
 
## 十大经典排序算法

* 插入排序： 直接插入，希尔排序

* 选择排序： 简单选择排序，堆排序

* 交换排序： 冒泡排序，快速排序

* 归并排序

* 基数排序


## 剑指offfer 所有算法

第01-10题


【剑指Offer学习】【面试题02：实现Singleton 模式——七种实现方式】

【剑指Offer学习】【面试题03：二维数组中的查找】

【剑指Offer学习】【面试题04：替换空格】

【剑指Offer学习】【面试题05：从尾到头打印链表】

【剑指Offer学习】【面试题06：重建二叉树】

【剑指Offer学习】【面试题07：用两个栈实现队列】

【剑指Offer学习】【面试题08：旋转数组的最小数字】

【剑指Offer学习】【面试题09：斐波那契数列】

【剑指Offer学习】【面试题10：二进制中1 的个数】

第11-20题

【剑指Offer学习】【面试题11：数值的整数次方】

【剑指Offer学习】【面试题12：打印1 到最大的n 位数】

【剑指Offer学习】【面试题13：在O（1）时间删除链表结点】

【剑指Offer学习】【面试题14：调整数组顺序使奇数位于偶数前面】

【剑指Offer学习】【面试题15：链表中倒数第k个结点】

【剑指Offer学习】【面试题16：反转链表】

【剑指Offer学习】【面试题17：合并两个排序的链表】

【剑指Offer学习】【面试题18：树的子结构】

【剑指Offer学习】【面试题19：二叉树的镜像】

【剑指Offer学习】【面试题20：顺时针打印矩阵】

第21-30题

【剑指Offer学习】【面试题21：包含min函数的钱】

【剑指Offer学习】【面试题22：栈的压入、弹出序列】

【剑指Offer学习】【面试题23：从上往下打印二叉树】

【剑指Offer学习】【面试题24：二叉搜索树的后序遍历序列】

【剑指Offer学习】【面试题25：二叉树中和为某一值的路径】

【剑指Offer学习】【面试题26：复杂链表的复制】

【剑指Offer学习】【面试题27：二叉搜索树与双向链表】

【剑指Offer学习】【面试题28：字符串的排列】

【剑指Offer学习】【面试题29：数组中出现次数超过一半的数字】

【剑指Offer学习】【面试题30：最小的k个数】

第31-40题

【剑指Offer学习】【面试题31：连续子数组的最大和】

【剑指Offer学习】【面试题32：求从1到n的整数中1出现的次数】

【剑指Offer学习】【面试题33：把数组排成最小的数】

【剑指Offer学习】【面试题34：丑数】

【剑指Offer学习】【面试题35：第一个只出现一次的字符】

【剑指Offer学习】【面试题36：数组中的逆序对】

【剑指Offer学习】【面试题37：两个链表的第一个公共结点】

【剑指Offer学习】【面试题38：数字在排序数组中出现的次数】

【剑指Offer学习】【面试题39：二叉树的深度】

【剑指Offer学习】【面试题40：数组中只出现一次的数字】

第41-50题

【剑指Offer学习】【面试题41：和为s 的两个数字vs 和为s 的连续正数序列】

【剑指Offer学习】【面试题42：翻转单词顺序vs左旋转字符串】

【剑指Offer学习】【面试题43 : n 个锻子的点数】

【剑指Offer学习】【面试题44：扑克牌的顺子】

【剑指Offer学习】【面试题45：圆圈中最后剩下的数字(约瑟夫环问题)】


【剑指Offer学习】【面试题47：不用加减乘除做加法】


【剑指Offer学习】【面试题49：把字符串转换成整数】

【剑指Offer学习】【面试题50：树中两个结点的最低公共祖先】

第51-60题

【剑指Offer学习】【面试题51：数组中重复的数字】

【剑指Offer学习】【面试题52：构建乘积数组】

【剑指Offer学习】【面试题53：正则表达式匹配】

【剑指Offer学习】【面试题54：表示数值的字符串】

【剑指Offer学习】【面试题55：字符流中第一个不重复的字符】

【剑指Offer学习】【面试题56：链表中环的入口结点】

【剑指Offer学习】【面试题57：删除链表中重复的结点】

【剑指Offer学习】【面试题58：二叉树的下一个结点】

【剑指Offer学习】【面试题59：对称的二叉树】

【剑指Offer学习】【面试题60：把二叉树打印出多行】

第61-67题

【剑指Offer学习】【面试题61：按之字形顺序打印二叉树】

【剑指Offer学习】【面试题62：序列化二叉树】

【剑指Offer学习】【面试题63：二叉搜索树的第k个结点】

【剑指Offer学习】【面试题64：数据流中的中位数】

【剑指Offer学习】【面试题65：滑动窗口的最大值】

【剑指Offer学习】【面试题66：矩阵中的路径】

【剑指Offer学习】【面试题67：机器人的运动范围】


## 其他

* 并查集

* KMP

  





