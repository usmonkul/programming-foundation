**Modul 1.2: O'zgaruvchilar va ma'lumot turlari**

JavaScriptda dasturlashni o'rganishda o'zgaruvchilar va ma'lumot turlari bilan ishlash asoslarini tushunish juda muhim. Keling, ularni batafsil ko'rib chiqaylik.

**O'zgaruvchilar**

O'zgaruvchilar - bu ma'lumotlarni saqlash uchun ishlatiladigan "konteynerlar". Ularni nomlangan qutilarga o'xshatishingiz mumkin. Har bir qutiga (o'zgaruvchiga) nom beramiz va uning ichiga turli xil ma'lumotlarni joylashtirishimiz mumkin: matn, sonlar, mantiqiy qiymatlar va boshqalar.

**O'zgaruvchi e'lon qilish**

JavaScriptda o'zgaruvchi e'lon qilish uchun `var`, `let` yoki `const` kalit so'zlaridan foydalanamiz. 

* `var`: Eski usul. Hozirda kamroq ishlatiladi.
* `let`: Zamonaviy usul. O'zgaruvchining qiymatini keyinchalik o'zgartirish mumkin bo'lganda ishlatiladi.
* `const`: O'zgarmas o'zgaruvchilar uchun ishlatiladi. E'lon qilingandan so'ng qiymatini o'zgartirib bo'lmaydi.

**Misol:**

```javascript
let ism = "Anvar";  // "ism" o'zgaruvchisiga "Anvar" matnini saqladik
let yosh = 25;     // "yosh" o'zgaruvchisiga 25 sonini saqladik
const PI = 3.14159; // "PI" o'zgarmasiga 3.14159 sonini saqladik
```

**O'zgaruvchilarni to'g'ri nomlash**

O'zgaruvchilarga nom berishda quyidagi qoidalarga amal qilish kerak:

* Nomlar harf, raqam, pastki chiziq (`_`) yoki dollar belgisi (`$`) dan boshlanishi mumkin.
* Nomlar raqam bilan boshlanishi mumkin emas.
* Nomlarda bo'sh joylar bo'lmasligi kerak.
* JavaScript kalit so'zlarini (masalan, `var`, `let`, `if`, `else`) o'zgaruvchi nomi sifatida ishlatib bo'lmaydi.
* O'zgaruvchi nomi uning maqsadini aks ettirishi kerak. Masalan, `foydalanuvchiIsmi` o'zgaruvchisi foydalanuvchining ismini saqlash uchun ishlatiladi.

Yaxshi nomlash amaliyoti:

* `camelCase` uslubidan foydalaning (birinchi so'z kichik harf bilan, keyingi so'zlar bosh harf bilan boshlanadi). Masalan: `foydalanuvchiIsmi`, `mahsulotNarxi`.
* Nomlarni ingliz tilida yozing. Bu kodni boshqa dasturchilar uchun ham tushunarli qiladi.
* Qisqartmalardan foydalanmang. Masalan, `fn` o'rniga `firstName` deb yozing.

**Ma'lumot turlari**

JavaScriptda turli xil ma'lumot turlari mavjud. Eng asosiylari:

* **Matn (String):**  Matnlar qo'shtirnoq ichida yoziladi. Masalan: `"Salom"`, `"Bu matn"`, `"123"` (bu ham matn hisoblanadi, chunki qo'shtirnoq ichida).
* **Son (Number):** Butun yoki kasr sonlar. Masalan: `10`, `-5`, `3.14`.
* **Mantiqiy (Boolean):** Faqat ikkita qiymat qabul qilishi mumkin: `true` (rost) yoki `false` (yolg'on).

**O'zgaruvchilarga qiymat berish va ularni konsolga chiqarish**

O'zgaruvchilarga qiymat berish uchun `=` belgisidan foydalanamiz. Masalan:

```javascript
let shahar = "Toshkent";
```

O'zgaruvchining qiymatini konsolga chiqarish uchun `console.log()` funktsiyasidan foydalanamiz:

```javascript
console.log(shahar); // Konsolda "Toshkent" chiqadi
```

**Matn va o'zgaruvchilarni birlashtirish**

Matn va o'zgaruvchilarni birlashtirish uchun `+` belgisidan foydalanamiz:

```javascript
let ism = "Doston";
console.log("Mening ismim " + ism); // Konsolda "Mening ismim Doston" chiqadi
```

**Xulosa**

Ushbu bo'limda siz o'zgaruvchilar va ma'lumot turlari bilan ishlashni o'rgandingiz. To'g'ri nomlash qoidalariga amal qilish kodni o'qish va tushunishni osonlashtiradi. Bu bilimlar sizga keyingi darslarda murakkabroq dasturlar yozishda yordam beradi.
