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