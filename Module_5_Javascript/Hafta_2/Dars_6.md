**Maqsad:** Bugun siz `while` sikllari, `for...of` sikllari va ichma-ich sikllar bilan chuqurroq tanishasiz. Bu sikllar turli xil vaziyatlarda kodni takrorlash uchun qo'llaniladi va ularni yaxshi tushunish sizga murakkabroq dasturlar yaratishda yordam beradi.

**Dars rejasi:**

1. **`while` sikli:**

    * `while` sikli berilgan shart rost bo'lgan ekan, kod blokini takrorlaydi. Bu shart har bir iteratsiyadan oldin tekshiriladi. Agar shart yolg'on bo'lsa, sikl to'xtaydi va undan keyingi kod bajariladi.

    ```javascript
    let i = 0;
    while (i < 5) {
      console.log(i);
      i++;
    }
    // Chiqish:
    // 0
    // 1
    // 2
    // 3
    // 4
    ```

    Bu kodda `while (i < 5)` sharti `i` o'zgaruvchisi 5 dan kichik bo'lgan ekan, rost bo'ladi. Sikl tanasida `console.log(i)` qatori `i` ning qiymatini konsolda chiqaradi va `i++` qatori `i` ni 1 ga oshiradi. `i` 5 ga teng bo'lganda, shart yolg'on bo'ladi va sikl to'xtaydi.

    * `while` siklini ishlatishdan oldin sikl o'zgaruvchisini e'lon qilish va unga boshlang'ich qiymat berish kerak. Aks holda, o'zgaruvchi aniqlanmagan bo'ladi va sikl ishlamaydi.
    * Sikl tanasida sikl o'zgaruvchisini o'zgartiradigan kod bo'lishi kerak, aks holda shart doim rost bo'lib qoladi va sikl cheksiz davom etadi. Bu "cheksiz sikl" deb ataladi va dasturning ishlashini to'xtatishi mumkin.

    * **`while` siklini amalda qo'llash misollari:**

        * Foydalanuvchi ma'lum bir qiymat kiritmaguncha takrorlanadigan kod bloki.
        * Fayl oxiriga yetguncha fayldan ma'lumotlarni o'qish.
        * O'yinlarda ma'lum bir shart bajarilmaguncha o'yin davom etishi.

2. **`for...of` sikli:**

    * `for...of` sikli massiv yoki matn kabi iteratsiya qilinadigan ob'ektlarning elementlari bo'ylab takrorlaydi. Bu sikl har bir element uchun kod blokini bajaradi.

    ```javascript
    let ranglar = ["qizil", "yashil", "ko'k"];

    for (let rang of ranglar) {
      console.log(rang);
    }
    // Chiqish:
    // "qizil"
    // "yashil"
    // "ko'k"
    ```

    Bu kodda `for...of` sikli `ranglar` massividagi har bir element uchun `console.log(rang)` qatorini bajaradi. `rang` o'zgaruvchisi har bir iteratsiyada massivning navbatdagi elementini oladi.

    * `for...of` sikli `for` sikliga qaraganda sodda va o'qish osonroq, chunki u indekslar bilan ishlashni talab qilmaydi.

    * **`for...of` siklini amalda qo'llash misollari:**

        * Massiv elementlarini konsolda chiqarish.
        * Massiv elementlarini qayta ishlash (masalan, har bir elementni 2 ga ko'paytirish).
        * Matnning har bir belgisini qayta ishlash.

3. **Ichma-ich sikllar:**

    * Ichma-ich sikllar bir sikl ichida boshqa siklni ishlatishni anglatadi. Bu murakkab masalalarni yechish uchun foydali bo'lishi mumkin. Misol uchun, ko'paytirish jadvalini yaratish uchun ichma-ich sikllardan foydalanish mumkin:

    ```javascript
    for (let i = 1; i <= 10; i++) {
      for (let j = 1; j <= 10; j++) {
        console.log(i + " x " + j + " = " + (i * j));
      }
      console.log(""); // Qatorlar orasida bo'sh qator qo'shish
    }
    ```

    Bu kodda tashqi `for` sikli 1 dan 10 gacha bo'lgan `i` qiymatlari uchun, ichki `for` sikli esa 1 dan 10 gacha bo'lgan `j` qiymatlari uchun takrorlanadi. Har bir iteratsiyada `i` va `j` ning ko'paytmasi konsolda chiqariladi.

    * Ichma-ich sikllarni ishlatishda tashqi siklning har bir iteratsiyasi uchun ichki sikl to'liq bajariladi.

    * **Ichma-ich sikllarni amalda qo'llash misollari:**

        * Ko'p o'lchamli massivlar bilan ishlash.
        * Naqshlar yaratish (masalan, yulduzcha naqshlari).
        * Jadvallar va matritsalar bilan ishlash.

**Qiyinchilik:**

* Yuqoridagi misoldan foydalanib, ko'paytirish jadvalini HTML jadvali sifatida web-sahifada chiqaruvchi dastur yarating. Bunda `document.write()` funksiyasidan foydalanishingiz mumkin.

**Eslatma:**

* `while` va `for...of` sikllari `for` sikliga alternativa hisoblanadi. Qaysi sikldan foydalanish kerakligi masala shartiga bog'liq.
* Ichma-ich sikllar murakkab masalalarni yechish uchun kuchli vosita bo'lishi mumkin, lekin ularni ishlatishda ehtiyot bo'lish kerak, chunki ular kodni murakkablashtirishi va dasturning ishlashini sekinlashtirishi mumkin.