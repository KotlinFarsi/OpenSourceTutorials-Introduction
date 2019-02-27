<div dir="rtl">

# توابعِ عضو در کاتلین


ما دیدیم که چگونه یه تابع Top-Level بسازیم، اما به هرحال کاتلین یه زبون شی گراست و بنابراین باید بتونیم داخل کلاس هم تابع بنویسیم که به این تابع ها Member-Functions میگن.

ولی خب تعریف تابع داخل کلاس خیلی راه حل سر راستی داره، به همون راحتی که قبلا توی یک فایل تابع مینوشیتم، مثلا کد زیر رو نگاه کنین

</div>

```kotlin
class Customer(var id: Int, var name: String, var yearOfBirth: Int){

    fun customerAsString(){
        println("id : $id - name : $name")
    }
}
```

<div dir="rtl">

که تابعمون دو خاصیت رو از کلاسمون چاپ میکنه.

برای استفاده ازش هم کافیه از شی که از کلاسمون ساختیم تابع رو صدا بزنیم

</div>

```kotlin
fun main(args: Array<String>) {
    var customer = Customer(10, "Sina",1995)
    
    customer.customerAsString()
}
```
