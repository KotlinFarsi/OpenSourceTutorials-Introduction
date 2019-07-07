<div dir="rtl">

# typealias در کاتلین


خب به قسمتی رسیدیم که دقیقا به بخش خاصی تعلق ندارن ولی یکی از ابزاری که میتونه خیلی کمکمون کنه.
typealias ها به ما این امکان رو میدن که بتونیم یک اسم جایگزین برای کلاس هایی که میخوایم استفاده کنیم بزاریم. 


مثلا میتونیم اسم یکی از کلاس هامون رو کوتاه کنیم و از این به بعد از اون اسم جایگزین استفاده کنیم
مثلا فرض کنید که کلاسی به این اسم
</div>



```kotlin
MutableMap<String , MutableList<File>>
```


<div dir="rtl">

و خیلی جاها قراره از این کلاس جاهای مختلفی استفاده کنیم که یقینا برای اینکه هربار این کلاس رو فراخونی کنیم و ازش نمونه بسازیم یه مقدار کلافه کننده ست
خوب اینجاست این ابزار در کاتلین به کمکمون میاد و میتونیم یک اسم جایگزین برای همچین کلاسی بنویسیم و از این به بعد از این اسم به جای استفاده از اسم طولانی کلاس استفاده کنیم
</div>

```kotlin
typealias FileTable = MutableMap<String, MutableList<File>>
```

<div dir="rtl">
حتی میشه از اونا برای اسم جایگزین توی inner class ها استفاده کرد:
</div>


```kotlin
class Food {
    inner class Pizza{
        //Codes...
    }
}

typealias PizzaInnerFood = Food.Pizza
```

<div dir="rtl">
نکته ای که باید بهش دقت کنید اینه که typealias ها یک کلاس یا تایپ جدیدی رو ارائه نمیدن بلکه فقط یه اسم جایگزین رو برای یک کلاس ارائه میدن.
</div>


```kotlin
typealias ArrName = ArrayList<String>;

MainActivity : AppCompatActivity(){
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
        val names = ArrName()
        names.add("Ali")
        names.add("Kamran")
        names.add("Sara")
   }
}
```
