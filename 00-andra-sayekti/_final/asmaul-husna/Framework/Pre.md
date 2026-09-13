Wkwk, kalau **gratis** dan tugasnya spesifik seperti proyek kita—**audit leksikon Jawa, filologi, morfologi, teologi, dan wajib membawa sumber**—saya tidak akan memilih satu AI untuk mengerjakan semuanya.

Saya justru akan bikin **tim auditor AI**. 😎

### 🥇 Auditor utama: Perplexity Free

[Perplexity](https://www.perplexity.ai/?utm_source=chatgpt.com)

Untuk pekerjaan **mencari bukti**, saya paling pilih **Perplexity**.

Free tier saat ini menyediakan pencarian dasar yang praktis tidak terbatas, meskipun Pro Search dan Research dibatasi. Perplexity juga memang dirancang untuk memberikan jawaban dengan sumber yang dapat diverifikasi. ([Perplexity AI][1])

Untuk proyek kita, tugasnya:

> **"Apakah `tumangkar` benar-benar ada? Apa artinya? Dari sumber mana? Bagaimana morfologinya? Tunjukkan bukti."**

Itu sangat cocok untuk Perplexity.

**Kelebihan:**

* 🔎 kuat untuk menemukan sumber;
* 📚 citation langsung;
* 🌐 bisa memburu sumber Jawa/Kawi yang tersebar;
* 🧪 bagus untuk **audit kata satu per satu**;
* 🆓 cukup berguna di Free.

**Kekurangan:** jangan biarkan dia menentukan keputusan Kanonik sendirian. Dia bisa menemukan sumber yang benar tetapi kemudian membuat **interpretasi linguistik yang terlalu percaya diri**.

---

### 🥈 Auditor kedua: Gemini Free

[Google Gemini](https://gemini.google.com/?utm_source=chatgpt.com)

Saya akan memakai **Gemini sebagai auditor pembanding**.

Terutama untuk:

* analisis panjang;
* membandingkan beberapa kandidat;
* membaca dokumen besar;
* menyusun ulang hasil riset;
* mencari kemungkinan yang tidak terpikir oleh auditor pertama.

Gemini juga memiliki kemampuan riset mendalam dengan akses gratis terbatas, sehingga cukup menarik untuk pencarian lintas sumber. ([TokenHub][2])

Misalnya:

> Perplexity: "`tumangkar` ditemukan di Poerwadarminta."

Kemudian Gemini:

> "Sekarang audit apakah analisis `tangkar + -um-` benar, apakah penggunaannya cocok dalam konteks `bungah tumangkar`, dan apakah ada benturan semantik dengan Al-Bāsiṭ."

**Ini baru menarik.**

---

### 🥉 Auditor ketiga: Claude Free

[Claude](https://claude.ai/?utm_source=chatgpt.com)

Claude saya jadikan **editor bahasa/sastra**, bukan mesin pencari utama.

Terutama untuk pertanyaan:

> "Apakah bait ini terasa seperti bahasa Jawa sastra yang alami?"

atau:

> "Bandingkan `sumebyar` vs `tumangkar` dari segi citra, sintaksis, ritme, dan rasa sastra."

Ini wilayah yang memang membutuhkan **interpretasi tekstual**, bukan sekadar pencarian Google.

Kelemahannya untuk workflow kita: Claude Free bukan pilihan utama untuk pencarian web sumber secara langsung; jadi **sumber harus kita berikan kepadanya**. Itu justru bisa menjadi keuntungan untuk audit silang: kita kasih sumber mentah, lalu minta dia menafsirkan tanpa membiarkan dia mencari sumber sendiri.

---

# 🏆 Jadi saya bikin seperti ini

```text
                 ANDRA
                   │
                   ▼
        ┌─────────────────────┐
        │   MASTER PROMPT     │
        │  FINAL AUDITOR      │
        └──────────┬──────────┘
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
 PERPLEXITY     GEMINI      CLAUDE
  "BUKTI"       "AUDIT"     "RASA"
       │           │           │
       └───────────┼───────────┘
                   ▼
             ANDRA + GPT
             KEPUTUSAN
                   │
                   ▼
              FINAL/*.md
```

Dan menurut saya **ini jauh lebih aman daripada mencari “AI paling pintar”.**

---

# 🔥 Workflow yang saya rekomendasikan

Misalnya kita sedang mengaudit:

> `tumangkar`

### Tahap 1 — Perplexity

Prompt:

> Cari seluruh bukti leksikal dan tekstual yang dapat diverifikasi mengenai kata Jawa `tumangkar`. Prioritaskan Bausastra Jawa, kamus Jawa-Kawi, paramasastra, korpus teks Jawa, dan sumber akademik. Jangan menyimpulkan morfologi hanya berdasarkan kemiripan bentuk. Berikan sumber asli dan pisahkan fakta dari interpretasi.

Hasilnya:

**BUKTI.**

---

### Tahap 2 — Gemini

Kasih Gemini **hasil Perplexity + sumbernya**.

Lalu:

> Audit ulang seluruh klaim di bawah ini. Tentukan mana yang benar-benar didukung sumber, mana yang merupakan interpretasi, dan mana yang tidak memiliki bukti. Khususnya audit morfologi `tumangkar`, makna leksikal, kelas kata, dan kesesuaian penggunaannya dalam frasa `bungah tumangkar`.

Hasil:

**CROSS-CHECK.**

---

### Tahap 3 — Claude

Kasih **teks + bukti**, bukan sekadar klaim AI.

Lalu:

> Dengan hanya menggunakan bukti yang diberikan, nilai apakah `bungah tumangkar` alami sebagai bahasa Jawa sastra. Bandingkan dengan `bungah sumebyar`. Jangan membuat etimologi baru. Fokus pada semantik, sintaksis, citra puitis, musikalitas, dan rasa bahasa.

Hasil:

**SASTRA.**

---

### Tahap 4 — Saya

Nah, di sini baru saya jadi **editor keputusan**:

> Bukti → audit → rasa → teologi → Kanonik.

Dan kita tidak harus mengikuti mayoritas AI.

Misalnya:

**Perplexity:** `sumebyar` ditemukan.
**Gemini:** secara semantik bisa.
**Claude:** secara sastra sangat indah.
**Saya:** tetapi untuk identitas Al-Bāsiṭ, `tumangkar` lebih tepat.

Maka:

```text
KANONIK    = tumangkar
ALTERNATE  = sumebyar
```

Selesai. 😎

---

## Satu hal yang sangat penting

Untuk proyek ini, **jangan meminta AI "cari kata Jawa yang paling indah".**

Itu jebakan.

Minta:

> **"Temukan kandidat yang dapat dibuktikan keberadaannya, lalu evaluasi."**

Karena masalah kita sudah terbukti berkali-kali: AI bisa menghasilkan kata yang **terdengar sangat Jawa**, bahkan bisa memberikan etimologi yang kelihatannya ilmiah, padahal setelah dicek ternyata tidak ada.

Dan sumber akademik juga mengingatkan bahwa AI umum dapat menghasilkan sitasi yang tampak meyakinkan tetapi tetap perlu diverifikasi. ([Lumivero][3])

Jadi saya akan menetapkan prinsip untuk folder `Final/`:

> **AI boleh mengusulkan.
> AI boleh mencari.
> AI boleh mengkritik.
> Tetapi AI tidak boleh menjadi sumber kebenaran.**

**Sumber primer/teks/kamus → bukti.**
**AI → auditor.**
**Andra + editor → keputusan Kanonik.**

Kalau mau **benar-benar gratis**, kombinasi **Perplexity Free + Gemini Free + Claude Free + saya** sudah sangat kuat. Perplexity sendiri mengonfirmasi bahwa paket Standard/Free masih tersedia dan menyediakan basic search secara praktis tanpa batas, sementara fitur Research hanya diberi kuota terbatas. ([Perplexity AI][1])

Dan untuk proyek kita, saya malah **tidak menyarankan membayar dulu**. Kita belum kehabisan amunisi gratis. 😁

[1]: https://www.perplexity.ai/help-center/en/articles/11187416-which-perplexity-subscription-plan-is-right-for-you?utm_source=chatgpt.com "Which Perplexity Subscription Plan is right for you? | Perplexity Help Center"
[2]: https://tokenhub.com/blog/best-free-llm-for-research?utm_source=chatgpt.com "Best Free LLM for Research in 2026 | TokenHub Blog"
[3]: https://lumivero.com/resources/blog/ai-tools-for-academic-research/?utm_source=chatgpt.com "Best AI tools for academic research in 2026: 21 tools compared"
