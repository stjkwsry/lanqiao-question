# 输入与输出

```java
import java.util.*;

Scanner sc = new Scanner(System.in);
// nextDouble()...
int i = sc.nextInt();
// 不会读取空格，以回车作为结束符
// 可以在一行中以空格作为分隔符，输入多个字符串
String str = sc.next();
// 读取空格，以回车作为结束符
str = sc.nextLine();

// 可以以空格作为分隔符输入一组数组数据，也可以用回车作为分隔符
// 字符串还是不变，next() 可以用空格作为分隔符一行输入多个数据，也可以使用回车作为分隔符；nextLine() 只能以回车作为分隔符
int[] arr = new int[10];
for (int i = 0; i < arr.length; i++) {
    arr[i] = sc.nextInt();
}

// 输出后不换行
System.out.print("");
// 输出后自动换行
System.out.println("");
// 格式字符串，不自动换行
// %s-String, %d-int, %b-boolean, %.?f-float（?为保留的小数位数（四舍五入））
System.out.printf("%d", i);
```

# 字符串

```java
String str;

// 获取字符串的长度
int i = str.length();
// 返回 str2 在 str 中第一次出现的索引
int i = str.indexOf(str2);
// 返回 str2 在 str 中指定索引之后第一次出现的索引
int i = str.indexOf(str2, idx)
// 将 str 与 str2 比较，小于时返回 <0，等于时返回 0，大于时返回 >0
int i = str.compareTo(str2);

// 获取字符串指定索引（从 0 开始）上的字符
char c = str.charAt(idx);

// 判断 str 中是否包含 str2
boolean b = str.contains(str2);
// 判断两个字符串中的字符是否一致（不建议用“==”，因为它会判断字符串对象地址）
boolean b = str.equals(str2);

// 获取 str 中 [idx, str.length()-1] 上的子串
String s = str.subString(idx);
// 获取 str 中 [startIdx, endIdx-1] 上的子串
String s = str.subString(startIdx, endIdx);
// 以字符串参数为分割符，将字符串分割成字符串数组
String[] s = str.split(str2);
```

# 类型转换

```java
// 强制转换
int i = (int) 123.456;

// 封装类转换
Integer i = Integer.valueOf(123);
int i = i.intValue();
// 将字符串转换为基本类型
Integer i = Integer.parseInt("123");
// 将二进制字符串转换为十进制数
// 2，4，8，10，16，32
Integer i = Integer.parseInt("111101", 2);

// 将十进制整数转换成对应的进制字符串
// 转换为二进制字符串
String s = Integer.toBinaryString(123);
// 转换为八进制字符串
String s = Integer.toOctalString(123);
// 转换为十六进制字符串
String s = Integer.toHexString(123);
```

# 数组与集合

```java
import java.util.*;

int[] arr; 
// 升序排序
Arrays.sort(arr);
// 基本数据类型封装类数组支持降序排序
Integer[] arr;
Arrays.sort(arr, Collections.reverseOrder());
// 以“[1, 2, 3]”格式输出
Arrays.toString(arr);

List<Integer> list = new ArrayList();
// 添加
list.add(element);
// 将元素插入到 idx 上，其他元素后移
list.add(idx, element);
// 格式化输出
System.out.println(Arrays.toString(list.toArray()));

HashMap<Integer, Integer> hm = new HashMap();
// 添加
hm.put(key);
hm.put(key, value);
// 判断是否存在 key
boolean b = hm.containsKey(key);
// 键数组
Object[] keys = hm.keySet().toArray();
// 值数组
Object[] values = hm.values().toArray();
```

# 日期与时间

> 需要 JDK 1.8+ 版本。

```java
import java.time.*;

// month与day从1开始计算
LocalDate ld = LocalDate.of(year, month, day);
// 默认以“year-month-day”格式输出
System.out.println(ld);

// 年
int i = ld.getYear();
// 月，从 1 开始计算
int i = ld.getMonthValue();
// 日，从 1 开始计算
int i = ld.getDayOfMonth();
// 星期，返回枚举值，值为星期的全大写英文单词
DayOfWeek d = ld.getDayOfWeek();

// 往后推整数 n 天
ld = ld.plusDays(n);
```
