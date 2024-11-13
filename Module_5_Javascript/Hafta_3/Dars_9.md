**Maqsad:** Bugun siz DOM manipulyatsiyasi haqida bilimingizni chuqurlashtirasiz va JavaScript yordamida veb-sahifada dinamik ravishda yangi elementlar yaratishni va ularni DOMga qo'shishni o'rganasiz.

**Dars rejasi:**

1. **DOM manipulyatsiyasini eslatish:**

    * DOM (Document Object Model) veb-sahifaning tarkibini, strukturasini va uslubini ifodalovchi daraxtsimon model.
    * JavaScript yordamida DOM elementlarini tanlash, o'zgartirish va yangi elementlar qo'shish mumkin.

2. **Dinamik elementlar yaratish:**

    * `document.createElement()` metodi yangi element yaratadi. Misol:

    ```javascript
    let yangiParagraf = document.createElement("p");
    ```

    Bu kod yangi `<p>` elementini yaratadi va uni `yangiParagraf` o'zgaruvchisiga yuklaydi.

3. **Element tarkibini o'zgartirish:**

    * Yangi yaratilgan elementning tarkibini o'zgartirish uchun quyidagi xususiyatlardan foydalanish mumkin:
        * `textContent`: Elementning matnini o'zgartiradi.
        * `innerHTML`: Elementning HTML tarkibini o'zgartiradi.

    Misol:

    ```javascript
    yangiParagraf.textContent = "Bu yangi paragraf.";
    ```

4. **Elementga atributlar qo'shish:**

    * Elementga atributlar qo'shish uchun `setAttribute()` metodidan foydalanish mumkin.

    Misol:

    ```javascript
    yangiParagraf.setAttribute("class", "matn");
    ```

    Bu kod yangi paragrafga `class="matn"` atributini qo'shadi.

5. **Elementni DOMga qo'shish:**

    * Yangi yaratilgan elementni DOMga qo'shish uchun quyidagi metodlardan foydalanish mumkin:
        * `appendChild()`: Elementni ota elementning oxiriga qo'shadi.
        * `insertBefore()`: Elementni ota elementning ma'lum bir bolasi oldidan qo'shadi.

    Misol:

    ```javascript
    document.body.appendChild(yangiParagraf);
    ```

    Bu kod yangi paragrafni `<body>` elementining oxiriga qo'shadi.

6. **Dinamik ro'yxat yaratish:**

    * Dinamik ravishda ro'yxat yaratish uchun `for` sikli va yuqoridagi metodlardan foydalanish mumkin. Misol:

    ```javascript
    let mevalar = ["Olma", "Anor", "Uzum"];

    let ro'yxat = document.createElement("ul");

    for (let meva of mevalar) {
      let element = document.createElement("li");
      element.textContent = meva;
      ro'yxat.appendChild(element);
    }

    document.body.appendChild(ro'yxat);
    ```

    Bu kod `mevalar` massividagi har bir meva uchun yangi `<li>` elementi yaratadi va uni `<ul>` elementiga qo'shadi. So'ngra, `<ul>` elementi `<body>` elementiga qo'shiladi.

**Mini-loyiha:**

* Veb-sahifada tugma va matn maydoni yarating. Tugmani bosganda, matn maydonidagi qiymatni o'qib, yangi paragraf yarating va uni sahifaga qo'shing.

**Mashqlar:**

1.  Veb-sahifada tugma yarating. Tugmani bosganda, tasodifiy rangdagi kvadrat yarating va uni sahifaga qo'shing.
2.  Veb-sahifada matn maydoni va tugma yarating. Tugmani bosganda, matn maydonidagi qiymatni o'qing va uni sahifadagi sarlavhaga qo'shing.
3.  Veb-sahifada tugma yarating. Tugmani bosganda, 1 dan 10 gacha bo'lgan sonlar ro'yxatini yarating va uni sahifaga qo'shing.