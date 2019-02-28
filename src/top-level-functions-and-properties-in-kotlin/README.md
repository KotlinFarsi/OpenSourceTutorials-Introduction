<div dir="rtl">

# توابع و خصیصه های درجه اول

خب همینطور که میدونین ما توی کاتلین توابع Top-Level داشتیم و چیزی که توی جاوا تعریف نشده این گونه توابعه. چجوری میتونیم از اینگونه توابع استفاده کنیم ؟

یک کلاس به نام TopLevelFunctions میسازیم

</div>

```kotlin
fun prefix(prefix: String, value : String): String = "$prefix-$value"
```

<div dir="rtl">

و این تابع رو داخلش مینویسیم. در واقع کامپایلر وقتی این فایل رو کامپایل میکنه یک فایلی به نام TopLevelFunctionsKt.class میسازه

<img src="./output-1.PNG" />

یعنی درواقع کلاس TopLevelFunctions از فایل ToplevelFunctions جدا میشه! ما اگه کلاسی به همین نام در این فایل ایجاد کنیم و کامپایلش کنیم متوجه میشیم که فایل .class مربوط به اون کلاس رو جدا از فایل اصلی ساخته!

<img src="./output-2.PNG" />

و داخل کد هم همین قضیه برقراره، اگه بخوایم به فایل دسترسی پیدا کنیم باید از TopLevelFunctionKt استفاده کنیم و اگر به کلاس از TopLevelFunction.

</div>

```java
TopLevelFunctionsKt.prefix("Hi","Sina");
```

<div dir="rtl">

به همین راحتی. این قضیه برای خصیصه های Top-Level نیز برقراره ولی با این تفاوت که از getter و setter ها استفاده میکنیم.ولی البته که اگر بخواین میتونین به صورت field دسترسی داشته باشین و راهش استفاده از const هه . به راحتی کد زیر

</div>

```kotlin
const val year = 2017
```

<div dir="rtl">

البته یادتون باشه که نمیتونین برای متغییر های var از const استفاده کنین!

</div>
