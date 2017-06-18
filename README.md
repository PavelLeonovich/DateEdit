# DateEdit
Simple way to edit date data

Key features:
<ul>
<li>date validation;</li>
<li>date format validation;</li>
<li>date format convertion;</li>
<li>easy date to unix convertion;</li>
<li>easy change year, month, week, day or hour.</li>
</ul>
Some examples:
<ul>
<li>$valid = DateEdit::validate("2017.02.03","Y.m.d");</li>
<li>$check = DateEdit::checkFormat("2017.02.03","Y.m.d");</li>
<li>$date = DateEdit::convertFormat("2017.02.03","Y.m.d","d-m-Y");</li>
<li>$date = DateEdit::dateToUnix("2017.06.18","Y.m.d");</li>
<li>$date = DateEdit::unixToDate(1497744000,"Y.m.d");</li>
<li>$date = DateEdit::changeYear("2017.02.03", "Y.m.d", 1, '+');</li>
<li>$date = DateEdit::changeMonth("2017.06.17", "Y.m.d", 1, '+');</li>
<li>$date = DateEdit::changeWeek("2017.06.17", "Y.m.d", 1, '+');</li>
<li>$date = DateEdit::changeDay("2017.06.17", "Y.m.d", 1, '+');</li>
<li>$date = DateEdit::changeHours("2017.06.17 23:39:00", "Y.m.d H:i:s", 1, '+');</li>
</ul>
