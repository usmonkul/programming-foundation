## 1-hafta, 3-kun: Funksiyalar bilan tanishuv (1-qism)

**Maqsad:** Bugun siz JavaScriptda funksiyalarni qanday yaratish va ishlatishni, parametrlar va argumentlarni qanday ishlatishni, funksiyalarning qaytish qiymatini qanday olishni o'rganasiz.

**Dars rejasi:**

1. **Nima uchun funksiyalardan foydalanamiz?**

    * Kodni qayta ishlatish: Funksiyalar bir xil kodni qayta-qayta yozishdan qutqaradi. Bir marta yozilgan funksiyani dasturning istalgan joyida chaqirish mumkin. Bu kodni ixchamlashtiradi va xatolar ehtimolini kamaytiradi.
    * Kodni tushunarli qilish: Funksiyalar kodni kichikroq, boshqarish oson bo'lgan bloklarga ajratadi. Bu kodni o'qish, tushunish va disk raskadrovka qilishni osonlashtiradi.
    * Kodni modullashtirish: Funksiyalar kodni modullarga ajratish imkonini beradi. Bu katta loyihalarda kodni tartibga solish va boshqarishni osonlashtiradi.

2. **Funksiyalarni e'lon qilish:**

    * Funksiyalar `function` kalit so'zi bilan e'lon qilinadi. Funksiya nomi, qavslar ichida parametrlar ro'yxati va figurali qavslar ichida funksiya tanasi yoziladi. Misol:

    ```javascript
    function salomlash() {
      console.log("Salom Dunyo!");
    }
    ```

    Bu kod `salomlash()` nomli funksiyani e'lon qiladi. Bu funksiya hech qanday parametr qabul qilmaydi va konsolda "Salom Dunyo!" xabarini chiqaradi.

    * Funksiyalarni o'zgaruvchiga o'xshatib ham e'lon qilish mumkin:

    ```javascript
    let salomlash = function() {
      console.log("Salom Dunyo!");
    };
    ```

    Bu usulda funksiya nomi o'zgaruvchiga o'xshab yoziladi va oxirida nuqtali vergul qo'yiladi.

3. **Funksiyalarni chaqirish:**

    * Funksiyani chaqirish uchun uning nomini va qavslarni yozish kerak. Misol:

    ```javascript
    salomlash(); // Funksiyani chaqirish
    ```

    Bu kod `salomlash()` funksiyasini ishga tushiradi va natijada konsolda "Salom Dunyo!" xabari chiqadi.

4. **Parametrlar va argumentlar:**

    * Funksiyalar parametrlar orqali ma'lumotlarni qabul qilishi mumkin. Parametrlar funksiya e'lon qilinganda qavslar ichida yoziladi. Misol:

    ```javascript
    function salomlash(ism) {
      console.log("Salom, " + ism + "!");
    }
    ```

    Bu kod `ism` nomli parametr qabul qiluvchi `salomlash()` funksiyasini e'lon qiladi.

    * Funksiyani chaqirganda, parametrlarga mos keladigan qiymatlarni (argumentlarni) berish kerak. Misol:

    ```javascript
    salomlash("Ali"); // "Salom, Ali!" ni chiqaradi
    salomlash("Vali"); // "Salom, Vali!" ni chiqaradi
    ```

    Bu kodda "Ali" va "Vali" qiymatlari argument sifatida `salomlash()` funksiyasiga uzatiladi.

    * Bir nechta parametrlarni ishlatish mumkin:

    ```javascript
    function toliqIsm(ism, familiya) {
      console.log("To'liq ismingiz: " + ism + " " + familiya);
    }

    toliqIsm("Ali", "Valiyev"); // "To'liq ismingiz: Ali Valiyev" ni chiqaradi
    ```

5. **Qaytish qiymati (return):**

    * Funksiyalar `return` kalit so'zi yordamida qiymat qaytarishi mumkin. `return` dan keyin kelgan qiymat funksiyani chaqirgan joyga qaytariladi. Misol:

    ```javascript
    function kvadrat(son) {
      return son * son;
    }

    let natija = kvadrat(5);
    console.log(natija); // 25 ni chiqaradi
    ```

    Bu kodda `kvadrat()` funksiyasi berilgan sonning kvadratini hisoblab, natijani qaytaradi. `kvadrat(5)` ifodasi 25 qiymatini qaytaradi va bu qiymat `natija` o'zgaruvchisiga yuklanadi.

    * `return` funksiyani to'xtatadi. `return` dan keyingi kod bajarilmaydi. Misol:

    ```javascript
    function tekshirish(son) {
      if (son > 10) {
        return "Son 10 dan katta";
      }
      console.log("Bu qator bajarilmaydi"); 
      return "Son 10 dan kichik yoki teng";
    }

    console.log(tekshirish(12)); // "Son 10 dan katta" ni chiqaradi
    ```

    Bu kodda `tekshirish(12)` chaqirilganda, `son > 10` sharti rost bo'ladi va `return "Son 10 dan katta";` qatori bajariladi. Funksiya shu yerda to'xtaydi va "Bu qator bajarilmaydi" qatori bajarilmaydi.

**Mashqlar:**

1.  Ikki sonni ayiruvchi funksiya yarating.
2.  Berilgan son juft yoki toq ekanligini tekshiruvchi funksiya yarating. Funksiya `true` yoki `false` qiymatini qaytarsin.
3.  Foydalanuvchidan ikkita sonni so'rab, ularning ko'paytmasini qaytaruvchi funksiya yarating.