<div dir="rtl">

# چندتایی ها (Tuples)

چندگانه ها زمانی استفاده میشن که شما به عنوان مثال خروجی یک تابع رو بخواین به صورت یک مجموعه دوگانه یا سه گانه برگردونید. باید در نظر داشته باشین که اگر تعداد خروجی هاتون بیشتر از 3 تا هست باید از کلاس ها استفاده کنید و چندگانه ها در کاتلین تا سه گانه ها بیشتر پشتیبانی نمی شوند.

خب اول بیاین یک تابع درست کنیم که یک دوگانه از جمله هارو برگردونه. مثلا یک تابع داشته باشیم که قراره اسم کشور رو بگیره و اسم پایتخت و جمعیت رو برگردونه.

</div>

```kotlin
fun capitalAndPopulation(country: String): Pair<String,Long>{
    return Pair("Madrid",2000000)
}

fun main(args: Array<String>) {
    val result = capitalAndPopulation("Spain")
    println(result.first)
    println(result.second)
}
```

<div dir="rtl">

خروجی تابعمون به صورت Pair هستش و وقتی میخوایم از تابع استفاده کنیم کافیه بگیم متغیر اول رو میخوایم یا دوم.

حالا اگه بخوایم یک سه گانه رو برگدونیم به این روش انجامش میدیم.

</div>

```kotlin
fun countryInformation(country: String): Triple<String,String,Long>{
    return Triple("Madrid", "Europe",2300000)
}

fun main(args: Array<String>) {
    val countryInfo = countryInformation("Spain")
    println(countryInfo.first)
    println(countryInfo.second)
    println(countryInfo.third)
}
```
