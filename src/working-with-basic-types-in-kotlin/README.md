<div dir="rtl">

# کار با Type های پایه ای

در کاتلین در واقع همه چیز یک شی (object) است. خب به عنوان مثال اگر به یک Integer نگاه کنیم، مثلا کد زیر:

</div>

```kotlin
var myInt : Int
```

<div dir="rtl">

در واقع Int یک شی است. درواقع ما تایپ های متفاوتی برای یک مقدار های عددی داریم، Byte ، Long ، Float ، Double . همینطور که میبینید ما یک سری تایپ داخلی برای متغیر ها داریم.

حالا اگه یادتون باشه گفتیم نیاز نیست توی کاتلین تایپ ها رو وقتی مقدار دهی کردیم بنویسیم

</div>

```kotlin
var myLong = 10
```

<div dir="rtl">

یعنی مثلا توی بالا کاتلین باید متوجه بشه که منظورمون چیه، ولی این اتفاق نمیفته و اگر myLong رو نگاه کنیم متوجه خواهیم شد که این مقدار یک Int است!  خب البته کاتلین راهی برای این قضیه داره، کافیه که ما عبارت بالا رو به صورت مقابل بنویسیم

</div>

```kotlin
var myLong = 10L
```

<div dir="rtl">

و حالا کاتلین متوجه میشه که شما Long میخواین.

حالا اگه شما میخواین تایپ های دیگه رو معرفی کنید میتونید به این صورت بنویسین.

</div>

```kotlin
val myLong = 10L
val myFloat = 100F
val myHex = 0x0F
val myBinary = 0xb01
```

<div dir="rtl">

توی کاتلین همونطور که گفتم نمیتونین همینجوری یک تایپ رو توی یک تایپ دیگه بریزین

</div>

```kotlin
val myInt = 10
val myLongAgain: Long = myInt
```

<div dir="rtl">

شما نمیتونید اینجوری که بالا نوشتم بنویسین ولی راهی هست که بتونین مقدار یک Int رو توی Long بریزین. باید از توابع اون تایپ استفاده کنید یعنی خط بالا رو به این صورت بنویسین

</div>

```kotlin
val myInt = 10
val myLongAgain: Long = myInt.toLong()
```
<div dir="rtl">

که درواقع اجازه میده یک مقدار رو تبدیل کنید به یک مقدار دیگه.

حالا بیاین بریم سراغ رشته ها،قطعه کد زیر رو ببینیم

</div>

```kotlin
val myChar = 'A'
val myString = "My String"
```

<div dir="rtl">

خب اگه دقت کنید کامپایلر با استفاده از " ‘ " متوجه میشه که این ایا کاراکتره یا ایا یک رشته است. 

</div>

```kotlin
val escapeCharacters = "A new Line \n"
```

<div dir="rtl">

میتونید از کاراکتر های پایان دهنده استفاده کنید.

</div>

```kotlin
val rawString = "Hello " +
        "This is second line" +
        "a third line"

val multipleLine = """
this is a string
and this is another line
"""
```

<div dir="rtl">

میتونید یک رشته رو در چند خط بنویسین.یک روش اینه که با استفاده از + در چند خط یک رشته رو بنویسید و یا این که با استفاده از 3 تا " " " بگین میخوایم یک رشته چند خطی بنویسیم. میتونید یک مقدار رو داخل یک رشته استفاده کنید.البته به دو روش که روش دوم خلاصه درس و کاتلینی تره.

</div>

```kotlin
val years = 10
val message = "A decade is " + years + " years"
val anotherMessage = "A decade is $years years"
```

<div dir="rtl">

اگر از همون روش دوم استفاده کردید و میخوایین از توابع داخلی اون متغییر استفاده کنید متونید این کار رو بکنید 

</div>

```kotlin
val name= "Mary"
val anotherOne = "length of name is ${name.length}"
```
