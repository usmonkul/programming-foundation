

### **Form (2-qism)**

**Maqsad:** Turli kiritish turlari, Form maydonlarini tashkil qilish va yanada murakkab Form yaratishni o‘rganish.

#### 1. Turli Kiritish Turlarini Qo‘shish

HTML Formida foydalanuvchilardan turli xil ma’lumotlarni to‘plash uchun bir qancha kiritish turlaridan foydalanishingiz mumkin. Keling, eng keng tarqalgan turlar bilan tanishamiz:

- **Belgilash katakchalari**: Foydalanuvchiga bir nechta variantni tanlash imkonini beradi.

  ```html
  <label><input type="checkbox" name="hobby" value="o'qish"> O'qish</label>
  <label><input type="checkbox" name="hobby" value="sayohat"> Sayohat</label>
  <label><input type="checkbox" name="hobby" value="musiqa"> Musiqa</label>
  ```

- **Radio Tugmalar**: Foydalanuvchiga faqat bitta variantni tanlash imkonini beradi.

  ```html
  <p>Sevimli rangingizni tanlang:</p>
  <input type="radio" name="color" value="qizil" id="qizil">
  <label for="qizil">Qizil</label>
  
  <input type="radio" name="color" value="ko'k" id="ko'k">
  <label for="ko'k">Ko'k</label>
  
  <input type="radio" name="color" value="yashil" id="yashil">
  <label for="yashil">Yashil</label>
  ```

- **Ochish Ro‘yxati**: Foydalanuvchiga ro‘yxatdan tanlash imkonini beradi.

  ```html
  <label for="city">Shaharni tanlang:</label>
  <select id="city" name="city">
    <option value="toshkent">Toshkent</option>
    <option value="samarqand">Samarqand</option>
    <option value="buxoro">Buxoro</option>
  </select>
  ```

#### 2. `<fieldset>` va `<legend>` yordamida Maydonlarni Guruhlash

O‘xshash maydonlarni guruhlash uchun `<fieldset>` dan foydalanishingiz mumkin va guruhga nom berish uchun `<legend>` ishlatiladi.

```html
<form>
  <fieldset>
    <legend>Shaxsiy Ma’lumotlar</legend>
    <label for="name">Ism:</label>
    <input type="text" id="name" name="name">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
  </fieldset>
  
  <fieldset>
    <legend>Afzalliklar</legend>
    <label><input type="checkbox" name="preference" value="yangiliklar"> Yangiliklar</label>
    <label><input type="checkbox" name="preference" value="yangilanishlar"> Yangilanishlar</label>
  </fieldset>
  
  <input type="submit" value="Yuborish">
</form>
```

#### 3. Amaliy Mashq

1. Turli kiritish turlari bilan Form yarating: belgilash katakchalari, radio tugmalar va ochish ro‘yxatidan foydalaning.
2. Formni mantiqiy qismlarga bo‘lish uchun `<fieldset>` va `<legend>` dan foydalaning.

---

### ** Semantik HTML**

**Maqsad:** Semantik HTML elementlari bilan tanishish va ularni ishlatish orqali kodni o‘qilishi oson, to‘liq va strukturalangan qilishni o‘rganish.

#### 1. Semantik HTML nima?

Semantik HTML – ma’noli teglarni qo‘llab, mazmunni aniq tasvirlaydi. Bu ekran o‘qiydiganlar va qidiruv tizimlari uchun sahifani oson tushunishga yordam beradi.

#### 2. Asosiy Semantik Elementlar

- **`<header>`**: Odatda kirish yoki navigatsiya havolalari joylashgan bo‘lim.
- **`<nav>`**: Navigatsiya havolalarini saqlash uchun.
- **`<main>`**: Sahifani asosiy mazmunini o‘z ichiga oladi.
- **`<article>`**: O‘z ichiga mustaqil mazmun (masalan, maqola yoki blog posti) oladi.
- **`<section>`**: Sahifadagi o‘xshash mazmunni guruhlash uchun.
- **`<aside>`**: Asosiy mazmundan tashqari ma’lumotlar uchun (masalan, yon panel).
- **`<footer>`**: Mualliflik huquqi yoki aloqa havolalari joylashgan bo‘lim.

#### 3. Semantik HTML bilan Oddiy Veb-sahifa Tuzish

Quyida semantik HTML yordamida tuzilgan sahifa ko‘rinishi:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Semantik HTML</title>
</head>
<body>

  <header>
    <h1>Mening Saytim</h1>
    <nav>
      <a href="#home">Bosh sahifa</a>
      <a href="#about">Biz haqimizda</a>
      <a href="#contact">Bog‘lanish</a>
    </nav>
  </header>

  <main>
    <section id="home">
      <h2>Saytimga Xush Kelibsiz</h2>
      <p>Bu HTML semantik tuzilishi misoli.</p>
    </section>
    
    <section id="about">
      <h2>Biz Haqimizda</h2>
      <p>Biz web dasturlash bo‘yicha yuqori sifatli qo‘llanmalarni taqdim etamiz.</p>
    </section>
  </main>

  <aside>
    <h3>Qo‘shimcha Havolalar</h3>
    <ul>
      <li><a href="#blog">Blog</a></li>
      <li><a href="#resurslar">Resurslar</a></li>
    </ul>
  </aside>

  <footer>
    <p>&copy; 2024 Mening Saytim. Barcha huquqlar himoyalangan.</p>
  </footer>

</body>
</html>
```

#### 4. Semantik HTMLning Foydalari

- **Yaxshi Mavjudlik**: Ekran o‘qiydiganlar uchun navigatsiyani osonlashtiradi.
- **SEO uchun Yaxshiroq**: Qidiruv tizimlari tuzilgan va aniq mazmunli sahifalarni afzal ko‘radi.
- **Qulaylik va Uslubiylik**: Struktura tushunarli bo‘lib, kodni o‘zgartirish va yangilash osonroq bo‘ladi.

#### 5. Amaliy Mashq

1. `<header>`, `<nav>`, `<main>`, `<section>`, `<aside>`, va `<footer>` teglarini ishlatib, sahifa tuzilmangizni yarating.
2. Har bir qismga matn qo‘shib, uni brauzerda qanday ko‘rinishini tekshiring.