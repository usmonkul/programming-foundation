## 1-hafta, 2-kun: Konsol bilan ishlash va shartli operatorlar

**Maqsad:** Bugun siz brauzer konsolida JavaScript kodini qanday ishlatishni, `console.log()` funksiyasi yordamida ma'lumotlarni chiqarishni va shartli operatorlar (`if`, `else if`, `else`) yordamida kod yozishni o'rganasiz.

**Dars rejasi:**

1. **Konsol bilan ishlash:**

    * Brauzer konsolini ochish: Ko'pgina brauzerlarda konsolni ochish uchun `F12` tugmasini bosish yoki sichqonchaning o'ng tugmasini bosib "Inspect" yoki "Tekshirish" ni tanlash kerak.
    * `console.log()` funksiyasi: Bu funksiya konsolda ma'lumotlarni chiqarish uchun ishlatiladi. O'zgaruvchilarning qiymatini, xabarlarni va boshqa ma'lumotlarni konsolda ko'rish uchun `console.log()` dan foydalanishingiz mumkin. Misollar:

    ```javascript
    console.log("Salom Dunyo!"); // "Salom Dunyo!" matnini chiqaradi
    let yosh = 15;
    console.log(yosh); // 15 sonini chiqaradi
    console.log("Mening yoshim:", yosh); // "Mening yoshim: 15" ni chiqaradi
    ```

    * Konsolda disk raskadrovka qilish: Konsol yordamida kodni disk raskadrovka qilish, ya'ni xatolarni topish va tuzatish mumkin. Konsolda o'zgaruvchilarning qiymatini tekshirish, kodning bajarilish jarayonini kuzatish va xatolar haqida ma'lumot olish mumkin.

2. **Shartli operatorlar:**

    * `if` operatori: Agar berilgan shart rost bo'lsa, kod blokini bajaradi. Misol:

    ```javascript
    let yosh = 18;
    if (yosh >= 18) {
      console.log("Siz kattalarsiz!");
    }
    ```

    Bu kodda, agar `yosh` o'zgaruvchisi 18 ga teng yoki katta bo'lsa, "Siz kattalarsiz!" xabari konsolda chiqadi.

    * `else` operatori: Agar `if` sharti yolg'on bo'lsa, `else` blok ichidagi kod bajariladi. Misol:

    ```javascript
    let yosh = 15;
    if (yosh >= 18) {
      console.log("Siz kattalarsiz!");
    } else {
      console.log("Siz hali voyaga yetmagansiz.");
    }
    ```

    Bu kodda, `yosh` 18 dan kichik bo'lgani uchun "Siz hali voyaga yetmagansiz." xabari chiqadi.

    * `else if` operatori: Bir nechta shartlarni tekshirish uchun ishlatiladi. Misol:

    ```javascript
    let baho = 75;
    if (baho >= 90) {
      console.log("A'lo!");
    } else if (baho >= 80) {
      console.log("Yaxshi!");
    } else if (baho >= 70) {
      console.log("Qoniqarli!");
    } else {
      console.log("Yomon!");
    }
    ```

    Bu kodda, `baho` o'zgaruvchisining qiymatiga qarab tegishli xabar konsolda chiqadi.

3. **Oddiy kirish va chiqish:**

    * `prompt()` funksiyasi: Foydalanuvchidan ma'lumot kiritishni so'rash uchun ishlatiladi. Misol:

    ```javascript
    let ism = prompt("Ismingizni kiriting:");
    console.log("Salom,", ism + "!");
    ```

    Bu kod foydalanuvchidan ismini so'raydi va "Salom, [ism]!" xabarini konsolda chiqaradi.

    * `alert()` funksiyasi: Foydalanuvchiga xabarnoma ko'rsatish uchun ishlatiladi. Misol:

    ```javascript
    alert("Xush kelibsiz!");
    ```

    Bu kod brauzerda "Xush kelibsiz!" xabarini ko'rsatadi.

**Mashqlar:**

1.  Foydalanuvchidan ikkita sonni so'rang va ularning yig'indisini konsolda chiqaring.
2.  Foydalanuvchidan yoshini so'rang va agar u 18 dan katta bo'lsa, "Siz saylovda qatnashishingiz mumkin" xabarini, aks holda "Siz saylovda qatnasha olmaysiz" xabarini chiqaring.
3.  Foydalanuvchidan baho sini so'rang va bahoga qarab "A'lo", "Yaxshi", "Qoniqarli" yoki "Yomon" xabarini chiqaring (baho shkalasi: 90-100 - A'lo, 80-89 - Yaxshi, 70-79 - Qoniqarli, 0-69 - Yomon).

**Eslatma:**  Kod bloklarida keltirilgan misollarni o'zingiz sinab ko'ring va turli xil qiymatlar bilan tajriba o'tkazing. Bu sizga kodni yaxshiroq tushunishga yordam beradi.
