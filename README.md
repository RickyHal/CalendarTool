# CalendarTool
A tool for lunar calendar conversion developed by kotlin

# CalendarTool
一个农历新历转换工具，使用kotlin编写。

# 方法说明
* toChinaMonth(m: Int): String<br/>
```
     公历月转农历月
     @param m month
     @return 1->正月，2->二月，...，10->十月，11->冬月，12->腊月
```
* toChinaDay(d: Int): String
```
     公历日转农历日
     @param d day
     @return 1->初一，11->十一，21->廿一，30->卅十
```
* getAnimal(y: Int): String
```
     获取生肖
     @param y full year
     @return 2021->牛
```
* solar2lunar(y: Int, m: Int, d: Int): CalendarInfo?
```
     公历转农历
     @param y full year : 2021
     @param m month : 2
     @param d day : 26
     @return [CalendarInfo]
```
* lunar2solar(y: Int, m: Int, d: Int): CalendarInfo?
```
     农历转公历
     @param y full year : 2021
     @param m month : 1
     @param d day : 15
     @param isLeapMonth is leap month，是否是闰月
     @return [CalendarInfo]
```

## CalendarInfo
```
data class CalendarInfo(
        val lYear: Int,         // 农历年
        val lMonth: Int,        // 农历月
        val lDay: Int,          // 农历日
        val Animal: String,     // 生肖
        val IMonthCn: String,   // 中文农历月
        val IDayCn: String,     // 中文农历日
        val cYear: Int,         // 公历年
        val cMonth: Int,        // 公历月
        val cDay: Int,          // 公历日
        val gzYear: String,     // 干支年
        val gzMonth: String,    // 干支月
        val gzDay: String,      // 干支日
        val isToday: Boolean,   // 是否是今天
        val isLeap: Boolean,    // 是否是闰月
        val nWeek: Int,         // 当前日是一周中的第几天
        val ncWeek: String,     // 中文星期
        val isTerm: Boolean,    // 是否是节气
        val Term: String? = null// 节气
)
```

## License

```text
Copyright 2018 Huang JinQun

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
