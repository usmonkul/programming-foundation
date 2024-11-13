**Maqsad:** Bugun siz JavaScriptda Eventlar (events) bilan qanday ishlashni o'rganasiz. Eventlar - bu veb-sahifada sodir bo'ladigan harakatlar, masalan, sichqoncha bosish, klaviatura bosish, sahifa yuklanishi va hokazo. JavaScript yordamida siz bu Eventlarga javob berishingiz va veb-sahifalarni interaktiv qilishingiz mumkin.

**Dars rejasi:**

1. **Eventlar nima?**

    * Eventlar - bu veb-brauzerda yoki foydalanuvchi tomonidan sodir bo'ladigan harakatlar. Misol uchun, foydalanuvchi tugmani bosganda, sichqonchani harakatlantirganda, klaviaturada tugmani bosganda yoki sahifa yuklanganda Eventlar sodir bo'ladi.
    * JavaScript yordamida siz bu Eventlarni "tinglashingiz" va ularga javob berishingiz mumkin. Bu sizga veb-sahifalarni interaktiv qilish imkonini beradi. Misol uchun, tugmani bosganda boshqa elementni ko'rsatish, sichqoncha ustiga kelganda elementning rangini o'zgartirish yoki klaviaturada tugmani bosganda ma'lumotlarni kiritish mumkin.

2. **Eventlar turlari:**

    * Veb-dasturlashda juda ko'p turli xil Eventlar mavjud. Eng ko'p ishlatiladigan Eventlarga quyidagilar kiradi:
        * `click`: Element bosilganda sodir bo'ladi.
        * `mouseover`: Sichqoncha elementi ustiga kelganda sodir bo'ladi.
        * `mouseout`: Sichqoncha elementdan chiqib ketganda sodir bo'ladi.
        * `keydown`: Klaviaturada tugma bosilganda sodir bo'ladi.
        * `keyup`: Klaviaturada bosilgan tugma qo'yib yuborilganda sodir bo'ladi.
        * `load`: Sahifa to'liq yuklanganda sodir bo'ladi.

3. **Eventlarni tinglash:**

    * Eventlarni tinglash uchun `addEventListener()` metodidan foydalaniladi. Bu metod ikkita parametr qabul qiladi:
        * Hodisa nomi (masalan, `click`, `mouseover`).
        * Hodisa sodir bo'lganda bajariladigan funksiya.

    Misol:

    ```javascript
    let tugma = document.getElementById("meningTugmam");

    tugma.addEventListener("click", function() {
      alert("Tugma bosildi!");
    });
    ```

    Bu kodda `addEventListener()` metodi `meningTugmam` IDga ega tugma elementiga `click` hodisasini tinglashni qo'shadi. Tugma bosilganda, `alert("Tugma bosildi!")` kodi bajariladi va foydalanuvchiga xabarnoma ko'rsatiladi.

4. **Eventlar ob'ekti:**

    * Hodisa sodir bo'lganda, hodisa ob'ekti yaratiladi. Bu ob'ekt hodisa haqida ma'lumotni o'z ichiga oladi, masalan, hodisa qaysi elementda sodir bo'lganligi, sichqonchaning koordinatalari va hokazo.
    * Hodisa ob'ektiga funksiya ichida `event` parametri orqali kirish mumkin.

    Misol:

    ```javascript
    let kvadrat = document.getElementById("meningKvadratim");

    kvadrat.addEventListener("mouseover", function(event) {
      console.log("Sichqoncha koordinatalari: x = " + event.clientX + ", y = " + event.clientY);
    });
    ```

    Bu kodda `mouseover` hodisasi sodir bo'lganda, `event` ob'ekti yaratiladi va uning `clientX` va `clientY` xususiyatlari sichqonchaning koordinatalarini o'z ichiga oladi.

5. **Eventlarni bekor qilish:**

    * `preventDefault()` metodi hodisaning standart harakatini bekor qiladi. Misol uchun, havola bosilganda yangi sahifaga o'tishni bekor qilish uchun `preventDefault()` metodidan foydalanish mumkin.

    Misol:

    ```javascript
    let havola = document.getElementById("meningHavolam");

    havola.addEventListener("click", function(event) {
      event.preventDefault();
      alert("Havola bosildi, lekin yangi sahifaga o'tilmadi.");
    });
    ```

**Mini-loyiha:**

* Veb-sahifada ikkita tugma yarating. Birinchi tugmani bosganda, sahifaning fon rangi qizilga o'zgaradi. Ikkinchi tugmani bosganda, sahifaning fon rangi asl holatiga qaytadi.

**Mashqlar:**

1.  Veb-sahifada matn maydoni yarating. Foydalanuvchi matn kiritganda, kiritilgan matnni konsolda chiqaradigan dastur yarating.
2.  Veb-sahifada rasm yarating. Sichqoncha rasm ustiga kelganda, rasmning o'lchami kattalashadigan, sichqoncha rasmdan chiqib ketganda esa asl o'lchamiga qaytadigan dastur yarating.
3.  Veb-sahifada havola yarating. Havola bosilganda, yangi sahifaga o'tish o'rniga, foydalanuvchiga xabarnoma ko'rsatiladigan dastur yarating.

Ushbu darslik sizga Eventlar bilan ishlash asoslarini o'rganishga yordam beradi. Eventlar veb-sahifalarni interaktiv qilish uchun juda muhimdir, shuning uchun ularni yaxshi tushunish muhimdir. Agar yana savollar bo'lsa, bemalol so'rang!
