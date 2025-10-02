MATKUL:PEMOGRAMAN WEB1
NAMA:ZAKI FAUZAN AKHBARI
KELAS:TI.24.A.4
NIM:312410348

# Tugas CSS - README

## 1. Eksperimen CSS

Pada tugas ini dilakukan eksperimen dengan mengubah dan menambah properti CSS berdasarkan CSS Cheat Sheet.
Contoh sederhana:

```css
h1 {
  color: blue;
  font-size: 32px;
  text-align: center;
}

p {
  color: gray;
  line-height: 1.5;
}
```

---

## 2. Perbedaan `h1 {...}` dengan `#intro h1 {...}`

* **`h1 {...}`**
  Selektor ini berlaku untuk semua elemen `<h1>` di halaman HTML.

* **`#intro h1 {...}`**
  Selektor ini hanya berlaku pada `<h1>` yang berada **di dalam elemen dengan id `intro`**.

**Contoh:**

```html
<h1>Judul Umum</h1>
<div id="intro">
  <h1>Judul di Intro</h1>
</div>
```

```css
h1 {
  color: blue;
}
#intro h1 {
  color: red;
}
```

**Hasil:**

* "Judul Umum" → biru
* "Judul di Intro" → merah

---

## 3. Urutan Prioritas CSS (Inline, Internal, External)

Aturan prioritas CSS:

1. **Inline CSS** (style langsung pada elemen) → paling tinggi
2. **Internal CSS** (di `<style>...</style>` dalam `<head>`)
3. **External CSS** (file `.css` yang dilink)
4. **Default browser**

**Contoh:**

```html
<head>
  <link rel="stylesheet" href="style.css"> <!-- External -->
  <style>
    p { color: green; } <!-- Internal -->
  </style>
</head>
<body>
  <p style="color: red;">Teks ini berwarna merah</p> <!-- Inline -->
</body>
```

**Hasil:**
Teks akan berwarna **merah** karena inline lebih kuat.

---

## 4. Elemen dengan ID dan Class

Jika sebuah elemen memiliki **ID** dan **Class**, maka prioritas adalah:

* Inline > **ID** > Class > Element

**Contoh:**

```html
<p id="paragraf-1" class="text-paragraf">Contoh teks</p>
```

```css
.text-paragraf {
  color: blue;
}
#paragraf-1 {
  color: red;
}
```

**Hasil:**
Teks akan berwarna **merah**, karena **ID lebih kuat daripada Class**.

---

## Kesimpulan

* `h1` bersifat global, sedangkan `#intro h1` lebih spesifik.
* Inline CSS memiliki prioritas paling tinggi dibanding internal dan eksternal.
* Selector ID (`#id`) lebih kuat dibanding Class (`.class`).
* Urutan prioritas CSS: **Inline > ID > Class > Elemen**.

---
