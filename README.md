# Tugas Web Portofolio WBD

Berikut adalah submisi tugas portofolio pribadi yang dibuat hanya menggunakan Vanilla HTML dan CSS.


## Struktur & Semantik HTML

Pemilihan struktur didasarkan pada prinsip-prinsip berikut:

-   **Pembagian Halaman yang Jelas:** Penggunaan tag semantik HTML5 seperti `<header>`, `<main>`, dan `<section>` digunakan untuk membagi halaman menjadi bagian-bagian logis yang jelas (header untuk navigasi, main untuk konten utama, dan section digunakan untuk membagi setiap topik bahasan).
-   **Navigasi Semantik:** Menu navigasi dibungkus dengan tag `<nav>`, yang secara spesifik memberitahu browser bahwa ini adalah blok navigasi utama. Link `<a>` menggunakan *anchor link* (`#id`) untuk *one-page scroll*.
-   **Struktur Berbasis Komponen:** Layout dibagi menjadi komponen-komponen yang dapat digunakan kembali, seperti `.container` untuk layout dua kolom dan `.project-card` untuk setiap item proyek. Ini membuat CSS lebih modular dan mudah dikelola.
-   **Penggunaan Class dan ID:** `id` digunakan secara spesifik untuk jadi target navigasi (`#overview`, `#profile`, `#projects`), sementara `class` lebih digunakan untuk menerapkan gaya visual, terutama yang dapat digunakan kembali di elemen lain.

Selain dari tag-tag struktural utama tersebut, elemen-elemen HTML lainnya digunakan sesuai dengan fungsi semantik pada umumnya.

## Desain & Interaksi


### Pemilihan Font

-   Font utama yang dipilih adalah **Roboto Mono**. Alasan utamanya adalah untuk memberikan nuansa-nuansa "programmer" karena font ini mengingatkan dengan tampilan di code-editor which sesuai dengan identitas saya (hehe).
-   Karena font ini didapatkan dari Google Fonts, untuk *fallback*, ada **SF Mono** (untuk perangkat Apple) dan **Consolas** (untuk perangkat Windows). 


### Skema Warna

Skema warna dirancang agar memiliki kontras tinggi, bersih, dan profesional, dengan beberapa warna aksen untuk menarik perhatian ke elemen-elemen penting.

-   **Dasar:** Hitam (`#060606`) digunakan pada semua teks dan garis batas sedangkan Putih (`#ffffff`) menjadi warna background. Pemilihan warna sederhana yang sudah pasti kontras diharapkan untuk membuat tampilan yang bersih dan mudah dibaca.
-   **Aksen Primer (Kuning):** Warna kuning cerah (`#F4FD6F`) digunakan sebagai warna utama untuk *call-to-action* dan elemen yang ingin ditonjolkan, seperti label nama dan tombol. Warna ini cukup cerah sehingga pas untuk digunakan sebagai pemberi aksen.
-   **Aksen Sekunder (Biru):** Biru muda (`#B7ECFC`) digunakan untuk elemen-elemen sekunder seperti *tag* keahlian dan kartu proyek, yang butuh di-highlight tapi versi lebih soft karena proporsi penggunaannya lebih banyak dibandingkan akses primer.
-   **Abu-abu Gelap:** Digunakan khusus untuk latar belakang blok kode (`.code-container`) untuk mensimulasikan tema gelap pada *code editor* yang populer.

### Interaksi Mikro (Micro-interactions)

Untuk membuat website terasa lebih hidup dan responsif, ditambahkan beberapa interaksi mikro yang halus menggunakan `transition` dan `:hover` di CSS. Tujuannya untuk memberikan *feedback* visual instan kepada pengguna saat mereka berinteraksi dengan elemen sebagai konfirmasi ke pengguna.
-   **Implementasi:**
    -   **Efek 'keangkat' (`transform: translateY`):** Diimplementasikan pada tombol, kartu proyek, dan label keahlian. Saat di-hover, elemen-elemen ini sedikit terangkat dan muncul bayangan, memberikan kesan tiga dimensi.
    -   **Efek 'membesar' (`transform: scale`):** Diimplementasikan pada ikon sosial media. Saat di-hover, ikon akan sedikit membesar, menandakan bahwa elemen tersebut interaktif.
    -   **Transisi Halus:** Semua perubahan status `:hover` (seperti perubahan warna, garis bawah pada link navbar, dan efek `transform`) diberi `transition` dengan durasi `0.2s` agar perubahannya terlihat mulus.


### Desain Responsif

Berikut beberapa teknik utama yang digunakan untuk mencapai desain web yang responsif adalah:

-   **Viewport Meta Tag:** Menyertakan tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">` di dalam `<head>` HTML. Ini memberitahu browser untuk merender halaman sesuai dengan lebar layar perangkat..

-   **Flexbox Layout:** Hampir seluruh tata letak utama, seperti pembagian dua kolom (`.container`) dan grid kartu proyek (`.projects-container`), dibangun menggunakan Flexbox yang digabung dengan properti seperti `flex-wrap` yang memungkinkan item untuk turun ke baris baru secara alami saat ruang tidak cukup. Selain itu, `flex-direction: column` digunakan di dalam *media query* untuk mengubah layout dari horizontal menjadi vertikal di layar kecil.

-   **Media Queries:** Aturan `@media (max-width: ...)` digunakan sebagai titik trigger kapan desain harus beradaptasi untuk layar yang lebih sempit. Pada breakpoint ini, perubahan yang terjadi adalah:
    -   Kolom yang tadinya 50% diubah menjadi 100% agar mengisi layar.
    -   Tinggi section yang tadinya dipatok setinggi layar (`calc(100vh - ...)`) diubah menjadi `auto`.
    -   Ukuran font dan padding disesuaikan agar tidak terlalu besar di layar kecil.

-   **Unit Fleksibel:** Penggunaan unit relatif seperti `%` untuk lebar, dan `vh` untuk tinggi section awal membantu elemen-elemen untuk menyesuaikan ukurannya secara proporsional terhadap layar.

-   **Best Practice CSS:** Penggunaan `box-sizing: border-box;` secara global menyederhanakan kalkulasi layout, memastikan  `padding` dan `border` tidak merusak dimensi elemen yang sudah ditentukan.

## Author

-   **Nama:** Noumisyifa Nabila Nareswari
-   **NIM:** 13523058