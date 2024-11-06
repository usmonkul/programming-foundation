### **Ro‘yxatlar va Havolalar**

**Maqsad:** Har xil turdagi ro‘yxatlar yaratishni va boshqa sahifalar yoki manbalarga havolalar qo‘shishni o‘rganish.

#### 1. Ro‘yxatlar Yaratish

HTML bizga tartiblangan va tartiblanmagan ro‘yxatlar yaratishga imkon beradi. Ro‘yxatlar menyular, ko‘rsatmalar yoki punktlar uchun qulay.

- **Tartiblangan ro‘yxat**: Tartiblangan ro‘yxat (`<ol>`) raqamlangan bo‘lib, har bir element ketma-ketlikda ko‘rsatiladi.

  ```html
  <h2>Tartiblangan Ro‘yxat Namuna</h2>
  <ol>
    <li>Birinchi element</li>
    <li>Ikkinchi element</li>
    <li>Uchinchi element</li>
  </ol>
  ```

- **Tartiblanmagan ro‘yxat**: Tartiblanmagan ro‘yxat (`<ul>`) belgilangan bo‘lib, ketma-ketlik shart emas.

  ```html
  <h2>Tartiblanmagan Ro‘yxat Namuna</h2>
  <ul>
    <li>Birinchi element</li>
    <li>Ikkinchi element</li>
    <li>Uchinchi element</li>
  </ul>
  ```

- **Ichki Ro‘yxatlar**: Bir ro‘yxatni boshqa bir `<li>` elementi ichida joylashtirish orqali ichki ro‘yxatlar hosil qilish mumkin.

  ```html
  <h2>Ichki Ro‘yxat Namuna</h2>
  <ul>
    <li>Asosiy element
      <ul>
        <li>Sub-element bir</li>
        <li>Sub-element ikki</li>
      </ul>
    </li>
    <li>Asosiy element ikki</li>
  </ul>
  ```

#### 2. Havolalar Qo‘shish

Havolalar `<a>` tegi yordamida yaratiladi. Ular boshqa veb-sahifalarga yoki fayllarga o‘tish imkonini beradi.

- **Oddiy Havola**: Boshqa veb-sahifaga havola qilish uchun `<a>` tegi bilan `href` atributidan foydalaning. `href` atributi manzilni ko‘rsatadi.

  ```html
  <p>Qo‘shimcha ma‘lumot olish uchun <a href="https://www.example.com">Example veb-sayti</a> ga tashrif buyuring.</p>
  ```

- **Yangi Yorliqda Ochiladigan Havola**: Havolani yangi yorliqda ochish uchun `<a>` tegiga `target="_blank"` qo‘shing.

  ```html
  <p>Example veb-saytini <a href="https://www.example.com" target="_blank">yangi yorliqda oching.</a></p>
  ```

- **Elektron Manzilga Havola**: `mailto:` yordamida elektron manzilga havola yaratish mumkin. Bu bosilganda foydalanuvchining elektron pochta dasturini ochadi.

  ```html
  <p>Biz bilan bog‘lanish uchun <a href="mailto:info@example.com">info@example.com</a> ga yozing.</p>
  ```

#### 3. Namuna: Ro‘yxatlar va Havolalarni Birlash

Quyidagi misol ro‘yxatlar va havolalarni birlashtiradi:

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Ro‘yxatlar va Havolalar</title>
</head>
<body>
  <h1>Mening Sevimli Veb-saytlarim</h1>
  <p>Mana mening tez-tez tashrif buyuradigan veb-saytlarim:</p>
  
  <ul>
    <li><a href="https://www.example.com" target="_blank">Example</a></li>
    <li><a href="https://www.wikipedia.org">Wikipedia</a></li>
    <li><a href="https://www.github.com">GitHub</a></li>
  </ul>
</body>
</html>
```

#### 4. Amaliy Mashq

1. O‘zingizning uchta sevimli kitobingiz yoki filmlaringizdan iborat tartiblangan ro‘yxat yarating.
2. Ko‘p tashrif buyuradigan uchta veb-sayt uchun tartiblanmagan ro‘yxat yarating va ularning har biriga `<a>` tegi yordamida havolalar qo‘shing.

---

### **Rasmlar va Media**

**Maqsad:** HTML hujjatiga rasmlar qo‘shishni va multimedia elementlarini o‘rganish.

#### 1. Rasmlar Qo‘shish

Rasm qo‘shish uchun `<img>` tegidan foydalaniladi. Bu tegin muhim atributlari `src` (manba) va `alt` (muqobil matn) hisoblanadi.

- **Oddiy Rasm Tegi**: `src` atributi rasm fayliga yo‘l ko‘rsatadi, `alt` esa rasmni tasvirlaydi, bu ko‘rish imkoni cheklangan foydalanuvchilar uchun foydali.

  ```html
  <img src="rasm.jpg" alt="Rasm ta'rifi">
  ```

- **Rasmning Hajmini Belgilash**: Kenglik va balandlikni belgilash uchun width va height atributlaridan foydalanishingiz mumkin.

  ```html
  <img src="rasm.jpg" alt="Rasm ta'rifi" width="200" height="100">
  ```

- **URL orqali Rasm**: `src` ga to‘liq URL manzilni kiritish orqali boshqa saytdan rasm qo‘shishingiz mumkin.

  ```html
  <img src="https://www.example.com/rasm.jpg" alt="Misol rasmi">
  ```

#### 2. Havola Qilingan Rasmlar

Rasmni bosiladigan qilish uchun uni `<a>` tegiga o‘rab qo‘yish mumkin.

```html
<a href="https://www.example.com">
  <img src="rasm.jpg" alt="Bosiladigan rasm" width="150">
</a>
```

#### 3. Multimedia Qo‘llash

HTML5 yordamida veb-sahifaga audio va video qo‘shish oson.

- **Audio Qo‘shish**: Tinglash va pauza funksiyasini qo‘shish uchun `<audio>` tegiga `controls` atributini qo‘shing.

  ```html
  <audio controls>
    <source src="audio-fayl.mp3" type="audio/mpeg">
    Brauzeringiz audio elementni qo‘llab-quvvatlamaydi.
  </audio>
  ```

- **Video Qo‘shish**: Xuddi audio kabi, `<video>` tegida `controls` atributidan foydalanib, video fayl qo‘shing.

  ```html
  <video width="320" height="240" controls>
    <source src="video-fayl.mp4" type="video/mp4">
    Brauzeringiz video elementni qo‘llab-quvvatlamaydi.
  </video>
  ```

#### 4. Namuna: Rasm va Multimedia Qo‘shish

Quyidagi misol bitta sahifada rasm, audio va videoni birlashtiradi.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Rasmlar va Multimedia</title>
</head>
<body>
  <h1>Mening Media Sahifamga Xush Kelibsiz</h1>
  
  <h2>Mening Sevimli Rasmim</h2>
  <img src="rasm.jpg" alt="Chiroyli manzara" width="300">
  
  <h2>Mening Sevimli Qo‘shig‘imni Tinglang</h2>
  <audio controls>
    <source src="qo‘shiq.mp3" type="audio/mpeg">
    Brauzeringiz audio elementni qo‘llab-quvvatlamaydi.
  </audio>
  
  <h2>Ajoyib Videoni Tomosha Qiling</h2>
  <video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Brauzeringiz video elementni qo‘llab-quvvatlamaydi.
  </video>
</body>
</html>
```

#### 5. Amaliy Mashq

1. O‘zingizning veb-sahifangizga rasm qo‘shing va uning `alt`, `width` va `height` atributlarini o‘rnating.
2. `<audio>` tegidan foydalanib, audio fayl qo‘shing va `<video>` tegidan foydalanib, video