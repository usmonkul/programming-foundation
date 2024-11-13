
### **Blok va Inline Elementlar**

**Maqsad:** Blok va inline elementlarning farqlarini tushunish va ularni veb-sahifadagi mazmunni tartibga solishda ishlatishni o‘rganish.

#### 1. Blok va Inline Elementlar Nima?

- **Blok elementlar**: Har doim yangi qatorni boshlab, to‘liq kenglikni egallaydi. Masalan: `<div>`, `<h1>` - `<h6>`, `<p>`, `<ul>`, va `<table>`.
- **Inline elementlar**: Faqat o‘z ichidagi mazmun uchun kerakli kenglikni egallaydi va yangi qator boshlamaydi. Masalan: `<span>`, `<a>`, `<img>`, va `<strong>`.

#### 2. Blok va Inline Elementlar Orasidagi Farqlar

- **Blok element** yangi qator boshlab, to‘liq kenglikni egallaydi.
- **Inline element** esa faqat kerakli o‘rinni oladi va boshqa elementlar bilan bir qatorda joylashadi.

Misollar bilan ko‘rib chiqamiz:

```html
<div style="background-color: lightblue; padding: 10px;">Bu blok element (div)</div>
<span style="background-color: yellow;">Bu inline element (span)</span>
<span style="background-color: yellow;">Bu ham inline element</span>
```

#### 3. Amaliy Mashq

1. Sahifada `<div>` va `<span>` elementlarini joylashtiring va ularning joylashishini tekshiring.
2. Inline va blok elementlar yordamida sahifada kichik bir qism yaratib, farqlarni ko‘rib chiqing.

---

### **  **Form (3-qism)**

**Maqsad:** Formda yuborish tugmachasi va boshqa tugmachalar yaratish, shuningdek, `<form>` tegi uchun `method` va `action` atributlari haqida o‘rganish.

#### 1. Form Tugmachalari

Formda ikki asosiy tugmachalar mavjud:

- **Yuborish Tugmasi**: Form ma’lumotlarini jo‘natish uchun ishlatiladi.
  ```html
  <input type="submit" value="Yuborish">
  ```

- **Oddiy Tugma**: Amallarni bajarish uchun ishlatiladi, masalan, Formni tozalash.
  ```html
  <button type="button" onclick="alert('Tugmani bosdingiz!')">Oddiy Tugma</button>
  ```

#### 2. `<form>` Tagida `method` va `action` Atributlari

- **method**: Form ma’lumotlarini qanday jo‘natishni belgilaydi. Ikkita asosiy qiymatga ega:
  - `GET`: URL orqali jo‘natadi, odatda qidiruv Formida ishlatiladi.
  - `POST`: Xavfsiz usul bo‘lib, katta hajmdagi ma’lumotlarni jo‘natishda ishlatiladi.
  
- **action**: Form jo‘natilganda ma’lumotlarni qabul qiladigan URL manzilini belgilaydi.

Misol:

```html
<form action="/maqsad_url" method="POST">
  <label for="ism">Ism:</label>
  <input type="text" id="ism" name="ism">
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">
  
  <input type="submit" value="Jo‘natish">
</form>
```

#### 3. Amaliy Mashq

1. Form yarating va unga bir nechta kiritish maydonlarini qo‘shing.
2. `method` va `action` atributlarini ishlatib, ma’lumotlarni jo‘natishni sinab ko‘ring.
