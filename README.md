# Kuronime Scraper - Node.js Anime Scraper

> **GitHub Repository Title**
>
> ```text
> Kuronime Scraper - Node.js Anime Scraper
> ```
>
> **Repository Name**
>
> ```text
> kuronime-scraper
> ```
>
> **GitHub Repository Description**
>
> ```text
> Node.js CLI scraper for Kuronime. Get homepage content, anime lists, latest episodes, search results, anime details, episode servers, genres, popular anime, ongoing anime, and release schedules in JSON format.
> ```

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-16%2B-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Axios-HTTP%20Client-5A29E4?style=for-the-badge&logo=axios&logoColor=white" alt="Axios">
  <img src="https://img.shields.io/badge/Cheerio-HTML%20Parser-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Cheerio">
  <img src="https://img.shields.io/badge/Creator-SCRIPETEREN-181717?style=for-the-badge&logo=github&logoColor=white" alt="Creator">
</p>

<p align="center">
  <b>Node.js CLI scraper untuk Kuronime.</b><br>
  Mengambil data homepage, anime series, episode terbaru, detail anime, episode server, pencarian, genre, anime ongoing, popular anime, dan jadwal rilis dalam format JSON.
</p>

---

## Fitur

- Mengambil data halaman utama Kuronime
- Mengambil daftar new episodes
- Mengambil daftar top episodes
- Mengambil daftar new anime series
- Mengambil top anime dari sidebar
- Mengambil daftar anime dengan pagination
- Mengambil daftar series anime
- Mengambil daftar episode anime
- Mencari anime berdasarkan keyword
- Mengambil hasil pencarian series anime
- Mengambil hasil pencarian episode
- Mengambil detail anime atau series
- Mengambil judul anime
- Mengambil poster anime
- Mengambil sinopsis anime
- Mengambil rating anime
- Mengambil genre anime
- Mengambil metadata atau informasi anime
- Mengambil jumlah episode
- Mengambil daftar episode
- Mengambil detail halaman episode
- Mengambil server episode atau mirror video
- Mengambil iframe video yang tersedia
- Mengambil daftar genre
- Mengambil anime ongoing
- Mengambil popular anime
- Mengambil jadwal rilis anime
- Mendukung custom path menggunakan command `list`
- Mendukung URL penuh dan path URL pada beberapa command
- Output JSON yang mudah digunakan untuk API, bot, website, atau aplikasi Node.js

---

## Teknologi

Project ini menggunakan:

- [Node.js](https://nodejs.org/)
- [Axios](https://axios-http.com/)
- [Cheerio](https://cheerio.js.org/)
- Built-in module `https`

---

## Struktur Project

```text
kuronime-scraper/
├── kuronime.js
├── package.json
├── package-lock.json
├── .gitignore
├── README.md
└── LICENSE
```

---

## Instalasi

Clone repository:

```bash
git clone [https://github.com/SCRIPETEREN/kuronime-scraper.git](https://github.com/SCRIPETEREN/kuronime-scraper.git)
```

Masuk ke folder repository:

```bash
cd kuronime-scraper
```

Install semua dependency:

```bash
npm install
```

Jika belum memiliki file `package.json`, install dependency manual:

```bash
npm install axios cheerio
```

Jalankan homepage scraper:

```bash
node kuronime.js home
```

Command tanpa argument juga otomatis menjalankan `home`:

```bash
node kuronime.js
```

---

## package.json

Buat file `package.json` dengan isi berikut:

```json
{
  "name": "kuronime-scraper",
  "version": "1.0.0",
  "description": "Node.js CLI scraper untuk mengambil data anime dan episode dari Kuronime.",
  "main": "kuronime.js",
  "scripts": {
    "start": "node kuronime.js home",
    "home": "node kuronime.js home",
    "anime": "node kuronime.js anime",
    "ongoing": "node kuronime.js ongoing",
    "popular": "node kuronime.js popular",
    "genres": "node kuronime.js genres",
    "jadwal": "node kuronime.js jadwal"
  },
  "keywords": [
    "kuronime",
    "anime",
    "anime-scraper",
    "anime-indonesia",
    "scraper",
    "nodejs",
    "axios",
    "cheerio"
  ],
  "author": "SCRIPETEREN",
  "license": "MIT",
  "dependencies": {
    "axios": "^1.7.9",
    "cheerio": "^1.0.0"
  }
}
```

Setelah membuat file `package.json`, jalankan:

```bash
npm install
```

Menjalankan homepage melalui NPM:

```bash
npm start
```

Contoh command NPM lain:

```bash
npm run anime
```

```bash
npm run ongoing
```

```bash
npm run popular
```

```bash
npm run genres
```

```bash
npm run jadwal
```

---

## Cara Penggunaan

Format dasar:

```bash
node kuronime.js <command> <input>
```

Command yang tersedia:

```text
home
anime [page]
search <query>
detail <slug|url>
episode <url>
genres
ongoing
popular
jadwal
list <path>
```

---

## Daftar Command

| Command | Keterangan | Contoh |
|---|---|---|
| `home` | Mengambil data homepage | `node kuronime.js home` |
| `anime [page]` | Mengambil daftar anime dengan pagination | `node kuronime.js anime 2` |
| `search <query>` | Mencari anime atau episode | `node kuronime.js search "one piece"` |
| `detail <slug>` | Mengambil detail series anime | `node kuronime.js detail one-piece-op` |
| `episode <url>` | Mengambil detail episode dan server | `node kuronime.js episode /nonton-one-piece-episode-1180/` |
| `genres` | Mengambil semua daftar genre anime | `node kuronime.js genres` |
| `ongoing` | Mengambil daftar anime episode ongoing | `node kuronime.js ongoing` |
| `popular` | Mengambil daftar popular anime | `node kuronime.js popular` |
| `jadwal` | Mengambil jadwal rilis anime | `node kuronime.js jadwal` |
| `list <path>` | Mengambil data dari custom path | `node kuronime.js list /anime/?status=&type=&order=latest` |

---

## Homepage

Untuk mengambil semua data dari halaman utama:

```bash
node kuronime.js home
```

Atau:

```bash
node kuronime.js
```

Data yang dapat diperoleh:

- New episodes
- Top episodes
- New anime series
- Top anime dari sidebar
- Rank anime
- Judul anime
- Poster anime
- Genre anime
- Rating anime
- Views episode
- Waktu update episode
- URL dan slug setiap item

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "new_episodes": [
      {
        "title": "One Piece Episode 1180",
        "series": "One Piece",
        "episode": "Episode 1180",
        "type": "TV",
        "url": "[https://kuronime.sbs/nonton-one-piece-episode-1180/](https://kuronime.sbs/nonton-one-piece-episode-1180/)",
        "slug": "nonton-one-piece-episode-1180",
        "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
        "views": 10000,
        "time": "1 jam lalu",
        "rating": 8.9
      }
    ],
    "top_episodes": [],
    "new_series": [],
    "top_anime": [
      {
        "rank": 1,
        "title": "One Piece",
        "url": "[https://kuronime.sbs/anime/one-piece-op/](https://kuronime.sbs/anime/one-piece-op/)",
        "slug": "anime/one-piece-op",
        "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
        "genres": [
          "Action",
          "Adventure",
          "Comedy"
        ]
      }
    ]
  }
}
```

---

## Daftar Anime

Untuk mengambil daftar anime terbaru:

```bash
node kuronime.js anime
```

Untuk mengambil halaman tertentu:

```bash
node kuronime.js anime 2
```

```bash
node kuronime.js anime 3
```

Halaman pertama menggunakan path:

```text
/anime/?status=&type=&order=latest
```

Halaman berikutnya menggunakan format:

```text
/anime/page/<nomor>/?status=&type=&order=latest
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [
      {
        "title": "One Piece",
        "type": "TV",
        "url": "[https://kuronime.sbs/anime/one-piece-op/](https://kuronime.sbs/anime/one-piece-op/)",
        "slug": "anime/one-piece-op",
        "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
        "rating": 8.9,
        "rating_raw": 8.9,
        "status": "Ongoing"
      }
    ],
    "next": "[https://kuronime.sbs/anime/page/2/?status=&type=&order=latest](https://kuronime.sbs/anime/page/2/?status=&type=&order=latest)",
    "total_page": "100"
  }
}
```

---

## Search Anime

Gunakan command `search` untuk mencari anime berdasarkan judul atau keyword.

Format:

```bash
node kuronime.js search "<query>"
```

Contoh:

```bash
node kuronime.js search "one piece"
```

```bash
node kuronime.js search "naruto"
```

```bash
node kuronime.js search "solo leveling"
```

```bash
node kuronime.js search "kimetsu no yaiba"
```

Script dapat menampilkan dua jenis hasil:

- `series` untuk hasil series anime
- `episodes` untuk hasil episode anime

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "query": "one piece",
    "series": [
      {
        "title": "One Piece",
        "type": "TV",
        "url": "[https://kuronime.sbs/anime/one-piece-op/](https://kuronime.sbs/anime/one-piece-op/)",
        "slug": "anime/one-piece-op",
        "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
        "rating": 8.9,
        "rating_raw": 8.9,
        "status": "Ongoing"
      }
    ],
    "episodes": [
      {
        "title": "One Piece Episode 1180",
        "series": "One Piece",
        "episode": "Episode 1180",
        "type": "TV",
        "url": "[https://kuronime.sbs/nonton-one-piece-episode-1180/](https://kuronime.sbs/nonton-one-piece-episode-1180/)",
        "slug": "nonton-one-piece-episode-1180",
        "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
        "views": 10000,
        "time": "1 jam lalu",
        "rating": 8.9
      }
    ]
  }
}
```

---

## Detail Anime

Gunakan command `detail` untuk mengambil informasi lengkap sebuah anime series.

Format:

```bash
node kuronime.js detail <slug>
```

Contoh menggunakan slug:

```bash
node kuronime.js detail one-piece-op
```

Contoh menggunakan path:

```bash
node kuronime.js detail /anime/one-piece-op/
```

Contoh menggunakan URL penuh:

```bash
node kuronime.js detail [https://kuronime.sbs/anime/one-piece-op/](https://kuronime.sbs/anime/one-piece-op/)
```

Data detail yang dapat diperoleh:

- Judul anime
- Slug anime
- URL detail
- Poster
- Sinopsis
- Rating
- Genre
- Informasi atau metadata anime
- Total episode
- Daftar episode
- URL episode
- Slug episode

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "title": "One Piece",
    "slug": "/anime/one-piece-op/",
    "url": "[https://kuronime.sbs/anime/one-piece-op/](https://kuronime.sbs/anime/one-piece-op/)",
    "poster": "[https://example.com/one-piece.jpg](https://example.com/one-piece.jpg)",
    "synopsis": "Cerita tentang Monkey D. Luffy dan petualangannya menjadi Raja Bajak Laut.",
    "rating": 8.9,
    "genres": [
      "Action",
      "Adventure",
      "Comedy",
      "Fantasy"
    ],
    "info": {
      "japanese": "ONE PIECE",
      "type": "TV",
      "status": "Ongoing",
      "premiered": "Fall 1999"
    },
    "total_episodes": 1180,
    "episodes": [
      {
        "title": "One Piece Episode 1180",
        "url": "[https://kuronime.sbs/nonton-one-piece-episode-1180/](https://kuronime.sbs/nonton-one-piece-episode-1180/)",
        "slug": "nonton-one-piece-episode-1180"
      }
    ]
  }
}
```

---

## Detail Episode

Gunakan command `episode` untuk mengambil informasi server dan iframe dari halaman episode.

Format:

```bash
node kuronime.js episode <url_episode>
```

Contoh menggunakan path:

```bash
node kuronime.js episode /nonton-one-piece-episode-1180/
```

Contoh menggunakan URL penuh:

```bash
node kuronime.js episode [https://kuronime.sbs/nonton-one-piece-episode-1180/](https://kuronime.sbs/nonton-one-piece-episode-1180/)
```

Data yang dapat diperoleh:

- Judul episode
- URL episode
- Server atau mirror video
- Value server
- Daftar iframe video

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "title": "One Piece Episode 1180 Subtitle Indonesia",
    "url": "[https://kuronime.sbs/nonton-one-piece-episode-1180/](https://kuronime.sbs/nonton-one-piece-episode-1180/)",
    "servers": [
      {
        "label": "Server 1",
        "value": "[https://example.com/embed/one-piece](https://example.com/embed/one-piece)"
      }
    ],
    "iframes": [
      "[https://example.com/embed/one-piece](https://example.com/embed/one-piece)"
    ]
  }
}
```

---

## Daftar Genre

Untuk mengambil semua genre anime:

```bash
node kuronime.js genres
```

Script mengambil data dari halaman:

```text
[https://kuronime.sbs/genres/](https://kuronime.sbs/genres/)
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": [
    {
      "name": "Action",
      "slug": "action",
      "url": "[https://kuronime.sbs/genres/action/](https://kuronime.sbs/genres/action/)"
    },
    {
      "name": "Adventure",
      "slug": "adventure",
      "url": "[https://kuronime.sbs/genres/adventure/](https://kuronime.sbs/genres/adventure/)"
    }
  ]
}
```

---

## Anime Ongoing

Untuk mengambil daftar anime ongoing:

```bash
node kuronime.js ongoing
```

Halaman sumber:

```text
/ongoing-anime/
```

Output dapat berisi daftar episode atau daftar series, tergantung struktur halaman yang tersedia.

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "heading": "Ongoing Anime",
    "items": [],
    "next": null,
    "total_page": null
  }
}
```

---

## Popular Anime

Untuk mengambil daftar popular anime:

```bash
node kuronime.js popular
```

Halaman sumber:

```text
/popular-anime/
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "heading": "Popular Anime",
    "items": [],
    "next": null,
    "total_page": null
  }
}
```

---

## Jadwal Rilis

Untuk mengambil jadwal rilis anime:

```bash
node kuronime.js jadwal
```

Halaman sumber:

```text
/jadwal-rilis/
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "heading": "Jadwal Rilis",
    "items": [],
    "next": null,
    "total_page": null
  }
}
```

---

## Custom List Path

Gunakan command `list` untuk mengambil data dari path lain yang kompatibel dengan struktur list Kuronime.

Format:

```bash
node kuronime.js list <path>
```

Contoh:

```bash
node kuronime.js list /anime/?status=&type=&order=latest
```

Contoh lain:

```bash
node kuronime.js list /ongoing-anime/
```

```bash
node kuronime.js list /popular-anime/
```

```bash
node kuronime.js list /jadwal-rilis/
```

Script akan mencoba membaca item episode dari selector:

```text
article.bsu
```

Jika tidak menemukan episode, script akan mencoba membaca item anime series dari selector:

```text
article.bs
```

---

## Struktur Response

Semua command sukses menggunakan struktur berikut:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {}
}
```

Jika terjadi error:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Pesan error"
}
```

---

## Mengubah Author Response

Pada source code awal, author response menggunakan `xvlovers`.

Ubah response sukses dari:

```js
console.log(JSON.stringify({
  author: "xvlovers",
  status: true,
  data
}, null, 2))
```

Menjadi:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: true,
  data
}, null, 2))
```

Ubah response error dari:

```js
console.log(JSON.stringify({
  author: "xvlovers",
  status: false,
  message: error.message
}, null, 2))
```

Menjadi:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: false,
  message: error.message
}, null, 2))
```

---

## Error Handling

Script menangani beberapa error berikut:

- Command tidak dikenal
- Query search kosong
- Slug detail anime kosong
- URL episode kosong
- Custom list path kosong
- Request HTTP gagal
- Website memberikan status selain `200`
- Timeout request
- Struktur HTML berubah
- Data anime atau episode tidak tersedia

Contoh search tanpa query:

```bash
node kuronime.js search
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Contoh: node kuronime.js search one piece"
}
```

Contoh detail tanpa slug:

```bash
node kuronime.js detail
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Contoh: node kuronime.js detail one-piece-op"
}
```

Contoh command tidak dikenal:

```bash
node kuronime.js test
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Command tidak dikenal: test
Gunakan: home | anime [page] | search <q> | detail <slug> | episode <url> | genres | ongoing | popular | jadwal | list <path>"
}
```

---

## Penggunaan Sebagai Module

Agar file `kuronime.js` dapat digunakan di project Node.js lain, ubah bagian paling bawah file.

Ganti:

```js
main()
```

Menjadi:

```js
if (require.main === module) {
  main()
}

module.exports = {
  getHome,
  getAnimeList,
  getEpisodeList,
  search,
  getDetail,
  getEpisode,
  getGenreList
}
```

Buat file baru bernama `app.js`:

```js
const {
  getHome,
  getAnimeList,
  search,
  getDetail,
  getEpisode,
  getGenreList
} = require("./kuronime")

async function main() {
  try {
    const home = await getHome()

    console.log(JSON.stringify(home, null, 2))

    const results = await search("one piece")

    console.log(JSON.stringify(results, null, 2))

    const detail = await getDetail("one-piece-op")

    console.log(JSON.stringify(detail, null, 2))

    const episode = await getEpisode("/nonton-one-piece-episode-1180/")

    console.log(JSON.stringify(episode, null, 2))
  } catch (error) {
    console.error(error.message)
  }
}

main()
```

Jalankan:

```bash
node app.js
```

---

## .gitignore

Buat file `.gitignore`:

```gitignore
node_modules/
.env
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.DS_Store
```

---

## Catatan Penting

- Struktur HTML Kuronime dapat berubah kapan saja.
- Jika class HTML, selector, atau struktur halaman berubah, scraper mungkin perlu diperbarui.
- Jangan melakukan request dalam jumlah besar dalam waktu singkat.
- Gunakan cache, delay, queue, dan rate limit apabila scraper digunakan untuk bot atau aplikasi publik.
- Tidak semua halaman episode memiliki server atau iframe yang dapat dibaca oleh selector saat ini.
- Data server dan iframe dapat berubah sesuai sistem video player yang digunakan website.
- Konfigurasi `rejectUnauthorized: false` digunakan untuk mengatasi masalah sertifikat tertentu, tetapi sebaiknya tidak digunakan untuk aplikasi production kecuali benar-benar diperlukan.
- Gunakan project ini untuk pembelajaran web scraping, parsing HTML, riset, dan pengolahan metadata.
- Patuhi ketentuan website sumber, hukum, serta hak cipta yang berlaku.

---

## License

Project ini menggunakan lisensi MIT.

Buat file `LICENSE`:

```text
MIT License

Copyright (c) 2026 SCRIPETEREN

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Creator

```text
SCRIPETEREN
```

```text
[https://github.com/SCRIPETEREN](https://github.com/SCRIPETEREN)
```

---

## Disclaimer

Repository ini dibuat untuk pembelajaran Node.js, HTTP request, HTML parsing, dan pengolahan metadata dari halaman yang tersedia secara publik.

Gunakan script secara bertanggung jawab. Jangan gunakan scraper untuk melakukan request berlebihan, menyebarkan konten tanpa izin, melanggar privasi, atau melakukan aktivitas yang melanggar ketentuan layanan dan hukum yang berlaku.

<p align="center">
  Made by <a href="https://github.com/SCRIPETEREN">SCRIPETEREN</a>
</p>