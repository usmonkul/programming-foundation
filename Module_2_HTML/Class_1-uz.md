Mana, HTML o‘rganishning **1- va 2-kuni** uchun batafsil qo‘llanma. Har bir kun bosqichma-bosqich tushuntirishlar, misollar va mashq topshiriqlarini o‘z ichiga oladi, bu esa o‘rganganlaringizni mustahkamlashga yordam beradi. Keling, boshlaymiz!

---

### **HTML ga kirish**

**Maqsad:** HTML asosiy tuzilishini tushunish va birinchi HTML hujjatingizni yaratish.

#### 1. HTML nima?

HTML (HyperText Markup Language) veb-sahifalar yaratish uchun asosiy til hisoblanadi. U tarkibni tuzish va tashkil qilish uchun teglar (tags) dan foydalanadi, shunda brauzerlar uni qanday ko‘rsatishni bilishadi.

- **Teglar (Tags)** HTML ning asosiy qismi bo‘lib, odatda `<tag>mazmun</tag>` tarzida yoziladi.
- HTML hujjatlari `.html` kengaytmasi bilan saqlanadigan oddiy matn fayllaridir.

#### 2. HTML ning Asosiy Tuzilishi

HTML hujjati ma'lum bir tuzilishga ega:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mening Birinchi Veb Sahifam</title>
  </head>
  <body>
    <h1>Mening Sahifamga Xush Kelibsiz</h1>
    <p>Bu mening HTML da yozgan birinchi paragrafim.</p>
  </body>
</html>
```

- **`<!DOCTYPE html>`**: Hujjatni HTML5 ekanligini bildiradi. Bu brauzerlarga hujjat turini tushunishga yordam beradi.
- **`<html>`**: HTML tarkibini o‘z ichiga oladigan asosiy tag.
- **`<head>`**: Metama’lumotlar (hujjat haqida ma'lumot, masalan, sarlavha yoki stil fayllariga havolalar) o‘z ichiga oladi.
- **`<title>`**: Brauzer yorlig‘ida ko‘rinadigan sahifa sarlavhasini belgilaydi.
- **`<body>`**: Veb-sahifada ko‘rsatiladigan tarkibni (matn, tasvirlar, havolalar va h.k.) o‘z ichiga oladi.

#### 3. Birinchi HTML Hujjatini Yaratish

1. **Matn Tahrirlovchini Ochish**: Notepad, VS Code yoki Sublime Text kabi matn tahrirlovchidan foydalaning.
2. **HTML Kodingizni Yozing**: Yuqoridagi kodni nusxalab tahrirlovchiga joylashtiring.
3. **Faylni Saqlash**: Uni `index.html` nomi bilan saqlang.
4. **Brauzerda Ochish**: Faylni ikki marta bosib, brauzerda oching. Ekranda sarlavha va paragraf ko‘rinishi kerak.

#### 4. Amaliy Mashq

1. `<title>` tegidagi matnni "Mening Ajoyib Veb Sahifam" deb o‘zgartiring va brauzerni yangilang.
2. `<body>` ichida yangi paragraf qo‘shing: `<p>Bu yana bir paragraf!</p>`

---

### **Asosiy Teglar va Tuzilish**

**Maqsad:** Veb-sahifada matnni tuzish uchun ishlatiladigan eng keng tarqalgan HTML teglarni o‘rganish va tarkibni formatlashga kirishish.

#### 1. Sarlavha va Paragraflar

Sarlavha va paragraflar sahifada matnli tarkib yaratishning asosiy qismlari hisoblanadi.

- **Sarlavhalar**: Olti darajadan iborat bo‘lib, `<h1>` (eng kattasi) dan `<h6>` (eng kichigi) gacha. Odatda, `<h1>` asosiy sarlavhalar uchun ishlatiladi, boshqa darajalari esa kichik sarlavhalar uchun.
  
  ```html
  <h1>Bu Asosiy Sarlavha</h1>
  <h2>Bu Kichik Sarlavha</h2>
  <h3>Bu Yanada Kichikroq Sarlavha</h3>
  ```

- **Paragraflar**: `<p>` tegi yordamida yoziladi. Paragraflar blok elementi bo‘lib, avtomatik ravishda yuqori va pastki qismida bo‘sh joy qoldiradi.

  ```html
  <p>Bu HTML da paragraf yozish usuli. Bu blok matn yozish uchun ishlatiladi.</p>
  ```

#### 2. Matn Formatlash Teglari

HTML da matnni shakllantirish va unga urg‘u berish uchun turli xil teglar mavjud. Eng keng tarqalganlaridan ba’zilari:

- **Qalin matn**: `<strong>` yoki `<b>`
  
  ```html
  <p>Bu <strong>muhim</strong> matn.</p>
  ```

- **Kursiv matn**: `<em>` yoki `<i>`
  
  ```html
  <p>Bu matn <em>urg‘ulangan</em>.</p>
  ```

- **Kichik matn**: `<small>`
  
  ```html
  <p>Bu matn <small>kichik hajmda</small>.</p>
  ```

- **Yangi satr qo‘shish**: `<br>` bitta yangi satr qo‘shadi. Bu yopuvchi tegga muhtoj emas.

  ```html
  <p>Bu birinchi satr.<br>Bu esa yangi satr.</p>
  ```

#### 3. Misol: Tuzilgan HTML Hujjatini Yaratish

Ushbu teglar bilan birgalikda quyidagi misolni yaratamiz:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML Asoslari</title>
  </head>
  <body>
    <h1>HTML ga Kirish</h1>
    <p>HTML veb-sahifalarni yaratish tili hisoblanadi. Uni o‘rganish oson va veb-ishlanma uchun muhimdir.</p>

    <h2>Nima uchun HTML ni o‘rganish kerak?</h2>
    <p>HTML <strong>veb-sayt yaratishda</strong> muhim hisoblanadi. U matn, tasvir va multimedia tarkibini tuzishda ishlatiladi.</p>

    <h2>Asosiy Matn Formatlash</h2>
    <p>Bu yerda <em>urg‘ulangan matn</em> va <small>kichik hajmdagi matn</small> mavjud.</p>

    <p>Hujjat tugadi.<br>O‘qiganingiz uchun rahmat!</p>
  </body>
</html>
```

#### 4. Amaliy Mashq

1. Yangi HTML fayl yarating va ichida quyidagilarni kiriting:
   - Bir `<h1>` va bir `<h2>` sarlavha.
   - Qalin va kursiv matnli bir nechta paragraflar.
2. Biror bir paragraflarda `<br>` dan foydalanib, yangi satrlar qo‘shing.
