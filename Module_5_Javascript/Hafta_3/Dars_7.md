**Maqsad:** Bugun siz DOM (Document Object Model) bilan tanishasiz va JavaScript yordamida veb-sahifalarni qanday qilib dinamik ravishda o'zgartirishni o'rganasiz.

**Dars rejasi:**

1. **DOM nima?**

    * DOM - bu veb-sahifaning tarkibini, strukturasini va uslubini ifodalovchi daraxtsimon model. U HTML hujjatni ob'ektlar daraxti sifatida tasvirlaydi, bu yerda har bir element, atribut va matn alohida ob'ekt hisoblanadi.
    * DOM veb-sahifani JavaScript orqali boshqarish imkonini beradi. Siz DOM orqali elementlarni qo'shishingiz, o'chirishingiz, o'zgartirishingiz va ularga turli xil Eventlarni (masalan, sichqoncha bosish, klaviatura bosish) bog'lashingiz mumkin.
    * DOM veb-dasturlashning asosiy qismlaridan biri hisoblanadi va interaktiv veb-sahifalar yaratish uchun juda muhimdir.

2. **DOM daraxti:**

    * DOM daraxti veb-sahifaning elementlarini ierarxik tarzda ifodalaydi. Eng yuqori element `window` ob'ekti hisoblanadi. Undan keyin `document` ob'ekti keladi, u HTML hujjatni ifodalaydi. `document` ob'ekti ichida `html` elementi, uning ichida esa `head` va `body` elementlari va hokazo joylashadi.
    * Har bir element o'zining ota elementiga (parent) va bolalar elementlariga (children) ega.
    * DOM daraxti orqali siz elementlar o'rtasidagi munosabatlarni bilib olishingiz va ularni boshqarishingiz mumkin.

3. **DOM elementlarini tanlash:**

    * JavaScriptda DOM elementlarini tanlash uchun quyidagi metodlardan foydalanish mumkin:
        * `getElementById()`: Berilgan IDga ega elementni tanlaydi.
        * `getElementsByTagName()`: Berilgan teg nomiga ega barcha elementlarni tanlaydi va ularni HTMLCollection ob'ekti sifatida qaytaradi.
        * `getElementsByClassName()`: Berilgan klass nomiga ega barcha elementlarni tanlaydi va ularni HTMLCollection ob'ekti sifatida qaytaradi.
        * `querySelector()`: Berilgan CSS selektoriga mos keladigan birinchi elementni tanlaydi.
        * `querySelectorAll()`: Berilgan CSS selektoriga mos keladigan barcha elementlarni tanlaydi va ularni NodeList ob'ekti sifatida qaytaradi.

    Misol:

    ```html
    <!DOCTYPE html>
    <html>
    <head>
      <title>DOM misol</title>
    </head>
    <body>
      <h1 id="sarlavha">Salom Dunyo!</h1>
      <p class="matn">Bu birinchi paragraf.</p>
      <p class="matn">Bu ikkinchi paragraf.</p>

      <script>
        let sarlavha = document.getElementById("sarlavha");
        console.log(sarlavha.textContent); // "Salom Dunyo!" ni chiqaradi

        let paragraflar = document.getElementsByClassName("matn");
        console.log(paragraflar[0].textContent); // "Bu birinchi paragraf." ni chiqaradi

        let birinchiParagraf = document.querySelector("p");
        console.log(birinchiParagraf.textContent); // "Bu birinchi paragraf." ni chiqaradi
      </script>
    </body>
    </html>
    ```

4. **DOM elementlarini o'zgartirish:**

    * DOM elementlarining xususiyatlarini o'zgartirish mumkin. Misol uchun, elementning matnini o'zgartirish uchun `textContent` xususiyatidan foydalanish mumkin:

    ```javascript
    sarlavha.textContent = "Yangi sarlavha";
    ```

    * Elementning HTML tarkibini o'zgartirish uchun `innerHTML` xususiyatidan foydalanish mumkin:

    ```javascript
    birinchiParagraf.innerHTML = "<b>Yangi matn</b>";
    ```

    * Elementning uslubini o'zgartirish uchun `style` xususiyatidan foydalanish mumkin:

    ```javascript
    birinchiParagraf.style.color = "red";
    ```

    * Elementga yangi atribut qo'shish yoki mavjud atributni o'zgartirish uchun `setAttribute()` metodidan foydalanish mumkin:

    ```javascript
    birinchiParagraf.setAttribute("title", "Yangi atribut");
    ```

5. **DOMga yangi elementlar qo'shish:**

    * `createElement()` metodi yangi element yaratadi.
    * `appendChild()` metodi yangi elementni mavjud elementga bolalar elementi sifatida qo'shadi.

    Misol:

    ```javascript
    let yangiParagraf = document.createElement("p");
    yangiParagraf.textContent = "Bu yangi paragraf.";
    document.body.appendChild(yangiParagraf);
    ```

**Mini-loyiha:**

* Veb-sahifada tugma yarating. Tugmani bosganda, sahifaning fon rangi o'zgaradigan dastur yarating.

**Mashqlar:**

1.  Veb-sahifada ro'yxat yarating va unga JavaScript yordamida yangi elementlar qo'shing.
2.  Veb-sahifada rasm yarating va sichqoncha ustiga kelganda rasm o'zgaradigan dastur yarating.
3.  Veb-sahifada matn maydoni yarating va foydalanuvchi matn kiritganda, matnni katta harflar bilan konsolda chiqaradigan dastur yarating.