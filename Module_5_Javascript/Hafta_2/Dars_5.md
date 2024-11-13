**Dars rejasi:**

1. **Ob'ektlar nima?**

    * Ob'ekt - bu xususiyatlar (properties) va metodlar (methods) to'plami. Xususiyatlar ob'ektning xususiyatlarini (masalan, rangi, o'lchami, nomi), metodlar esa ob'ekt ustida bajariladigan amallarni (masalan, yurish, gapirish, hisoblash) ifodalaydi.
    * Ob'ektlar real dunyo ob'ektlarini modellashtirish uchun ishlatiladi. Misol uchun, "mashina" ob'ekti rangi, modeli, yili kabi xususiyatlarga va yurish, to'xtash, signal chalish kabi metodlarga ega bo'lishi mumkin.
    * Ob'ektlar ma'lumotlarni tashkil qilish uchun ham ishlatiladi. Misol uchun, "talaba" ob'ekti ismi, familiyasi, yoshi, bahosi kabi xususiyatlarga ega bo'lishi mumkin.

2. **Ob'ektlarni yaratish:**

    * Ob'ektlar figurali qavslar (`{}`) ichida kalit-qiymat juftliklari sifatida yaratiladi. Kalitlar xususiyat nomlarini, qiymatlar esa xususiyatlarning qiymatlarini ifodalaydi. Misol:

    ```javascript
    let talaba = {
      ism: "Ali",
      familiya: "Valiyev",
      yosh: 15,
      baho: 4
    };
    ```

    Bu kodda `talaba` ob'ekti to'rtta xususiyatga ega: `ism`, `familiya`, `yosh` va `baho`.

3. **Ob'ekt xususiyatlariga kirish:**

    * Ob'ekt xususiyatlariga kirish uchun nuqta (`.`) yoki kvadrat qavslar (`[]`) dan foydalanish mumkin. Misol:

    ```javascript
    console.log(talaba.ism); // "Ali" ni chiqaradi
    console.log(talaba["familiya"]); // "Valiyev" ni chiqaradi
    ```

4. **Ob'ekt xususiyatlarini o'zgartirish:**

    * Ob'ekt xususiyatlarini o'zgartirish mumkin. Misol:

    ```javascript
    talaba.baho = 5;
    console.log(talaba.baho); // 5 ni chiqaradi
    ```

5. **Ob'ektlarga yangi xususiyatlar qo'shish:**

    * Ob'ektlarga yangi xususiyatlar qo'shish mumkin. Misol:

    ```javascript
    talaba.sinf = "9A";
    console.log(talaba.sinf); // "9A" ni chiqaradi
    ```

6. **Ob'ekt metodlari:**

    * Metodlar ob'ekt bilan bog'liq funksiyalardir. Ular ob'ekt ustida amallar bajarish uchun ishlatiladi. Misol:

    ```javascript
    let talaba = {
      ism: "Ali",
      familiya: "Valiyev",
      salomlash: function() {
        console.log("Salom, mening ismim " + this.ism + "!");
      }
    };

    talaba.salomlash(); // "Salom, mening ismim Ali!" ni chiqaradi
    ```

    Bu kodda `salomlash()` metodi `talaba` ob'ekti bilan bog'liq. Metod ichida `this` kalit so'zi ob'ektning o'ziga ishora qiladi.

7. **`this` kalit so'zi:**

    * `this` kalit so'zi ob'ektning o'ziga ishora qiladi. U ob'ekt metodlari ichida ob'ekt xususiyatlariga kirish uchun ishlatiladi.

8. **Ob'ektlar bilan sikllar:**

    * `for...in` sikli yordamida ob'ekt xususiyatlari bo'ylab takrorlash mumkin. Misol:

    ```javascript
    for (let kalit in talaba) {
      console.log(kalit + ": " + talaba[kalit]);
    }
    // Chiqish:
    // "ism: Ali"
    // "familiya: Valiyev"
    // "salomlash: function() { ... }"
    ```

**Mini-loyiha:**

* "Kitob" ob'ekti yarating. Kitobning nomi, muallifi, nashr yili kabi xususiyatlarni qo'shing. Kitob haqida ma'lumotni konsolda chiqaruvchi metod yarating.

**Mashqlar:**

1.  "Mashina" ob'ekti yarating. Mashinaning rangi, modeli, yili kabi xususiyatlarni qo'shing.
2.  Berilgan ob'ektning barcha xususiyatlarini konsolda chiqaruvchi funksiya yarating.
3.  Ikki ta "Talaba" ob'ekti yarating va ularning baho
 larini taqqoslovchi funksiya yarating.



 ## 2-hafta, 6-kun: JSON bilan ishlash

**Maqsad:** Bugun siz JSON (JavaScript Object Notation) haqida bilib olasiz va JavaScriptda JSON ma'lumotlari bilan qanday ishlashni o'rganasiz.

**Dars rejasi:**

1. **JSON nima?**

    * JSON - bu ma'lumotlarni almashish uchun ishlatiladigan matn asosidagi format. U odamlar va kompyuterlar uchun oson o'qiladigan va yoziladigan formatda ma'lumotlarni ifodalaydi.
    * JSON JavaScript sintaksisiga asoslangan, lekin u dasturlash tilidan mustaqil format. Ya'ni, JSON ma'lumotlarini JavaScriptdan tashqari boshqa dasturlash tillarida ham ishlatish mumkin.
    * JSON veb-dasturlashda keng qo'llaniladi, chunki u server va klient o'rtasida ma'lumotlarni almashish uchun qulay formatdir.

2. **JSON strukturasi:**

    * JSON ma'lumotlari kalit-qiymat juftliklari to'plami sifatida ifodalanadi. Kalitlar qo'shtirnoq ichida yozilgan matnlar, qiymatlar esa quyidagi ma'lumot turlaridan biri bo'lishi mumkin:
        * Matn (String)
        * Son (Number)
        * Mantiqiy qiymat (Boolean: `true` yoki `false`)
        * Massiv (Array)
        * Ob'ekt (Object)
        * `null`

    Misol:

    ```json
    {
      "ism": "Ali",
      "familiya": "Valiyev",
      "yosh": 15,
      "baho": [4, 5, 4],
      "manzil": {
        "shahar": "Samarqand",
        "ko'cha": "Ulug'bek"
      }
    }
    ```

3. **JSONni JavaScript ob'ektiga aylantirish:**

    * `JSON.parse()` metodi JSON matnini JavaScript ob'ektiga aylantiradi. Misol:

    ```javascript
    let jsonMatn = '{ "ism": "Ali", "familiya": "Valiyev" }';
    let obyekt = JSON.parse(jsonMatn);

    console.log(ob'ekt.ism); // "Ali" ni chiqaradi
    ```

4. **JavaScript ob'ektini JSONga aylantirish:**

    * `JSON.stringify()` metodi JavaScript ob'ektini JSON matniga aylantiradi. Misol:

    ```javascript
    let obyekt = { ism: "Ali", familiya: "Valiyev" };
    let jsonMatn = JSON.stringify(obyekt);

    console.log(jsonMatn); // '{ "ism": "Ali", "familiya": "Valiyev" }' ni chiqaradi
    ```

5. **JSONni qo'llash:**

    * JSON veb-dasturlashda server va klient o'rtasida ma'lumotlarni almashish uchun keng qo'llaniladi.
    * JSON ma'lumotlar bazalarida ma'lumotlarni saqlash uchun ham ishlatilishi mumkin.
    * JSON konfiguratsiya fayllarida sozlamalarni saqlash uchun ham qulay formatdir.

**Mini-loyiha:**

* JSON formatida saqlangan talaba ma'lumotlarini o'qing va konsolda talabaning ismi, familiyasi va baholarini chiqaring.

**Mashqlar:**

1.  JSON formatida saqlangan kitob ma'lumotlarini JavaScript ob'ektiga aylantiring.
2.  JavaScript ob'ektini JSON formatida matnga aylantiring va konsolda chiqaring.
3.  JSON formatida saqlangan mahsulotlar ro'yxatini o'qing va har bir mahsulotning nomini va narxini konsolda chiqaring.

