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
