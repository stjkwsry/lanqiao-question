# 输入与输出

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        // nextDouble()...
        int i = sc.nextInt();
        // 不会读取空格，以回车作为结束符
        // 可以在一行中以空格作为分隔符，输入多个字符串
        String str = sc.next();
        // 读取空格，以回车作为结束符
        str = sc.nextLine();
        
        // 输出后不换行
        System.out.print("");
        // 输出后自动换行
        System.out.println("");
        // 格式字符串，不自动换行
        // %s-String, %d-int, %b-boolean, %.?f-float（?为保留的小数位数（四舍五入））
        System.out.printf("%d", i);
    }
}
```

# 字符串

```java
public class Main {
    public static void main(String[] args) {
        String str, str2;
        // 获取字符串的长度
        str.length();
        // 获取字符串指定索引（从0开始）上的字符
        char c = str.charAt(idx);
        // 以参数为分割符，将字符串分割成字符串数组
        String[] s = str.split("");
        // 将str与字符串str2比较，小于时返回<0，等于时返回0，大于时返回>0
        int i = str.compareTo(str2);
    }
}
```

# 数组与集合

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int[] arr;
        // 以“[1, 2, 3]”格式输出
        Arrays.toString(arr);
    }
}
```

# 日期与时间

> JDK 1.8+

```java
import java.time.*;

public class Main {
    public static void main(String[] args) {
        // month与day从1开始计算
        LocalDate ld = LocalDate.of(year, month, day);
        // 默认以“year-month-day”格式输出
        System.out.println(ld);
        
        // 年
        ld.getYear();
        // 月，从1开始计算
        ld.getMonthValue();
        // 日，从1开始计算
        ld.getDayOfMonth();
        // 星期，返回枚举值，值为星期的全大写英文单词
        ld.getDayOfWeek();
        
        // 往后推n天
        ld = ld.plusDays(n);
    }
}
```
