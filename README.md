# 1. Project maqsadi 

Projectning birinchi o'rindagi maqsadi xj-business.com saytida ro'yxatdan 
o'tilgan foydalanuvchilarga login paroli orqali kirib u yerda foydalanuvchilarni 
boshqarish, finansoviy ma'lumotlarni ko'rish
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

Aktivatsiya jarayoni to'lov qilinishi bilan belgilanadi. To'lov qilmaganlar pending bo'lib turaveradi.

Avtorizatsiya quyidagi fieldlar orqali amalga oshiriladi:
* Login (id beriladi) - majburiy
* Boshida tanlagan paroli - majburiy

### 2.3.1. Sbros parol

Shu bilan birga sbros parol qilish imkoniyati bo'lishi kerak, sbros qilinayoganda emailga 
xat keladi va shu xatdagi link orqali parolini sbros qilishi mumkin. Xat noreply@xj-business.com 
manzilidan kelishi kerak. Xatni example: https://nago.laborasyon.com/demos/layouts/default/mailing.html

### 2.3.2. Logindan keyin qilinadigan ishlar

Keyinchalik popup funksiyasidan foydalangan holda kirgandan yangiliklarni taqdim etiladigan qilsak bo'ladi

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

1. Foydalanuvchilar darajasi
2. Chap va o'ng qanotlar
3. Yangi foydalanuvchini joylashtirish funksiyasi
4. Har bir foydalanuvchini ma'lumotlarini ko'rish funksiyasi
5. Daromad hisoblash logikasi

Dizayni bo'yicha biriktirilgan rasmdagidek shaklda, iloji boricha qulayroq qilinishi kerak. 
Pasdagi strelkani bossa pasga qarab ketaverishi kerak, ya'ni pasga va tepaga chiqishlarni
yaxshilab qarab chiqilishi kerak. 2.4.1. punktda keltirilgan znachoklar tegishli tartibda ko'rinib 
turishi lozim bo'ladi.

To'lov qilgandan so'ng 12 hafta aktiv bo'lib turadi, aks holda pending holatiga o'tkaziladi. Pending foydalanuvchilarga 12 hafta vaqt beriladi aktiv bo'lishi uchun.
Agar berilgan vaqt ichida to'lov qilmasa ban statusiga o'tkaziladi va yaroqsiz akkaunt deb ataladi. 

Foydalanuvchilar daraxtida hech kimni joyi o'chib ketmaydi. Lekin uni joyidan qayta foydalanib bo'lmaydi, ya'ni, boshqa foydalanuvchini biriktirib bo'lmaydi.
Uslovniy 12 hafta berilgan muddatdan keyin kelib yana aktivlashtirish uchun foydalanuvchiga jarima solinadi qanchadir miqdorda.

### 2.4.1. Foydalanuvchilar darajasi

https://telegra.ph/file/8e49691db8d4fdc7fee1d.jpg

Shu yerda ko'rsatilganday, har xil turdagi foydalanuvchilar darajalari bo'lishi mumkin. Deylik bu "silver" shartlari https://telegra.ph/file/bce118ccec8b584c6fb49.jpg
Shunga o'xshash har bir darajaning o'zini algoritmlari bo'ladi, ya'ni qaysidir darajaga yetganda znachok almashadi va level ham shunga yarasha almashadi. Har bir levelga 
yetganda qandaydir sovg'alar olish imkoniyatlari bor.

Quyida keltirilganlar darajalar va u darajaga yetish shartlari keltirilgan (batafsil videoni 4:20dan boshlab aytilgan va ko'rsatilgan):

* Представитель менеджер команды лидеров - 15 - дополнительный аккаунт или 95$
* Представитель Бронзовой команды лидеров - 50 - андроид смартфон
* Представитель Серебряной команды лидеров - 150 - Apple смартфон
* Представитель Золотой команды лидеров - 300 - Путевка на каникулы с лидерами
* Представитель Платиновой команды лидеров - 500 - Путевка на каникулы семейные с лидерами
* Представитель Рубиновой команды лидеров - 1500 - Автомобиль «Spark» или 8 000 y.e.
* Представитель Изумрудной команды лидеров - 3000 - Автомобиль «Hyundai Creta» или 15 000 y.e.
* Представитель Бриллиантовой команды лидеров - 5000 - Квартира или 50 000 y.e.

Yuqorida keltirilganlarni qisqacha ta'rifi: "Unvonning nomi" - "4 hafta aktiv bo'lganlar soni" - "Katta bonus"

> **To'lov haqida:** Foydalanuvchilar aktiv va noaktiv foydalanuvchilarga bo'linadi. Aktiv foydalanuvchilar 4 hafta ichida narsa sotib olganlar hisoblanadi. Agar 4 hafta ichida hech qanday narsa sotib olmasa, unda u avtomatik tarzda 4-haftaning yakshanba kuni soat 19:59 da aktiv holatdan noaktiv holatiga o'tkaziladi.


### 2.4.2. Chap va o'ng qanotlar

Sistemada chap va o'ng tarmoqlar degan tushunchalar ko'p ishlatilinadi. Bu nega kerak? Kam tarmoqda odam ko'paygani uchungina bonus pullari yoziladi. Bu 2.4.5. punktda batafsil keltirilgan.
Qisqasi: kam tarmoqda foydalanuvchi qo'shilgani uchun bonus yozilsa chap va o'ng tarmoqlar hardoyim deyarli baravar yuradi. Shu maqsadda qilingan.


### 2.4.3. Yangi foydalanuvchini joylashtirish funksiyasi

https://telegra.ph/file/a4e44047ea5cfc4548efb.jpg ushbu rasmda ko'rsatilganiday bo'sh qanotlarga yangi qo'shilgan child foydalanuvchilarni biriktirish imkoniyati bor.
Har bir qo'shilganfoydalanuvchi kimningdir child foydalanuvchisi bo'lib ro'yxatdan o'tadi. Childning parenti yoki grandparenti ham sistemada uni chap yoki o'ng qanotiga joylashtirish
imkoni bor (batafsil videoda 32:30 minutida). Joylashtirmagunicha u child foydalanuvchi pending bo'lib turadi. Agar pending child lar bo'lmasa ushbu ko'rinishdagiday narsa chiqib turadi: https://telegra.ph/file/64c63faaf669da6770d72.jpg 

Foydalanuvchi daraxtiga yangi foydalanuvchi qo'shish soat 20:00 gacha olib boriladi. Agar yakshanba kuni soat 20:00 gacha foydalanuvchini joylashtirishga ulgurmasa 2.4.5. punktdagi daromad qo'shilmaydi. va keyingi hafta uchungina qo'shiladi.

### 2.4.4. Har bir foydalanuvchini ma'lumotlarini ko'rish funksiyasi

Har bir foydalanuvchini ustiga bir martta bosilsa uni ma'lumotlari popup ko'rinishida chiqib kelishi kerak. 
example: https://telegra.ph/file/d5b440f3b189013447d8f.jpg


### 2.4.5. Daromad hisoblash logikasi

Kam tarmog'ida (2.4.2. punktda keltirilgan) joriy xaftada nechta foydalanuvchi 
qo'shilgan bo'lsa shuni 3$ ga ko'paytirib uni balansiga qo'shib qo'yaverilishi kerak. 
Bu amal har yakshanba kuni soat 20:00 da amalga oshiriladi. Keyingi haftada esa yana 
huddi shunday, faqat kelgusi haftada qo'shiluvchi foydalanuvchilar uchungina hisoblanadi. 
Bonus faqat bir marotaba beriladi. Chizma: https://telegra.ph/file/39ce00b8c314588078611.jpg

## 2.5. Dokumentlar

Dokumentlar bo'limida hech qanday amal bajarilmaydi, faqatgina ma'lumot olish manbai bo'lib xizmat qila oladi.

### 2.5.1. Darajalar bo'yicha ma'lumotnoma

8 turdagi darajalarni har biri bo'yicha alohida ma'lumot berilgan bo'ladi. Bu ma'lumotlar jadval ko'rinishida saqlanadi va u kamdan kam o'zgartiriladi.
Agar mumkin bo'lsa o'zgartirish funksiyasi qilinadi. 2.4.1 punktda keltirilgan ma'lumotlardan olinadi.

### 2.5.2. Polojeniye

Dokumentatsiya ko'rinishidagi terminlar va kerakli informatsiyalar jamlangan text ko'rinishidagi ma'lumot.
Agar mumkin bo'lsa o'zgartirish funksiyasi qilinadi. https://telegra.ph/file/dd249a26ef078aab21fba.jpg

### 2.5.3. User turlari bo'yicha ma'lumotnoma.

Icon yoniga text ko'rinishida qilib ketilaveradi. Ma'lumotlar 2.4.1. punktdan olinadi. Example: https://telegra.ph/file/8e49691db8d4fdc7fee1d.jpg


## 2.6. Moliyaviy jadval

Molivayiv jadvalga o'tish knopkasini saytni tepa qismiga alohida button qilib qo'shsa ham bo'ladi.
Popup chiqib ushbu ma'lumotlar keltirilishi kerak bo'ladi:

* Joriy sof daromad "Kam qanotdagi (chap yoki o'ng) aktiv child userlar soni" x "Bonus summasi: har bir foydalanuvchi uchun birxil" = "Joriy sof daromad"
* Kam qanotdagi (chap yoki o'ng) aktiv child userlar soni
* Bonus summasi: har bir foydalanuvchi uchun birxil
* Qachongacha aktivligi: sanasi va vaqti
* Katta bonus uchun hisoblanadigan 

## 2.7. Shaxsiy kabinet

Tab ko'rinishida bo'ladi. Quyidagi keltirilgan 3 ta tabdan iborat bo'ladi:

* Sistemadagi ma'limotlar
* Rekvizitlar
* Shaxsiy ma'lumotlar

### 2.7.1. Sistemadagi ma'lumotlar

https://telegra.ph/file/4ed1890c61ddc52e7e1f4.jpg Bazadan quyidagi ma'lumotlarni olib berishi kerak bo'ladi:

* Sponsor ID raqami (ya'ni parent user)
* FISh sponsorniki
* ID raqam (child userniki)
* Familya
* Ism
* Otchestvo
* Email
* Telefon raqam
* Yangi parol
* Yangi parolni takrorlash (save qilinganidan keyin parolni yangilab qo'yadi)

### 2.7.2. Rekvizitlar

https://telegra.ph/file/1fd3f4b8e15e75e45db7b.jpg Bazadan quyidagi ma'lumotlarni olib berishi kerak bo'ladi:

* Karta raqami
* Karta egasining ism familyasi

### 2.7.3. Shaxsiy ma'lumotlar

https://telegra.ph/file/b3ef86be40e0246fee60d.jpg Bazadan quyidagi ma'lumotlarni olib berishi kerak bo'ladi va o'zgartirish imkoni ham bo'lishi kerak:

* Tug'ilgan yili oyi kuni (datepicker foydalaniladi va limit qo'yiladi 18 yoshdan kattalar tanlanishi uchun)
* Shaxar
* Tug'ilgan joyi
* Pasport seriya va raqami - majburiy
* Pasport kim tomonidan berilganligi - majburiy
* Shaxsning INNsi - majburiy

## 2.8. Shaxsan taklif etilganlar ro'y'xati

Jadval ko'rinishida berilgan bo'ladi. Quyida ko'rsatilgan taritbda beriladi:

* Tartib raqami
* Login (ya'ni childning ID raqami)
* FISh
* Qachon ro'yxatdan o'tganligi
* Oxirgi martaa aktivatsiya qilgan sanasi
* Unvoni (eg Bronza, Silver)
* Telefon raqami
* Emaili
