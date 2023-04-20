**设计一张日期维度表**<br />表名称：DIM_PUB_DATE

**具体属性值：**

| 字段名称 | 字段类型 | 字段描述 | 示例 |
| --- | --- | --- | --- |
| ds | string | Id（主键） | 20210624 |
| d_date | string | 日期 | 2021-06-24 |
| d_datetime | string | 日期（包含时分秒） | 2021-06-24 00:00:00 |
| y_ds | string | 去年id | 20200624（减12月） |
| y_date | string | 去年日期 | 2020-06-24 |
| y_datetime | string | 去年日期（包含时分秒） | 2020-06-24 00:00:00 |
| d_year | string | 年份 | 2021 |
| d_yearstartday | string | 年初日 | 2021-01-01 |
| y_year | string | 去年份 | 2020 |
| y_yearstartday | string | 去年初日 | 2020-01-01 |
| d_month | string | 月份 | 2021-06 |
| d_monthstartday | string | 月初日 | 2021-06-01 |
| d_monthendday | string | 月尾日 | 2021-06-30 |
| y_month | string | 去年月份 | 2020-06 |
| y_monthstartday | string | 去年月初日 | 2020-06-01 |
| y_monthendday | string | 去年月尾日 | 2020-06-30 |
| d_quarter | string | 季度 | Q2 |
| d_yearquarter | string | 季度（带年份） | 2021-2 |
| week | string | 星期（数字表示） | 1,2,3,4,5,6,7：1代表星期一 |
| d_week | string | 星期几 | 星期一 |
| d_dayofyear | string | 当年第几天 | D100 |
| d_dayofmonth | string | 当月第几天 | D24 |
| d_dayofweek | string | 当周第几天 | D4 |
| d_weekofmonth | string | 当月第几周 | W4 |
| d_weekofyear | string | 当年第几周 | W24 |
| is_weekend | string | 是否周末 | 1：是，2：否 |
| day_type | string | 日历天类型 | 0：节假日，1：工作日，2：休息日<br />（调休也属于工作日） |
| hol_name | string | 节假日名称 | 元旦，调休，春节，清明节，劳动节，端午节，中秋节，国庆节 |


**生成方法： **<br />使用python生成一张维度表，考虑到通用性，可以先写到Excel或者CSV里面，然后自定义写入到hive或者odps里面去。
