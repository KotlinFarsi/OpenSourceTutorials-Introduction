<div dir="rtl">

# deconstructing values

ما دیدیم که زمانی که داریم به دوگانه ها یا سه گانه ها دسترسی پیدا میکنیم، هر دسترسی رو با استفاده از first و second و third انجام میدیم، خب البته مشکلی هم نیست ولی خب یکی از هدف های کاتلین این بود که دقیق تر کد بزنیم و این که بگیم اولی یا دومی یا سومی دقیق نیست یعنی اصلا اولی یا دومی چی هستند؟ و درواقع من باید برم به محل تعریف تابع تا متوجه بشم اولی چیه یا دومی یا سومی.

به عنوان مثال کدی که نوشتیم رو نگاه کنین:

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

خب ما اینجا result رو داریم و در نتیجه میتونیم first و second رو بدست بیاریم، ولی first چه مقداری رو بهمون میداد ؟ یا second چی؟ خب برای این که بفهمیم میریم بالا و نگاه میکنیم میبینیم که String و Long رو داریم برمیگردونیم ولی بازم دیدگاهی نداریم که این دو نماینده چه متغییر هایی بودن.

کاتلین برای حل این مشکل بهمون این امکان رو میده که متغییر هارو بشکنین، به عنوان مثال کد زیر رو نگاه کنین:

</div>

```kotlin
fun capitalAndPopulation(country: String): Pair<String,Long>{
    return Pair("Madrid",2000000)
}

fun main(args: Array<String>) {
    val (capital,population) = capitalAndPopulation("Spain")

    println(capital)
    println(population)
}
```

<div dir="rtl">

در واقع این به معنیه اینه که من میتون به جای این که جواب رو توی یک متغیر بریزم، جواب رو توی دومتغیر با نام دلخواه بریزم.البته این شکستن تنها برای چندگانه ها نیست. اگر به کد تعریف دوگانه ها یا سه گانه ها مراجعه کنید(در IntelliJ IDEA دکمه ctrl را نگه دارید و موس را برروی Pair ببرید و کلیک کنید) متوجه خواهید شد که درواقع دوگانه ها یا سه گانه ها کلاس های دیتای از پیش تعریف شده ای هستند که ما از انها استفاده میکنیم. پس همینطور که ما میتونیم برای دوگانه ها به عنوان مثال مقادیر خروجی رو بشکنیم، همین کار رو برای کلاس های دیتا هم میتونیم انجام بدیم. به عنوان مثال

</div>

```kotlin
data class CustomerKotlin(var id: Int, var name: String, var email: String){
    override fun toString(): String {
        return "{\"id\": \"$id\", \"name\": \"$name\"}"
    }
}
 
fun main(args: Array<String>) {
    val (id,name,email) = CustomerKotlin(1,"Sina","Sinadarvi@gmail.com")
    println(id)
    println(name)
    println(email)
}
```
