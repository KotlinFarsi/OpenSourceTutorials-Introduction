<div dir="rtl">

# کارکردن با کلاس های abstract در کاتلین

اگر با مفهوم abstract اشنا باشید کلاسی  مد نظرمون هست که نمیتونیم ازش نمونه ای رو بسازیم ولی میتونیم از اون ارثبری کنیم.

</div>

```kotlin
abstract class StoredEntity

class Employee: StoredEntity()

fun main(args: Array<String>) {
    val se = Employee()
}
```

<div dir="rtl">

خب حالا با خودتون میگین چه فایده ای داره که از کلاس های abstract استفاده کنیم؟ خب در واقع کلاس های abstract تفاوتی با کلاس های پایه ای دارند و اونم اینه که یک کلاس abstract میتونه هم مانند یک کلاس معمولی یک تابع/متغییر که مقدار دهی شده داشته باشه، و هم یک تابع abstract داشته باشه ک پیاده سازی نشده. مثلا فرض کنید که چندین کلاس داریم که یک سری کار انجام میدن ولی محتوای کارشون شبیه به هم با اندکی تفاوته، برای همین میایم یک کلاس abstract میسازیم و تابع abstract اون رو هم میسازیم ولی بدنه تابع رو توی هر کدوم از کلاس ها بسته به نوع کلاسمون میسازیم.مثال زیر رو نگاه کنین:

</div>

```kotlin
abstract class StoredEntity{
    abstract fun store()
}

class Employee: StoredEntity() {
    
    override fun store() {
        TODO("not implemented")
    }
}
```

<div dir="rtl">

البته تموم عضو های کلاس abstract نیازی به abstract بودن خودشون ندارن:

</div>

```kotlin
abstract class StoredEntity{
    val isActive = true
    
    abstract fun store()
    
    fun status():String{
        return isActive.toString()
    }
}

class Employee: StoredEntity() {
    override fun store() {
        TODO("not implemented")
    }
}

fun main(args: Array<String>) {
    val se = Employee()

    se.isActive
    se.status()
}
```

<div dir="rtl">

فقط همینطور که میدونید ما نمیتونیم توی main دوباره به isActive مقدار بدیم.

</div>


