**Dars rejasi:**

1. **Massivlarni eslatish:**

    * Massiv - bu tartiblangan qiymatlar to'plami.
    * Indekslar 0 dan boshlanadi.
    * Massivlar dinamik o'lchamga ega.

2. **Ko'p o'lchamli massivlar:**

    * Massivlar ichida boshqa massivlarni saqlash mumkin. Bu ko'p o'lchamli massivlar deyiladi. Misol uchun, ikki o'lchamli massiv matritsani ifodalashi mumkin:

    ```javascript
    let matritsa = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9]
    ];

    console.log(matritsa[0][0]); // 1 ni chiqaradi
    console.log(matritsa[1][2]); // 6 ni chiqaradi
    ```

    * Ko'p o'lchamli massivlar bilan ishlash uchun ichma-ich sikllardan foydalanish mumkin.

3. **Massiv metodlari (qayta ko'rib chiqish va qo'shimcha):**

    * `push()`, `pop()`, `unshift()`, `shift()`, `splice()` metodlarini eslatish.
    * `concat()`: Ikki yoki undan ortiq massivlarni birlashtirib, yangi massiv qaytaradi.

    ```javascript
    let a = [1, 2];
    let b = [3, 4];
    let c = a.concat(b); // c = [1, 2, 3, 4]
    ```

    * `slice()`: Massivning bir qismini yangi massiv sifatida qaytaradi.

    ```javascript
    let a = [1, 2, 3, 4, 5];
    let b = a.slice(1, 4); // b = [2, 3, 4]
    ```

    * `indexOf()`, `lastIndexOf()`, `includes()` metodlarini eslatish.
    * `join()`: Massiv elementlarini matnga birlashtiradi.

    ```javascript
    let a = ["Salom", "dunyo"];
    let b = a.join(" "); // b = "Salom dunyo"
    ```

    * `reverse()`: Massiv elementlarini teskari tartibda joylashtiradi.

    ```javascript
    let a = [1, 2, 3];
    a.reverse(); // a = [3, 2, 1]
    ```

    * `sort()`: Massiv elementlarini alifbo tartibida yoki o'sish tartibida saralaydi.

    ```javascript
    let a = [3, 1, 2];
    a.sort(); // a = [1, 2, 3]
    ```

    * `forEach()`: Massivning har bir elementi uchun funksiyani bajaradi.

    ```javascript
    let a = [1, 2, 3];
    a.forEach(function(element) {
      console.log(element * 2);
    });
    // Chiqish:
    // 2
    // 4
    // 6
    ```

    * `map()`: Massivning har bir elementi uchun funksiyani bajaradi va natijalarni yangi massivda qaytaradi.

    ```javascript
    let a = [1, 2, 3];
    let b = a.map(function(element) {
      return element * 2;
    });
    console.log(b); // [2, 4, 6]
    ```

    * `filter()`: Berilgan shartga mos keladigan elementlarni yangi massivda qaytaradi.

    ```javascript
    let a = [1, 2, 3, 4, 5];
    let b = a.filter(function(element) {
      return element > 2;
    });
    console.log(b); // [3, 4, 5]
    ```

    * `reduce()`: Massiv elementlarini bitta qiymatga qisqartiradi.

    ```javascript
    let a = [1, 2, 3, 4, 5];
    let yigindi = a.reduce(function(accumulator, currentValue) {
      return accumulator + currentValue;
    }, 0);
    console.log(yigindi); // 15
    ```

4. **Massivlar bilan ishlash bo'yicha maslahatlar:**

    * Massivlarni samarali ishlatish uchun ularning xususiyatlari va metodlarini yaxshi bilish kerak.
    * Massivlar bilan ishlashda sikllar va shartli operatorlardan foydalanish ko'p hollarda zarur bo'ladi.
    * Murakkab masalalarni yechish uchun ko'p o'lchamli massivlar va massiv metodlarini birgalikda ishlatish mumkin.

**Mini-loyiha:**

* Foydalanuvchidan 10 ta son kiritishni so'rang va ularni massivga saqlang. So'ngra, massivning o'rtacha qiymatini hisoblang va konsolda chiqaring.

**Mashqlar:**

1.  Ikki o'lchamli massiv yarating va uning elementlarini konsolda chiqaring.
2.  Berilgan massivda nechta juft son borligini aniqlovchi funksiya yarating.
3.  Berilgan massivda berilgan element necha marta takrorlanganini aniqlovchi funksiya yarating.


1. **`for` siklini eslatish:**

    * `for` sikli uchta qismdan iborat:
        * Boshlang'ich qiymat: Sikl boshlanishidan oldin bir marta bajariladigan ifoda. Odatda, bu sikl o'zgaruvchisini (masalan, `i`) 0 ga tenglashtirish uchun ishlatiladi.
        * Shart: Har bir iteratsiyadan oldin tekshiriladigan mantiqiy ifoda. Agar shart rost bo'lsa, sikl tanasi bajariladi. Aks holda, sikl to'xtaydi.
        * Qadam: Har bir iteratsiyadan keyin bajariladigan ifoda. Odatda, bu sikl o'zgaruvchisini 1 ga oshirish (`i++`) yoki kamaytirish (`i--`) uchun ishlatiladi.

    ```javascript
    for (let i = 0; i < 10; i++) {
      console.log(i); // 0 dan 9 gacha bo'lgan sonlarni chiqaradi
    }
    ```

2. **Massivlar bilan `for` sikli:**

    * Massiv elementlari bo'ylab takrorlash uchun `for` siklidan foydalanish mumkin. Sikl o'zgaruvchisi massiv indekslarini ifodalaydi. Misol:

    ```javascript
    let ranglar = ["qizil", "yashil", "ko'k"];

    for (let i = 0; i < ranglar.length; i++) {
      console.log(ranglar[i]);
    }
    // Chiqish:
    // "qizil"
    // "yashil"
    // "ko'k"
    ```

    Bu kodda `for` sikli `ranglar` massividagi har bir element uchun `console.log(ranglar[i])` qatorini bajaradi. `i` o'zgaruvchisi 0 dan boshlanadi va `ranglar.length` dan kichik bo'lgancha 1 ga oshib boradi. Har bir iteratsiyada `ranglar[i]` kodi massivning `i`-indeksdagi elementini qaytaradi.

3. **Massiv elementlarini o'zgartirish:**

    * `for` sikli yordamida massiv elementlarini o'zgartirish mumkin. Misol:

    ```javascript
    let sonlar = [1, 2, 3, 4, 5];

    for (let i = 0; i < sonlar.length; i++) {
      sonlar[i] = sonlar[i] * 2;
    }

    console.log(sonlar); // [2, 4, 6, 8, 10] ni chiqaradi
    ```

    Bu kodda `for` sikli `sonlar` massividagi har bir elementni 2 ga ko'paytiradi.

4. **`for` sikli bilan massiv elementlarini qidirish:**

    * `for` sikli yordamida massivda ma'lum bir shartga mos keladigan elementlarni qidirish mumkin. Misol:

    ```javascript
    let sonlar = [1, 5, 2, 8, 3, 7];

    for (let i = 0; i < sonlar.length; i++) {
      if (sonlar[i] > 5) {
        console.log(sonlar[i] + " soni 5 dan katta");
      }
    }
    // Chiqish:
    // "8 soni 5 dan katta"
    // "7 soni 5 dan katta"
    ```

    Bu kodda `for` sikli `sonlar` massividagi har bir elementni tekshiradi va agar element 5 dan katta bo'lsa, tegishli xabarni konsolda chiqaradi.

5. **Ichma-ich `for` sikllari:**

    * Ko'p o'lchamli massivlar bilan ishlash uchun ichma-ich `for` sikllaridan foydalanish mumkin. Misol:

    ```javascript
    let matritsa = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9]
    ];

    for (let i = 0; i < matritsa.length; i++) {
      for (let j = 0; j < matritsa[i].length; j++) {
        console.log(matritsa[i][j]);
      }
    }
    ```

    Bu kodda tashqi `for` sikli matritsaning qatorlari bo'ylab, ichki `for` sikli esa har bir qatorning elementlari bo'ylab takrorlanadi.

**Mini-loyiha:**

* Foydalanuvchidan 5 ta ism kiritishni so'rang va ularni massivga saqlang. So'ngra, `for` sikli yordamida har bir ismning uzunligini konsolda chiqaring.

**Mashqlar:**

1.  Berilgan massivda nechta manfiy son borligini aniqlovchi funksiya yarating.
2.  Berilgan massivda berilgan qiymatdan katta bo'lgan elementlarni yangi massivda qaytaruvchi funksiya yarating.
3.  Ikki o'lchamli massiv yarating va uning barcha elementlarining yig'indisini hisoblang.

Ushbu qo'shimchalar bilan `for` sikli yordamida massivlar bo'ylab takrorlash mavzusi yanada tushunarli bo'ldi degan umiddaman. Agar yana savollar bo'lsa, bemalol so'rang!
