<div align="center">

# ✨ @neelegirly/downloader

### Soft-glow Media-Downloader für TikTok, Instagram, YouTube, Spotify, SoundCloud, Threads & mehr

[![npm version](https://img.shields.io/npm/v/@neelegirly/downloader?style=for-the-badge&color=ff69b4&logo=npm)](https://www.npmjs.com/package/@neelegirly/downloader)
[![npm downloads](https://img.shields.io/npm/dw/@neelegirly/downloader?style=for-the-badge&color=f472b6&logo=npm)](https://www.npmjs.com/package/@neelegirly/downloader)
[![Node](https://img.shields.io/badge/Node-16%2B-22c55e?style=for-the-badge&logo=node.js)](https://nodejs.org)
[![Scope](https://img.shields.io/badge/Scope-@neelegirly-f9a8d4?style=for-the-badge)](https://www.npmjs.com/package/@neelegirly/downloader)
[![Maintained by Neelegirly](https://img.shields.io/badge/Maintained%20by-Neelegirly-f5bde6?style=for-the-badge)](https://github.com/neelegirly)

**Release `0.1.64`** · Promise-basiert · leichtgewichtig · botfreundlich

</div>

---

## 💖 Warum dieses Paket?

`@neelegirly/downloader` ist ein kleiner, praktischer Wrapper für häufig genutzte Download- und Search-Endpunkte.
Er eignet sich perfekt für Bots, Utilities und kleine Automationen, wenn du Medien oder Suchergebnisse schnell in einer einheitlichen API haben willst.

### Highlights

- 🌸 Ein Paket für viele Plattformen
- ⚡ Promise-basierte, einfache Nutzung
- 🧁 Ideal für Bot-Workflows wie Onimai & Co.
- 🎧 Enthält Download- **und** Search-Helper
- 🫧 Fehler liefern ein konsistentes Antwortobjekt statt harter Crashes

---

## 📦 Installation

```bash
npm install @neelegirly/downloader@0.1.64 --save-exact
```

---

## 🚀 Quickstart

```js
const { instagram, tikdown, alldown, spotifySearch } = require('@neelegirly/downloader')

async function demo() {
  const insta = await instagram('https://www.instagram.com/p/example/')
  console.log('Instagram:', insta)

  const tiktok = await tikdown('https://vm.tiktok.com/example/')
  console.log('TikTok:', tiktok)

  const mixed = await alldown('https://example.com/media-link')
  console.log('AllDown:', mixed)

  const tracks = await spotifySearch('lofi anime', 3)
  console.log('Spotify Search:', tracks)
}

demo().catch(console.error)
```

---

## 🧩 Verfügbare Helper

| Helper | Zweck |
|---|---|
| `ndown(url)` | generischer Download-Endpunkt |
| `instagram(url)` | Instagram-Links auflösen |
| `tikdown(url)` | TikTok-Downloads |
| `ytdown(url)` | YouTube-Downloads |
| `threads(url)` | Threads-Links auflösen |
| `twitterdown(url)` | Twitter/X-Medien laden |
| `fbdown2(url, key)` | Facebook-Downloads |
| `GDLink(url)` | Google-Drive-Dateien auflösen |
| `pintarest(url)` | Pinterest-Downloads |
| `capcut(url)` | CapCut-Links auflösen |
| `likee(url)` | Likee-Downloads |
| `alldown(url)` | universeller Multi-Downloader |
| `spotifySearch(name, limit)` | Spotify-Suche |
| `soundcloudSearch(name, limit)` | SoundCloud-Suche |
| `spotifyDl(url)` | Spotify-Download-Metadaten |
| `soundcloud(url)` | SoundCloud-Download |
| `terabox(url)` | Terabox-Links auflösen |

---

## 🌐 Unterstützte Plattformen

- TikTok
- Instagram
- YouTube
- Threads
- Twitter / X
- Facebook
- Pinterest
- CapCut
- Likee
- Google Drive
- Spotify
- SoundCloud
- Terabox

---

## ⚠️ Verhalten bei Fehlern

Das Paket ist bewusst bot-freundlich gehalten:
Wenn ein Upstream-Endpunkt fehlschlägt, wird ein Objekt wie dieses zurückgegeben, statt direkt einen Fehler zu werfen:

```js
{
  developer: 'MOHAMMAD NAYAN',
  status: false,
  msg: 'Instagram API error'
}
```

Das macht Retry-Logik oder Fallbacks in Bots deutlich entspannter.

---

## 📝 Release Notes `0.1.64`

- README komplett neu gestaltet
- Branding auf `@neelegirly/downloader` bereinigt
- Paket-Metadaten für den frischen Release aufgeräumt
- bereit für den neuen Reinstall-Flow in Onimai und Darkbot

---

## 💫 Support

- npm: [`@neelegirly/downloader`](https://www.npmjs.com/package/@neelegirly/downloader)
- GitHub-Profil: [`@neelegirly`](https://github.com/neelegirly)

<div align="center">

**Stay cute, ship fast, download smarter. 🌸**

</div>
