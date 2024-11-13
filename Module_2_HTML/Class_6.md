### **Meta-teglar va Hujjat Strukturasini O‘rganish**

**Maqsad:** HTML hujjati uchun meta-teglar va hujjat strukturasini to‘g‘ri o‘rnatish. Bu brauzerlarga va qidiruv tizimlariga sahifa haqida to‘liqroq ma’lumot beradi.

#### 1. Meta-teg Nima?

Meta-teglar sahifa haqida umumiy ma’lumotlar (metadata) beradi. Bu ma’lumotlar foydalanuvchilarga ko‘rinmaydi, lekin brauzerlar va qidiruv tizimlari uchun muhim.

#### 2. Asosiy Meta-teglar

- **Charset**: Hujjat uchun belgilar kodlash usulini belgilaydi (odatda UTF-8 ishlatiladi).
  ```html
  <meta charset="UTF-8">
  ```

- **Viewport**: Moslashuvchan dizayn (responsive design) uchun kerak. Mobil qurilmalarda sahifa to‘g‘ri ko‘rinishini ta’minlaydi.
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

- **Description**: Qidiruv tizimlari va ijtimoiy tarmoqlarda sahifa tavsifini ko‘rsatadi.
  ```html
  <meta name="description" content="Bu sahifa HTML darslariga bag‘ishlangan.">
  ```

#### 3. Hujjat Strukturasida Title va Link

- **Title**: Brauzer yorlig‘ida ko‘rsatiladigan sahifa nomini belgilaydi.
  ```html
  <title>Mening Sahifam</title>
  ```

- **Link**: Tashqi uslub jadvallarini (CSS) sahifaga ulash uchun ishlatiladi.
  ```html
  <link rel="stylesheet" href="style.css">
  ```

#### 4. Amaliy Mashq

1. HTML sahifangizga `<meta>`, `<title>`, va `<link>` teglari qo‘shing.
2. Tashqi CSS fayliga havola berish orqali sahifangizni bezating.

Quyidagi misolda HTML hujjatining umumiy strukturasini ko‘rishingiz mumkin:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Bu HTML darslari sahifasi.">
  <title>HTML Darslari</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>HTML Darslariga Xush Kelibsiz!</h1>
  <p>Bu sahifada HTML asoslari bilan tanishasiz.</p>
</body>
</html>
```

---

### **HTML-da Kirish Imkoniyatlarini Yaxshilash**

**Maqsad:** HTML-da kirish imkoniyatlarini oshirish uchun zarur bo‘lgan amaliyotlarni o‘rganish.

#### 1. Kirish Imkoniyatlari (Accessibility) Nima?

Kirish imkoniyatlari nogironlar va boshqa imkoniyati cheklangan foydalanuvchilar uchun sahifani osonroq foydalanish imkoniyatini yaratadi. Bu foydalanuvchi tajribasini yaxshilaydi va sahifani barcha odamlar uchun qulay qiladi.

#### 2. Alt Matn Qo‘shish

Rasmlarga **alt** atributini qo‘shish, ekran o‘qiydigan foydalanuvchilar uchun rasmlarning mazmunini ta’riflashga yordam beradi.

```html
<img src="toshkent.jpg" alt="Toshkentning tarixiy joylari">
```

#### 3. Formlarda Yorliqlar Qo‘shish

Shakllar uchun **label** teglari foydalanuvchilarga maydonning vazifasini tushunishga yordam beradi.

```html
<label for="name">Ismingiz:</label>
<input type="text" id="name" name="name">
```

#### 4. ARIA Rollari

ARIA (Accessible Rich Internet Applications) rollari sahifadagi elementlarning vazifasini aniqlash uchun ishlatiladi.

Misol uchun, asosiy mazmun qismi uchun `<main>` tegi mavjud bo‘lmasa, unga `role="main"` atributini qo‘shishingiz mumkin.

```html
<div role="main">
  <h1>Asosiy Maqola</h1>
  <p>Bu asosiy kontent qismi.</p>
</div>
```

#### 5. Amaliy Mashq

1. O‘z sahifangizda har bir rasmga **alt** matn qo‘shing.
2. Shakl maydonlarini **label** teglar bilan belgilab chiqing.
3. ARIA rollarini kiritib, sahifani kirish imkoniyati yuqori qilib yarating.