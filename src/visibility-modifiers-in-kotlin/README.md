<div dir="rtl">

#  visibility modifier ها در کاتلین
اگه دقت کرده باشین در تموم کد هایی که تا الان نوشیتم از هیچ گونه visibility-modifier ای استفاده نکردیم. و در واقع در کاتلین این قرارداد هست که visibility-modifier پیش فرض public است.

توی کاتلین 4 نوع visibility-modifier داریم:
-	Public که پیشفرضمونه و از همه جا قابل دسترسیه
برای Top-Level-Declaration ها ( منظور تموم تعریف هایی که به صورت Top-level انجام میشه، مثلا Top-level-function ها )
-	Private که تنها از داخل همون فایلی که تعریف شده قابل دسترسیه
-	Internal که در واقع این اجازه رو میده که از هرجای برنامه بتونیم به اون دسترسی داشته باشیم، تازمانی که داخل همون module که توش تعریف شده باشیم. درواقع module اینجا منظورمون gradle module ، maven module و غیره و امثال این هاست
برای کلاس ها ما 3 نوع Visibility-modifier داریم
-	Private تنها دسترسی رو به عضو های یک class میده
-	Protected به مانند private میمونه ولی علاوه بر اون دسترسی رو به subclass ها هم میده
-	Internal در واقع اجازه میده که هر چیزی داخل module به اون دسترسی داشته باشه.
