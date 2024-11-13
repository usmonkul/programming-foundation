**Maqsad:** Bugun siz JavaScript dasturlash tili bilan tanishasiz, asosiy ma'lumot turlarini o'rganasiz va o'zgaruvchilarni nomlash qoidalarini bilib olasiz.

**Dars rejasi:**

1.  **JavaScript nima?**

    * JavaScript - bu web-sahifalarga interaktivlik qo'shish uchun ishlatiladigan dasturlash tili. U orqali siz tugmalarni bosish, animatsiyalar yaratish, ma'lumotlarni yuborish va qabul qilish kabi ko'plab amallarni bajarishingiz mumkin. Misol uchun, veb-saytlarda ko'rgan slayderlar, pop-up oynalar, forma validatsiyalari va boshqa dinamik elementlar JavaScript yordamida yaratiladi.
    * JavaScript frontend (foydalanuvchi ko'radigan qism) va backend (server tomoni) dasturlashda keng qo'llaniladi. Frontendda u HTML va CSS bilan birgalikda ishlaydi, backendda esa Node.js platformasi orqali server dasturlarini yaratishda foydalaniladi.
    * JavaScript dunyodagi eng mashhur dasturlash tillaridan biri hisoblanadi.  Stack Overflow kabi platformalarda o'tkazilgan so'rovnomalarga ko'ra, JavaScript dasturchilar orasida eng ko'p ishlatiladigan til hisoblanadi.

2.  **Rivojlanish muhitini sozlash:**

    * **Kod muharriri:** Kod yozish uchun sizga kod muharriri kerak bo'ladi. Visual Studio Code, Sublime Text, Atom kabi bepul muharrirlarni ishlatishingiz mumkin. Bu muharrirlar sintaksisni ajratib ko'rsatish, kodni avtomatik to'ldirish, xatolarni topish kabi funksiyalarni taklif qiladi va kod yozish jarayonini osonlashtiradi.
    * **Web-brauzer:** Kodni ishga tushirish va natijalarni ko'rish uchun web-brauzer (Chrome, Firefox, Edge) kerak. Brauzerning konsolida (Developer Tools) kodni tekshirish va xatolarni topish mumkin. Konsol - bu brauzerda JavaScript kodini ishga tushirish, natijalarni ko'rish va xatolarni disk raskadrovka qilish uchun ishlatiladigan vositadir.
    * **Onlayn kodlash platformalari:** Agar dasturlarni o'rnatishni xohlamasangiz, CodePen, Repl.it kabi onlayn platformalarda kod yozishingiz mumkin. Bu platformalar kod muharriri va brauzerni birlashtiradi va kodni tezkor ravishda yozish va sinab ko'rish imkonini beradi.

3.  **Asosiy sintaksis:**

    * **O'zgaruvchilar:** Ma'lumotlarni saqlash uchun o'zgaruvchilardan foydalanamiz. O'zgaruvchilar `let`, `const` kalit so'zlari bilan e'lon qilinadi. `let` bilan e'lon qilingan o'zgaruvchining qiymatini keyinchalik o'zgartirish mumkin, `const` bilan e'lon qilingan o'zgaruvchining qiymatini esa o'zgartirib bo'lmaydi.

    ```javascript
    let yosh = 15; 
    console.log(yosh); // 15 ni chiqaradi

    yosh = 16; 
    console.log(yosh); // 16 ni chiqaradi

    const ism = "Ali"; 
    console.log(ism); // "Ali" ni chiqaradi

    ism = "Vali"; // Xatolik beradi, chunki const o'zgaruvchining qiymatini o'zgartirib bo'lmaydi.
    ```

    * **Ma'lumot turlari:**
        * **Sonlar (Number):**  10, 3.14, -5 kabi sonlarni ifodalaydi.  Misollar:

        ```javascript
        let yosh = 20;
        let narx = 9.99;
        let temperatura = -10;
        ```

        * **Matnlar (String):** "Salom", 'Dunyo' kabi matnlarni ifodalaydi. Qo'shtirnoq yoki birtirnoq ichida yoziladi. Misollar:

        ```javascript
        let ism = "Ali";
        let familiya = 'Valiyev';
        let xabar = "Assalomu alaykum!";
        ```

        * **Mantiqiy qiymatlar (Boolean):** `true` (rost) yoki `false` (yolg'on) qiymatlarini oladi. Misollar:

        ```javascript
        let kattalar = true;
        let togriJavob = false;
        let aktiv = true;
        ```

    * **Operatorlar:**
        * **Arifmetik operatorlar:** `+`, `-`, `*`, `/`, `%` (qoldiq) kabi matematik amallarni bajarish uchun ishlatiladi. Misollar:

        ```javascript
        let a = 10;
        let b = 5;
        let summa = a + b; // 15
        let ayirma = a - b; // 5
        let kopaytma = a * b; // 50
        let bolinma = a / b; // 2
        let qoldiq = a % b; // 0
        ```

        * **Tenglashtirish operatori:** `=` o'zgaruvchiga qiymat berish uchun ishlatiladi. Misollar:

        ```javascript
        let yosh = 20;
        let ism = "Ali";
        ```

        * **Taqqoslash operatorlari:** `==` (teng), `!=` (teng emas), `>` (katta), `<` (kichik), `>=` (katta yoki teng), `<=` (kichik yoki teng) kabi taqqoslashlarni amalga oshirish uchun ishlatiladi. Misollar:

        ```javascript
        let a = 10;
        let b = 5;

        console.log(a == b); // false
        console.log(a != b); // true
        console.log(a > b);  // true
        console.log(a < b);  // false
        console.log(a >= b); // true
        console.log(a <= b); // false
        ```

4.  **O'zgaruvchilarni nomlash qoidalari:**

    * O'zgaruvchi nomi harf, raqam yoki pastki chiziq (`_`) bilan boshlanishi mumkin. Misollar: `ism`, `yosh1`, `_maxfiy`.
    * O'zgaruvchi nomida bo'sh joy bo'lmasligi kerak.  Agar bir nechta so'zdan iborat nom kerak bo'lsa, `camelCase` (masalan, `meningIsmim`) yoki `snake_case` (masalan, `mening_ismim`) uslublaridan foydalaning.
    * JavaScriptda katta-kichik harflar farqlanadi (`ism` va `Ism` ikki xil o'zgaruvchi). Shuning uchun o'zgaruvchilarni nomlashda katta-kichik harflarga e'tibor bering.
    * O'zgaruvchilarga mazmunli nomlar berish tavsiya etiladi (masalan, `yosh` o'rniga `studentYoshi`). Bu kodni o'qish va tushunishni osonlashtiradi.

5.  **Birinchi JavaScript dasturi:**

    * Konsolda "Salom Dunyo\!" yozuvini chiqarish:

    ```javascript
    console.log("Salom Dunyo!"); 
    ```

    Bu kod brauzer konsolida "Salom Dunyo!" yozuvini chiqaradi. `console.log()` funksiyasi JavaScriptda ma'lumotlarni