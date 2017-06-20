# DateEdit
Simple way to edit date data

Key features
<ul>
<li>date validation;</li>
<li>date format validation;</li>
<li>date format convertion;</li>
<li>easy date to unix convertion;</li>
<li>easy change year, month, week, day or hour.</li>
</ul>

Some examples
```php
$valid = DateEdit::validate("2017.02.03","Y.m.d");
$check = DateEdit::checkFormat("2017.02.03","Y.m.d");
$date = DateEdit::convertFormat("2017.02.03","Y.m.d","d-m-Y");
$date = DateEdit::dateToUnix("2017.06.18","Y.m.d");
$date = DateEdit::unixToDate(1497744000,"Y.m.d");
$date = DateEdit::changeYear("2017.02.03", "Y.m.d", 1, '+');
$date = DateEdit::changeMonth("2017.06.17", "Y.m.d", 1, '+');
$date = DateEdit::changeWeek("2017.06.17", "Y.m.d", 1, '+');
$date = DateEdit::changeDay("2017.06.17", "Y.m.d", 1, '+');
$date = DateEdit::changeHours("2017.06.17 23:39:00", "Y.m.d H:i:s", 1, '+');
```
