<div dir="rtl">

# constant ها

مبحث بعدی که میخوام دربارش صحبت کنم Constant هاست. ما خیلی درمورد constant ها صحبت نکردیم تنها جایی که اشاره ای بهش شد زمانی بود که میخواستیم یک object بسازیم. خب حالا چجوری میتونیم Constant ها رو بسازیم، در واقع ما نحوه ساخت اون ها رو قبلا دیدیم

</div>

```kotlin
object Copyright {
    val author = "Sina Darvishi"
}
```

<div dir="rtl">

یک object ساختیم و یک خصیصه بهش دادیم. همین. در واقع فرقی با ساختن یک object که قبلا دیدیم نداره. ما درواقع از همین به عنوان constant استفاده میکنیم.

و من میتونم توی هرجایی ازش استفاده کنم

</div>

```kotlin
object Copyright {
    val author = "Sina Darvishi"
}

fun main(args: Array<String>) {
    Copyright.author
}
```


<div dir="rtl">

و درواقع من هر موقع پکیجش رو اضافه کنم میتونم از این استفاده کنم.

همچنین ما میتونیم Constant ها رو به عنوان Top-Level معرفی کنیم

</div>

```kotlin
val CopyrightAuthor = "Sina Darvishi"

object Copyright {
    val author = "Sina Darvishi"
}

fun main(args: Array<String>) {
    Copyright.author
    CopyrightAuthor
}
```

<div dir="rtl">

خب درواقع این سوال پیش میاد که آیا من باید Constant ها رو توی جاهای رندوم قرارشون بدم و هر موقع خواستم صداشون بزنم؟

درواقع این به معماری برنامتون بستگی داره، به نظر من این خیلی بهتره که Constant ها رو توی یک Object دسته بندی کنین تا این که همه رو در هرجای برنامه استفاده کنیم.

مثلا وقتی میخوایم تنظیمات یک Camera رو به صورت Constant نگه داری کنیم، یک object به عنوان CameraSettings درست کنیم و constant هارو توی اون نگه داریم.

</div>
