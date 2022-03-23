# 1. Project maqsadi 

Projectning birinchi o'rindagi maqsadi xj-business.com saytida ro'yxatdan 
o'tilgan foydalanuvchilarga login paroli orqali kirib u yerda piramida 
shaklidagi foydalanuvchilarni boshqarish, finansoviy ma'lumotlarni ko'rish
va hokazo amallarni bajarib, odamlarga tovar reklamasi uchun qulayroq pul 
topish maqsadida sistema yaratiladi (keyingi o'rinlarda sistema deb 
ataymiz)


# 2. Sistemaning tuzilishi

Sistema quyidagi asosiy bloklardan tashkil topadi:

1. Registratsiya, autentifikatsiya va avtorizatsiya
2. Foydalanuvchilar daraxti
3. Dokumentlar
4. Moliyaviy jadval
5. Shaxsiy kabinet
6. Taklif etilganlar ro'yxati
7. Yangiliklar


## 2.1. Foydalanuvchi turlari

Sistemada ikki xildagi foydalanuvchi turlari ko'zda tutilgan bo'ladi. 
Birinchi turdagi foydalanuvchi administrator. Unga barcha foydalanuvchilarni 
ma'lumotlarini edit, delete, create funksiyalari va ma'lumotlarini ko'rish
va o'zgartirish imkoniyati mavjud bo'ladi


## 2.2. Registratsiya 

Sistemada registratsiyadan o'tish harkimga ham ochiq, sistemaga faqatgina
xj-business.com sayti orqali kimdirning taklifi orqaligina registratsiyadan
o'tish mumkin. Ya'ni partnyor id raqami (pozivnoyi) bo'lmasa registratsiya
qila olmaydi  

Hozirda saytda 3 qadam orqali quyidagi fieldlarni to'ldirib registratsiya 
qilish mumkin. 

1-qadam:
* Sponsor ID raqami - majburiy
* Ismi - majburiy
* Familyasi - majburiy
* Sharifi - majburiy

2-qadam:
* Elektron pochta manzili - majburiy
* Pasport seriya va raqami - majburiy
* Pasport kim tomonidan berilganligi - majburiy
* Shaxsning INNsi - majburiy

3-qadam:
* Telefon raqami - majburiy
* Parol - majburiy
* Takroriy parol - majburiy
* Shartnomani qabul qilganligi to'g'risida checkbox - majburiy

Saytda kiritilgan ma'lumotlar esa sistema bazasiga foydalanuvchi sifatida qo'shiladi.
Statusi esa unverified bo'lib turadi


## 2.3. Autentifikatsiya va avtorizatsiya

Saytda ro'yxatdan o'tilganidan keyin ko'rsatilgan emailga tasdiqlash linki yuboriladi.
Shu link orqali o'tganda sistemaga avtomatik ravishda kiradi. Statusi verified ga 
o'zgartiriladi

Avtorizatsiya quyidagi fieldlar orqali amalga oshiriladi:
* Login (tel raqami yoki emaili) - majburiy
* Boshida tanlagan paroli - majburiy

Shu bilan birga sbros parol qilish imkoniyati bo'lishi kerak, sbros qilinganda emailga 
xat keladi va shu xatdagi link orqali parolini sbros qilishi mumkin. Xat noreply@xj-business.com 
manzilidan kelishi kerak

Avtorizatsiyadan so'ng foydalanuvchi o'zining shaxsiy kabinetiga tushadi. Shaxsiy kabinetta
quyidagi keltirilgan funksiyalar joylashishi kerak:

1. Foydalanuvchilar daraxti
2. Dokumentlar
3. Moliyaviy jadval
4. Shaxsiy kabinet
5. Taklif etilganlar ro'yxati
6. Yangiliklar

## 2.4. Foydalanuvchilar daraxti

Foydalanuvchilar daraxti bu registratsiyada kimdirning tagidan kimdir yozilishi. 
https://telegra.ph/file/b3cd8c8b5e1d4c1c27d9a.jpg
