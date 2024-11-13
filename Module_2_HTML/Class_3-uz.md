### **Jadval yaratish**

**Maqsad:** HTML yordamida jadvallar yaratishni o‘rganing. Jadvallar ma’lumotlarni tuzilgan holda taqdim etish, jadval ko‘rinishidagi ma’lumotlar va ro‘yxatlar uchun juda qulay.

#### 1. Jadvalning Asosiy Tuzilishi

HTML jadvallari quyidagi elementlardan iborat:

- `<table>`: Jadvalning asosiy konteyneri.
- `<tr>`: Jadval satri (jadvalning har bir qatori).
- `<th>`: Jadval sarlavhasi (ustunlarning nomlari).
- `<td>`: Jadval ma’lumoti (har bir qatorning ichidagi ma’lumotlar hujayrasi).

Oddiy misol:

```html
<h2>Oddiy Jadval</h2>
<table>
  <tr>
    <th>Kun</th>
    <th>Faoliyat</th>
    <th>Vaqt</th>
  </tr>
  <tr>
    <td>Dushanba</td>
    <td>Sport zali</td>
    <td>07:00</td>
  </tr>
  <tr>
    <td>Seshanba</td>
    <td>Suzish</td>
    <td>18:00</td>
  </tr>
</table>
```

#### 2. Jadvalga Chegaralar Qo‘shish

Chegaralarni qo‘shib, jadvallaringizni yanada tartibli qilish mumkin.

```html
<table border="1">
  <tr>
    <th>Ism</th>
    <th>Yosh</th>
    <th>Kasb</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>30</td>
    <td>Muhandis</td>
  </tr>
  <tr>
    <td>Sara</td>
    <td>28</td>
    <td>Dizayner</td>
  </tr>
</table>
```

#### 3. Ustun va Qatorlarni Birlash

Ba’zida hujayralarni bir nechta ustun yoki qatorda birlashtirish kerak bo‘lishi mumkin:

- **colspan**: Hujayrani gorizontal yo‘nalishda birlashtiradi.
- **rowspan**: Hujayrani vertikal yo‘nalishda birlashtiradi.

```html
<table border="1">
  <tr>
    <th colspan="2">Bog‘lanish Ma’lumotlari</th>
  </tr>
  <tr>
    <td>Email</td>
    <td>example@example.com</td>
  </tr>
  <tr>
    <td>Telefon</td>
    <td>+123-456-7890</td>
  </tr>
</table>
```

#### 4. Namuna: Jadval Elementlarini Birlashtirish

Quyidagi misol ko‘proq tafsilotlarni o‘z ichiga olgan jadval tuzilishini namoyish etadi:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Haftalik Jadval</title>
</head>
<body>
  <h1>Mening Haftalik Jadvalim</h1>
  <table border="1">
    <tr>
      <th>Kun</th>
      <th>Faoliyat</th>
      <th>Vaqt</th>
    </tr>
    <tr>
      <td rowspan="2">Dushanba</td>
      <td>Sport zali</td>
      <td>07:00</td>
    </tr>
    <tr>
      <td>Ish</td>
      <td>09:00 - 17:00</td>
    </tr>
  </table>
</body>
</html>
```

#### 5. Amaliy Mashq

1. 3x3 o‘lchamli jadval yarating.
2. Birinchi qatorda sarlavha qatori bo‘lsin va har bir ustun nomini qalin qilib qo‘ying.
3. Bir hujayrada colspan yoki rowspandan foydalaning.

---

### **6-kun: Form - Foydalanuvchi Ma’lumotlarini Kiritish**

**Maqsad:** HTML Formi yordamida foydalanuvchi ma’lumotlarini yig‘ish uchun kerakli elementlar bilan Form yaratishni o‘rganish.

#### 1. Formning Asosiy Tuzilishi

Form yaratish uchun `<form>` tegi barcha kirish elementlarini o‘z ichiga oladi. Formda quyidagi atributlar ishlatiladi:

- `action`: Form ma’lumotlarini yuborish manzili.
- `method`: Ma’lumotni yuborish usuli (masalan, `GET` yoki `POST`).

```html
<form action="submit_form.php" method="POST">
  <!-- Form elementlari shu yerga kiritiladi -->
</form>
```

#### 2. Formning Asosiy Elementlari

Formda quyidagi keng tarqalgan elementlardan foydalaniladi:

- **Matn Kiritish**: `<input type="text">` bir qatorli matn maydonlari uchun ishlatiladi.
  
  ```html
  <label for="name">Ism:</label>
  <input type="text" id="name" name="name">
  ```

- **Elektron Pochta Kiritish**: `<input type="email">` elektron pochta manzillarini kiritish uchun.

  ```html
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">
  ```

- **Parol Kiritish**: `<input type="password">` parollar uchun.

  ```html
  <label for="password">Parol:</label>
  <input type="password" id="password" name="password">
  ```

- **Yuborish Tugmasi**: `<input type="submit">` Formni yuborish uchun.

  ```html
  <input type="submit" value="Yuborish">
  ```

#### 3. Ochiluvchi Ro‘yxat va Radio Tugmalar

Formda ochiluvchi ro‘yxatlar va radio tugmalardan ham foydalanish mumkin.

- **Ochiluvchi Ro‘yxat (Select Box)**: `<select>` va `<option>` yordamida amalga oshiriladi.

  ```html
  <label for="city">Shaharni tanlang:</label>
  <select id="city" name="city">
    <option value="tashkent">Toshkent</option>
    <option value="samarkand">Samarqand</option>
    <option value="bukhara">Buxoro</option>
  </select>
  ```

- **Radio Tugmalar**: Foydalanuvchiga bir nechta variantdan bittasini tanlash imkonini beradi.

  ```html
  <p>Jinsingiz:</p>
  <input type="radio" id="erkak" name="gender" value="erkak">
  <label for="erkak">Erkak</label>
  
  <input type="radio" id="ayol" name="gender" value="ayol">
  <label for="ayol">Ayol</label>
  ```

#### 4. Namuna: To‘liq Form

Quyidagi misol turli Form elementlarini birlashtiradi:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Ro‘yxatdan o‘tish Formi</title>
</head>
<body>
  <h1>Ro‘yxatdan o‘tish Formi</h1>
  <form action="submit_form.php" method="POST">
    
    <label for="name">Ism:</label>
    <input type="text" id="name" name="name"><br><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <label for="password">Parol:</label>
    <input type="password" id="password" name="password"><br><br>
    
    <p>Jinsingiz:</p>
    <input type="radio" id="erkak" name="gender" value="erkak">
    <label for="erkak">Erkak</label>
    
    <input type="radio" id="ayol" name="gender" value="ayol">
    <label for="ayol">Ayol</label><br><br>
    
    <label for="city">Shaharni tanlang:</label>
    <select id="city" name="city">
      <option value="tashkent">Toshkent</option>
      <option value="samarkand">Samarqand</option>
      <option value="bukhara">Buxoro</option>
    </select><br><br

    <input type="submit" value="Ro‘yxatdan o‘tish">
    
  </form>
</body>
</html>
```