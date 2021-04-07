#冒泡算法

##算法步骤
相邻两个数进行大小比较，若是他们在错误的位置（按照降序或者升序排列），重复以上操作一直到整个列表都被排序。
因此冒泡排序总的平均时间复杂度为 O(n2 )
##动画演示
![Algorithm Visualization](https://www.runoob.com/wp-content/uploads/2019/03/bubbleSort.gif)
##代码实现（python）

```
def bubble(arr):
    n = len(arr)
    # 两两数据需要交换的次数
    for i in range(n - 1):
        # 第一次循环 找到最大的数放在最后
        # i 值代表已经排序好的数
        for j in range(n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j + 1], arr[j] = arr[j], arr[j + 1]
    return arr


print(bubble([1, 2, 3, 1, 2, 5, 2]))

# 反序操作
def bubbleSort(arr):
    for i in range(len(arr) - 1, 0, -1):  # 反向遍历
        for j in range(0, i):  # 由于最右侧的值已经有序，不再比较，每次都减少遍历次数
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr
```





