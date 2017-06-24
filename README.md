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
boolean validate ( string $date , string $format )
```php
$valid = DateEdit::validate("2017.02.03","Y.m.d");
// result: $valid = true

$valid = DateEdit::validate("2017.13.03","Y.m.d");
// result: $valid = false
```
### checkFormat
boolean checkFormat ( string $date , string $format )
```php
$check = DateEdit::checkFormat("2017.02.03","Y.m.d");
// result: $check = true

$check = DateEdit::checkFormat("03.02.2017","Y.m.d");
// result: $check = false
```
### convertFormat
string convertFormat ( string $date , string $informat , string $outformat )
```php
echo DateEdit::convertFormat("2017.02.03","Y.m.d","d-m-Y");
// result: 03-02-2017
```
### dateToUnix
int dateToUnix ( string $date , string $format )
```php
echo DateEdit::dateToUnix("2017.06.18","Y.m.d");
// result: 1497744000
```
### unixToDate
string unixToDate ( int $date , string $format )
```php
echo  DateEdit::unixToDate(1497744000,"Y.m.d");
// result: 2017.06.18
```
### changeDate
string changeDate( string $date , string $format [, string $period = 'day' [, int $NUM = 1 [, string $direction = '+' ]]] )
```php
echo  DateEdit::changeDate( "2017.02.03" , "Y.m.d" , 'day', 1, '+');
// result: 2017.02.04
```
### changeYear
string changeYear ( string $date , string $format [, int yearN = 1 [, string direction = '+' ]] )
```php
echo  DateEdit::changeYear("2017.02.03", "Y.m.d", 1, '+');
// result: 2018.02.03
```
### changeMonth
string changeMonth ( string $date , string $format [, int monthN = 1 [, string direction = '+' ]] )
```php
echo  DateEdit::changeMonth("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.07.17
```
### changeWeek
string changeWeek ( string $date , string $format [, int weekN = 1 [, string direction = '+' ]] )
```php
echo  DateEdit::changeWeek("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.06.24
```
### changeDay
string changeDay ( string $date , string $format [, int dayN = 1 [, string direction = '+' ]] )
```php
echo  DateEdit::changeDay("2017.06.17", "Y.m.d", 1, '+');
// result: 2017.06.18
```
### changeHours
string changeHours ( string $date , string $format [, int hoursN = 1 [, string direction = '+' ]] )
```php
echo  DateEdit::changeHours("2017.06.17 23:39:00", "Y.m.d H:i:s", 1, '+');
// result: 2017.06.18 00:39:00
```
