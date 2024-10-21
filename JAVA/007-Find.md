`排序`
--

`> 内部排序`

`指将需要处理的所有数据都加载到内部存储器中进行排序 包括交换式排序法、选择式排序法和插入式排序法`

`> 外部排序`

`数据量过大无法全部加载到内存中 需要借助外部存储进行排序 包括合并排序法和直接合并排序法`

`冒泡排序法`
--

`冒泡排序的基本思想是 使值较大的元素逐渐从前移向后部就象水底下的气泡一样逐渐向上冒` 

```java
public static void main(String[] args) {
    int arr[] = {5,4,3,2,1};
    int temp = 0;
    for (int i = 0; i < arr.length - 1; i++) {
        for (int j = 0; j < arr.length - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

`选择排序`
--

`选择排序的基本思想是 如果有N个元素需要排序那么从 N 个元素中找到最小的那个元素与前面置上的元素交换`

```java
public static void main(String[] args) {
    int arr[] = {5,4,3,2,1};
    int temp = 0;
    for(int i = 0;i<arr.length;i++) {
        int min = i;
        for(int j = i;j<arr.length;j++) {
            if(arr[j] <= arr[min]) {
                min = j;
            }
        }
        temp = a[min];
        a[min] = a[i];
        a[i] = temp;
    }
}
```

`顺序查找 二分查找`
--
