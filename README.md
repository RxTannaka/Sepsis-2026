# Sepsis Manager v2026

Alat bantu klinis berbasis web untuk skrining, manajemen, dan pengambilan keputusan pada pasien dengan dugaan sepsis. Dirancang sebagai *single-page app* ringan tanpa backend, dapat dijalankan langsung dari browser atau di-host sebagai file statis.

## Fitur Utama

| Modul | Deskripsi |
|-------|-----------|
| **Skrining NEWS2** | Kalkulator skor *National Early Warning Score 2* (RR, SpO₂, suplemen oksigen, TD sistolik, nadi, kesadaran ACVPU, suhu) dengan klasifikasi risiko Rendah / Sedang / Tinggi dan rekomendasi tindakan. |
| **Bundle 1 & 6 Jam** | Checklist resusitasi awal (laktat, kultur, antibiotik, cairan 30 mL/kg) dan target re-evaluasi 6 jam (laktat clearance, MAP, urine output, CRT). |
| **Kriteria ICU** | Evaluasi indikasi transfer ICU berdasarkan kriteria mayor (1) dan minor (≥3). |
| **Etiologi & Kultur** | Checklist antimikroba pertama, sumber spesimen kultur, dan visualisasi distribusi sumber sepsis (epidemiologi). |

## Teknologi

- **HTML5** — single file, tanpa build step
- **Tailwind CSS** via Play CDN (`cdn.tailwindcss.com`)
- **Google Fonts** — Inter
- **Vanilla JavaScript** — logika skoring & interaksi tab

## Cara Menjalankan

### Lokal
```bash
# cukup buka file di browser
open index.html
```

### Lewat server statis (opsional)
```bash
python3 -m http.server 8000
# buka http://localhost:8000
```

### Deploy
File statis, bisa di-host di GitHub Pages, Netlify, Vercel, Cloudflare Pages, atau shared hosting apa pun.

## Struktur

```
Sepsis-2026/
├── index.html       # seluruh aplikasi (UI + logika)
└── README.md
```

## Aksesibilitas & UX

- Target sentuh minimum 44×44px pada semua kontrol
- Tipografi minimum 12px (`text-xs`), body 16px
- `aria-label`, `role="tablist"`, `role="progressbar"` pada elemen interaktif
- Respek `prefers-reduced-motion`
- Safe-area inset untuk perangkat dengan gesture bar
- Ikon SVG (bukan emoji) pada navigasi

## Disclaimer

Aplikasi ini merupakan **alat bantu edukasi dan pengingat klinis**, bukan pengganti penilaian klinis. Keputusan akhir tatalaksana pasien tetap menjadi tanggung jawab dokter yang merawat. Selalu ikuti protokol lokal rumah sakit dan pedoman terkini (Surviving Sepsis Campaign, NEWS2 RCP, dsb.).

## Referensi

- Surviving Sepsis Campaign Guidelines (SCCM/ESICM)
- Royal College of Physicians — NEWS2
- Pedoman Nasional Pelayanan Kedokteran (PNPK) Sepsis

## Lisensi

Untuk penggunaan klinis/edukasi. Sesuaikan dengan kebijakan institusi.
