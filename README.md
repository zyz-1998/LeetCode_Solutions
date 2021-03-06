# LeetCode Solutions
* [剑指offer](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/A、剑指offer.md)
* [LeetCode](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/B、LeetCode.md)
* [shell](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/C、shell.md)
* [多线程](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/D、多线程.md)
* [专题](https://github.com/FangChao1086/Data_structures_and_algorithms/tree/master/专题)
  * [数组](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/专题/数组.md)  
  * [排序](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/专题/排序.md)
  * [链表](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/专题/链表.md)
  * [二叉树](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/专题/二叉树.md)
  * [动态规划](https://github.com/FangChao1086/Data_structures_and_algorithms/blob/master/专题/动态规划.md)
  * [回溯](https://github.com/FangChao1086/data_structures_and_algorithms/blob/master/专题/回溯.md)
  * [栈与队列](https://github.com/FangChao1086/data_structures_and_algorithms/blob/master/专题/栈与队列.md)
  * [数位问题](https://github.com/FangChao1086/data_structures_and_algorithms/blob/master/专题/数位问题.md)
  * [并查集](https://blog.csdn.net/weixin_43824059/article/details/88535734)

## 基础
### 输入
* 数据个数未知
  ```cpp
  1 3 5 10

  // C++
  vector<int> v;
  int tmp;
  while(cin >> tmp){
      v.push_back(tmp);
      if (getchar() == '\n')
          break;
  }
  ```

### 生成数据(结构)
```cpp
// 二维数组
int dp[n][m];  // 方法1
memset(dp,0,sizeof(dp));  // 用0填充
vector<vector<int>> dp(n,vector<int>(m,0));  // 方法2；n*m填充0
vector<int> res(input.begin(), input.begin() + k);  // 方法3；input是已经存在的vector

// 优先队列  最大最小堆
priority_queue<pair<int,int>> pq;  // 最大堆，默认
priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq; // 最小堆
```
### 数据处理
```cpp
// 将res（vector类型）中的元素反向
vector<int>(res.rbegin(), res.rend()); 

// 累加 vector 中的值
int sum = accumulate(A.begin(), A.end(), 0);  // 其中 A 是vector， 0是代表累加的初值为0；

// 排序(根据pair中的第二个关键字降序)
#include"algorithm"
bool cmp2(pair<int, int> a, pair<int, int> b) {
    return a.second > b.second; 
}
vector<pair<int, int>> vec;
sort(vec.begin(), vec.end(), cmp2);
```

### 数据类型转换
```cpp
// char 转 string
// 假设mp[0]是char;
string str;
str.push_back(mp[0]);

// string 转 int
string str = "123";
int n = atoi(str.c_str());  // 其中 .c_str() 必须要有
cout << n;  // 123
```
