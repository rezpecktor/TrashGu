# TrashGu Design System

**Version:** 0.1
**Status:** Approved design direction, implementation pending
**Design approach:** Environmental Editorial Utility
**Login layout:** Split Editorial
**Design quality framework:** Anti-Slop

---

## 1. Product Identity

TrashGu adalah aplikasi yang membantu pengguna mengenali dan mengklasifikasikan sampah, memahami kategori hasil klasifikasi, dan mendukung kebiasaan pemilahan sampah yang lebih baik.

### Brand Personality

- **Clear:** Informasi mudah dipahami.
- **Grounded:** Terasa dekat dengan kehidupan sehari-hari.
- **Trustworthy:** Tidak berlebihan dalam menyampaikan kemampuan aplikasi.
- **Practical:** Mengutamakan tindakan yang dapat dilakukan pengguna.
- **Human:** Bahasa ramah, natural, dan tidak kaku.

### Core Principle

**Clarity before decoration.**

Setiap elemen visual harus memiliki tujuan yang jelas: memperkuat identitas, membantu pemahaman, memperjelas navigasi, atau mendukung interaksi.

TrashGu tidak boleh terlihat seperti template SaaS atau dashboard AI generik.

---

## 2. Anti-Slop Integration

Gunakan empat skill resmi yang telah dipasang dari:

https://github.com/miqdadbadjuber/anti-slop

Lokasi project-scoped:

```text
.codex/skills/
├── antislop/
├── antislop-ui/
├── antislop-human/
└── antislop-layoutmobile/
```

### Skill Responsibilities

| Skill                 | Tanggung jawab                                       |
| --------------------- | ---------------------------------------------------- |
| antislop              | Pemeriksaan pola generik dan kualitas keseluruhan    |
| antislop-ui           | Hierarki visual, komponen, performa, dan kualitas UI |
| antislop-human        | Aksesibilitas, usability, dan perilaku interaksi     |
| antislop-layoutmobile | Responsive layout dan pengalaman mobile              |

### Working Modes

- **AFTER:** Audit tampilan yang sudah ada.
- **DURING:** Evaluasi kualitas ketika implementasi UI berlangsung.

### Anti-Slop Design Rules

Hindari:

- Gradient dekoratif tanpa alasan.
- Glow dan shadow berlebihan.
- Kartu seragam untuk semua jenis informasi.
- Layout dashboard generik yang tidak mencerminkan kebutuhan pengguna.
- Headline dan microcopy yang terdengar seperti template.
- Ikon dekoratif yang tidak membantu pengguna.
- Animasi berlebihan.
- Elemen interaktif palsu.
- Ketergantungan berlebihan pada satu warna aksen.
- Desain mobile yang hanya merupakan desktop yang diperkecil.

Anti-Slop berfungsi sebagai quality filter, bukan pengganti identitas visual TrashGu.

Jika terdapat konflik antara rekomendasi desain dan kebutuhan fungsional aplikasi, pertahankan fungsi yang sudah bekerja dan laporkan konfliknya.

---

## 3. Visual Direction

### Design Identity

**Environmental Editorial Utility**

Desain menggabungkan dua karakter:

**Editorial**

Digunakan untuk identitas merek, headline, storytelling singkat, dan komposisi visual yang berkarakter.

**Utility**

Digunakan untuk form, tombol, navigasi, klasifikasi, hasil prediksi, statistik, dan riwayat.

### Anti-Slop Design Dials

- ENERGY: 1
- RHYTHM: 2
- MOTION: 1

Interpretasi:

- Tampilan tenang dan tidak terlalu ramai.
- Komposisi memiliki variasi hierarki yang disengaja.
- Animasi minimal dan hanya untuk feedback yang berguna.

### Visual Priorities

1. Keterbacaan.
2. Kejelasan tindakan utama.
3. Konsistensi visual.
4. Identitas lingkungan.
5. Aksesibilitas.
6. Dekorasi seperlunya.

---

## 4. Color System

### Core Palette

| Token  | Hex       | Usage                              |
| ------ | --------- | ---------------------------------- |
| Forest | `#244C3D` | Primary brand, CTA, branding panel |
| Paper  | `#F6F5EF` | Main background                    |
| Sage   | `#DDE8DB` | Secondary surfaces                 |
| Ink    | `#202A25` | Primary text                       |
| Line   | `#D7DED5` | Borders and dividers               |

Palet ini adalah baseline desain. Penggunaan final setiap kombinasi warna harus lolos pemeriksaan kontras.

### Color Principles

- Hijau adalah identitas TrashGu, bukan warna untuk setiap elemen.
- Gunakan warna netral sebagai fondasi.
- Warna kategori sampah harus konsisten di seluruh halaman.
- Warna error, warning, success, dan informasi harus dibedakan berdasarkan makna.
- Jangan menggunakan warna sebagai satu-satunya indikator status.
- Jangan menggunakan gradient hanya untuk membuat tampilan terlihat modern.

### Accessibility

- Kontras teks normal minimal 4.5:1.
- Kontras teks besar minimal 3:1.
- Indikator fokus dan komponen penting harus memiliki kontras yang memadai.
- Verifikasi setiap kombinasi warna aktual sebelum digunakan.

---

## 5. Typography

### Typography Direction

Gunakan tipografi modern, natural, dan mudah dibaca.

### Principles

- Headline boleh lebih ekspresif daripada body text.
- Teks antarmuka harus sederhana dan jelas.
- Hindari terlalu banyak ukuran dan font weight.
- Gunakan line-height yang nyaman.
- Jangan menggunakan ukuran teks sangat kecil demi estetika.
- Hindari uppercase panjang untuk konten utama.
- Pastikan tipografi tetap nyaman pada mobile.

### Font Policy

- Prioritaskan font dan fallback yang sudah tersedia.
- Jangan menambah font dependency tanpa persetujuan.
- Font final dipilih setelah mempertimbangkan keterbacaan, performa, dan konsistensi.

---

## 6. Layout and Spacing

### Layout Principles

- Gunakan whitespace untuk membangun hierarki.
- Pertahankan alignment yang konsisten.
- Gunakan border dan shadow secara selektif.
- Hindari card untuk setiap kelompok informasi.
- Gunakan asimetri secara terkontrol.
- Jangan membuat layout kompleks jika tidak meningkatkan usability.

### Responsive Principles

- Mobile adalah pengalaman yang dirancang secara sengaja.
- Konten utama harus tetap mudah ditemukan pada layar kecil.
- Hindari horizontal scrolling.
- Jangan membuat elemen dekoratif mendominasi viewport mobile.
- Pastikan form tetap dapat digunakan saat keyboard virtual terbuka.

Spacing, radius, dan breakpoint final harus mengikuti kebutuhan implementasi dan teknologi yang sudah digunakan.

---

## 7. Login Page: Split Editorial

### Design Objective

Membuat halaman login yang memiliki identitas TrashGu kuat, tetapi tetap cepat, jelas, dan nyaman digunakan.

### Desktop Composition

Gunakan dua area utama.

#### Left: Editorial Brand Panel

Berisi:

- Logo atau identitas TrashGu.
- Headline singkat yang relevan dengan pengelolaan sampah.
- Deskripsi singkat manfaat aplikasi.
- Elemen visual lingkungan yang memiliki konteks.

Contoh headline:

**Kenali sampah. Mulai dari sini.**

Contoh supporting copy:

_Langkah sederhana menuju pemilahan yang lebih baik._

Hindari:

- Ilustrasi dekoratif yang tidak berkaitan dengan produk.
- Terlalu banyak teks.
- Gradient atau efek visual berlebihan.
- Animasi yang mengganggu.

#### Right: Login Form

Berisi:

- Heading "Masuk ke TrashGu".
- Deskripsi singkat jika diperlukan.
- Input email atau username.
- Input kata sandi.
- Kontrol tampilkan/sembunyikan kata sandi.
- Tombol masuk.
- Tautan registrasi.
- Pesan validasi dan status login.

### Mobile Composition

- Gunakan satu kolom.
- Area identitas dipadatkan.
- Form menjadi prioritas utama.
- Hindari panel branding yang terlalu tinggi.
- Pastikan tombol masuk mudah dijangkau.
- Jangan mengorbankan label atau feedback demi menghemat ruang.

### Login Accessibility Requirements

- Gunakan landmark `<main>`.
- Gunakan satu heading utama `<h1>`.
- Setiap input memiliki label yang terlihat.
- Toggle password menggunakan button yang aksesibel.
- Error field dihubungkan dengan input.
- Status login dapat diumumkan kepada screen reader.
- Semua interaksi mendukung keyboard.
- Fokus terlihat jelas.
- Area sentuh cukup besar.
- Jangan menampilkan fitur lupa kata sandi sebagai tautan aktif jika belum memiliki fungsi.

### Functional Preservation

Implementasi login di masa mendatang wajib mempertahankan:

- ID form dan input yang dipakai JavaScript.
- Payload `identifier` dan `password`.
- Endpoint API yang sudah bekerja di localhost.
- Penyimpanan `authToken` dan `currentUser`.
- Redirect ke dashboard.
- Validasi dan feedback login.
- Alur registrasi yang sudah ada.

Tidak boleh mengubah kontrak autentikasi hanya untuk kebutuhan visual.

---

## 8. Dashboard Direction

### Design Objective

Dashboard harus membantu pengguna melakukan tugas utama TrashGu, bukan hanya menampilkan statistik.

### Primary Principle

**Task-first, not stats-first.**

### Information Hierarchy

1. Aksi utama: Klasifikasi Baru.
2. Ringkasan hasil atau aktivitas yang relevan.
3. Riwayat klasifikasi.
4. Statistik dan visualisasi data yang membantu pemahaman.

### Dashboard Rules

- Hindari empat kartu statistik identik tanpa hierarki.
- Gunakan warna kategori secara konsisten.
- Pertahankan navigasi yang jelas.
- Pastikan menu sidebar dapat digunakan dengan keyboard.
- Modal harus memiliki pengelolaan fokus yang benar.
- Tampilkan loading, empty, error, dan success state.
- Gunakan chart hanya jika memberikan informasi yang berguna.
- Jangan mengandalkan thumbnail yang mungkin tidak tersedia di backend.

### Scope

Redesign dashboard dilakukan pada fase terpisah setelah halaman login selesai dan disetujui.

---

## 9. Components and Interaction

### Buttons

- Primary action harus mudah dikenali.
- Secondary action tidak boleh bersaing secara visual.
- Tombol disabled dan loading harus jelas.
- Setiap tombol harus memiliki perilaku nyata.
- Icon-only button membutuhkan accessible name.

### Forms

- Label selalu terlihat.
- Placeholder bukan pengganti label.
- Error disampaikan dengan jelas.
- Field yang invalid memiliki penjelasan yang sesuai.
- Jangan menghapus data input ketika validasi gagal tanpa alasan.

### Navigation

- State aktif terlihat jelas.
- Fokus keyboard terlihat.
- Menu yang dapat dibuka harus memiliki state aksesibilitas.
- Jangan menggunakan elemen noninteraktif sebagai pengganti tombol.

### Feedback

Setiap alur penting mempertimbangkan:

- Loading.
- Success.
- Error.
- Empty state.
- Recovery action.

---

## 10. Motion and Animation

Motion harus membantu pemahaman pengguna.

### Allowed

- Feedback hover dan focus.
- Transisi panel yang ringan.
- Indikator loading.
- Perubahan state yang memperjelas interaksi.

### Avoid

- Animasi dekoratif tanpa tujuan.
- Efek bergerak terus-menerus.
- Transisi panjang yang memperlambat penggunaan.
- Motion yang mengganggu input atau navigasi.

Hormati `prefers-reduced-motion`.

---

## 11. Responsive and Accessibility Quality Gates

Setiap implementasi UI harus diperiksa pada:

- Mobile sempit.
- Mobile umum.
- Tablet.
- Small laptop.
- Desktop.
- Zoom browser 200%.

### Accessibility Checklist

- Keyboard-only navigation.
- Visible focus indicators.
- Accessible names.
- Contrast.
- Semantic landmarks.
- Form labels.
- Error announcements.
- Touch targets.
- Reduced motion.
- Modal focus management jika ada.

### Functional States

Verifikasi:

- Loading.
- Success.
- Error.
- Empty state.
- Kegagalan jaringan.
- Input tidak valid.

Pengujian harus berdasarkan perilaku aktual di browser ketika implementasi telah disetujui.

---

## 12. Technical Constraints

TrashGu menggunakan:

- HTML.
- Tailwind CSS.
- JavaScript.
- Webpack.
- Flask backend.

### Constraints

- Prioritaskan teknologi yang sudah tersedia.
- Jangan mengganti framework frontend tanpa persetujuan.
- Jangan menambah dependency tanpa alasan dan persetujuan.
- Jangan mengubah endpoint API untuk kepentingan desain.
- Jangan mengubah autentikasi yang sudah bekerja.
- Jangan mengubah database atau model ML.
- Jangan mengubah Git history tanpa persetujuan.

### Existing Functionality

Pertahankan seluruh alur yang sudah berhasil:

- Registrasi.
- Login.
- Dashboard.
- Upload gambar.
- Tampilan hasil klasifikasi.
- Riwayat pengguna.

Integrasi model ML sungguhan berada di luar scope redesign UI.

---

## 13. Implementation Workflow

Dokumen ini adalah panduan desain, bukan izin otomatis untuk mengubah aplikasi.

`AGENTS.md` tetap menjadi sumber utama Approval Policy.

### Phase 1: Design Foundation

- Instalasi dan verifikasi Anti-Slop.
- Audit UI yang sudah ada.
- Penetapan arah visual.
- Pembuatan DESIGN.md.

### Phase 2: Login Redesign

Hanya setelah approval terpisah:

- Implementasi Split Editorial.
- Perbaikan aksesibilitas login.
- Verifikasi responsivitas.
- Pengujian autentikasi localhost.
- Review visual dan fungsional.

### Phase 3: Dashboard Redesign

Hanya setelah approval terpisah:

- Hierarki task-first.
- Penyempurnaan navigasi.
- Perbaikan aksesibilitas.
- Perbaikan loading, empty, dan error state.
- Pengujian regresi.

### Phase 4: Other Pages

Dilakukan bertahap dengan approval masing-masing.

---

## 14. Design Review Checklist

Sebelum perubahan UI dianggap selesai:

- [ ] Identitas TrashGu terasa jelas.
- [ ] Tindakan utama mudah ditemukan.
- [ ] Layout tidak terasa seperti template generik.
- [ ] Tipografi mudah dibaca.
- [ ] Warna digunakan secara konsisten.
- [ ] Semua kontrol interaktif benar-benar berfungsi.
- [ ] Keyboard navigation bekerja.
- [ ] Focus indicators terlihat.
- [ ] Contrast memenuhi persyaratan.
- [ ] Mobile layout dirancang dengan sengaja.
- [ ] Tidak ada overflow horizontal.
- [ ] Loading, error, dan success state jelas.
- [ ] Tidak ada dependency baru tanpa approval.
- [ ] Autentikasi dan API tetap berfungsi.
- [ ] Tidak ada perubahan di luar scope approval.

---

## 15. Governance

Dokumen ini merupakan baseline desain TrashGu versi 0.1.

Perubahan desain berikutnya harus mengikuti:

1. `AGENTS.md`.
2. `DESIGN.md`.
3. Empat skill Anti-Slop yang terpasang.
4. Persetujuan eksplisit pengguna untuk perubahan yang diperlukan.

Jika terjadi konflik, aturan keselamatan dan approval dalam `AGENTS.md` memiliki prioritas tertinggi.

Dokumen ini tidak memberikan izin untuk mengubah source code, database, model ML, dependency, atau Git history.
