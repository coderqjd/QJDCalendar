# QJDCalendar
一款简单的日历的视图控件，支持"周历"和"月历"切换。
# 示例图片
<img src="https://github.com/coderqjd/QJDCalendar/blob/master/MonthCalendar.png" width="375" height="667" alt="图片描述文字"/>

<img src="https://github.com/coderqjd/QJDCalendar/blob/master/WeekCalendar.png" width="375" height="667" alt="图片描述文字"/>

# 安装
pod 'QJDCalendar'
# 如何使用
- 导入头文件
```objc
#import <QJDCalendar.h>
```
- 创建一个可以"周历"和"月历"相互切换的日历
```objc
    QJDCalendarView *calendarView = [QJDCalendarView calendarView];
    calendarView.frame = [UIScreen mainScreen].bounds;
    calendarView.delegate = self;
    [self.view addSubview:calendarView];
```
- 可以实现代理进行交互
```objc
- (void)calendarView:(UIView *)calendarView didSelectAtIndexPath:(NSIndexPath *)indexPath dateString:(NSString *)dateStr {
}
```
- 如果想要单独使用月历
```objc
    QJDMonthCalendarView *monthCalendarView = [QJDMonthCalendarView monthCalendarView];
    monthCalendarView.frame = [UIScreen mainScreen].bounds;
    [self.view addSubview:monthCalendarView];
```
- 如果想要单独使用周历
```objc
    QJDWeekCalendarView *weekCalendarView = [QJDWeekCalendarView weekCalendarView];
    weekCalendarView.frame = [UIScreen mainScreen].bounds;
    [self.view addSubview:weekCalendarView];
```
