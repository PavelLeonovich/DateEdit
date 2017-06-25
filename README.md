# DateEdit
Simple way to edit date data

## Key features
<ul>
<li>date validation;</li>
<li>date format validation;</li>
<li>date format convertion;</li>
<li>easy date to unix convertion;</li>
<li>easy change year, month, week, day or hour.</li>
</ul>

## Some examples
### validate
```php
// Description:
boolean validate ( string $date , string $format )

$valid = DateEdit::validate("2017.02.03","Y.m.d");
// result: $valid = true

$valid = DateEdit::validate("2017.13.03","Y.m.d");
// result: $valid = false
```
### checkFormat
```php
// Description:
boolean checkFormat ( string $date , string $format )

$check = DateEdit::checkFormat("2017.02.03","Y.m.d");
// result: $check = true

$check = DateEdit::checkFormat("03.02.2017","Y.m.d");
// result: $check = false
```
### convertFormat
```php
// Description:
string convertFormat ( string $date , string $informat , string $outformat )

echo DateEdit::convertFormat("2017.02.03","Y.m.d","d-m-Y");
// result: 03-02-2017
```
### dateToUnix
```php
// Description:
int dateToUnix ( string $date , string $format )

echo DateEdit::dateToUnix("2017.06.18","Y.m.d");
// result: 1497744000
```
### unixToDate
```php
// Description:
string unixToDate ( int $date , string $format )

echo  DateEdit::unixToDate(1497744000,"Y.m.d");
// result: 2017.06.18
```
### changeDate
```php
// Description:
string changeDate( string $date , string $format [, string $period = 'day' [, int $NUM = 1 [, string $direction = '+' ]]] )

echo  DateEdit::changeDate( "2017.02.03" , "Y.m.d" , 'day', 1, '+');
// result: 2017.02.04
```
### changeYear
```php
// Description:
string changeYear ( string $date , string $format [, int yearN = 1 [, string direction = '+' ]] )

echo  DateEdit::changeYear("2017.02.03", "Y.m.d", 1, '+');
// result: 2018.02.03
```
### changeMonth
```php
// Description:
string changeMonth ( string $date , string $format [, int monthN = 1 [, string direction = '+' ]] )

echo  DateEdit::changeMonth("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.07.17
```
### changeWeek
```php
// Description:
string changeWeek ( string $date , string $format [, int weekN = 1 [, string direction = '+' ]] )

echo  DateEdit::changeWeek("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.06.24
```
### changeDay
```php
// Description:
string changeDay ( string $date , string $format [, int dayN = 1 [, string direction = '+' ]] )

echo  DateEdit::changeDay("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.06.18
```
### changeHours
```php
// Description:
string changeHours ( string $date , string $format [, int hoursN = 1 [, string direction = '+' ]] )

echo  DateEdit::changeHours("2017.06.17 23:39:00", "Y.m.d H:i:s", 1, '+');
// result: 2017.06.18 00:39:00
```
