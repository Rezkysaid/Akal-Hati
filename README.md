# Sesi. (Akal-Hati)

Ruang untuk meluah — web app PWA "terapi diri" yang simulasi seorang therapist duduk semeja. Bina dengan HTML/CSS/JS tulen (satu `index.html`), boleh terus dihoskan di GitHub Pages.

## Fitur (MVP)

- **Sesi Meja** — chat dengan AI therapist (Deepseek API), personality konsisten, framework CBT/ACT, natural dalam Melayu rojak
- **Teknik On-Demand** — Box Breathing (guided animation) & Grounding 5-4-3-2-1
- **Crisis Detection Layer** — detect tanda distress akut di client-side dan terus paparkan talian bantuan sebenar Malaysia (Talian HEAL 15555, Befrienders KL, Talian Kasih, 999)
- **PWA** — boleh install ke home screen, app shell berfungsi offline
- **Privasi** — semua data (API key, perbualan) disimpan dalam browser pengguna sahaja (localStorage)

## Cara guna

1. Enable GitHub Pages: **Settings → Pages → Deploy from branch** → pilih branch & root
2. Buka URL Pages tu, tekan ikon ⚙ dan masukkan Deepseek API key kau sendiri (dapatkan di [platform.deepseek.com](https://platform.deepseek.com))
3. Mula meluah

> **Nota fasa test (BYOK):** Buat masa ni API key dimasukkan oleh pengguna sendiri dan disimpan dalam browser dia sahaja — tiada key dalam code. Untuk production sebenar, panggilan API patut diproksi melalui backend supaya key dan system prompt kekal server-side (rujuk SESICONTEXT).

## Fail

| Fail | Fungsi |
|---|---|
| `index.html` | Keseluruhan app (UI + logic + system prompt) |
| `manifest.webmanifest` | Konfigurasi PWA |
| `sw.js` | Service worker (cache app shell, network-first) |
| `icon-192.png`, `icon-512.png` | Ikon app |

## Batasan yang sengaja dijaga

- AI **tidak** diagnose, score, atau ramal risiko mental health
- Kes distress akut **tidak** dihandle oleh AI sendirian — sentiasa redirect ke talian bantuan sebenar
- Tiada gamification yang boleh buat pengguna rasa "fail"

Sesi. bukan pengganti professional mental health.
