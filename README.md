<div align="center">

# QmrPad

**Veggpanel for bad og kjøkken**
Huawei MediaPad T3 10 · Fully Kiosk Browser · én HTML-fil

</div>

---

## Om

QmrPad er et lett, selvbygd veggpanel som erstatter tunge apper på et eldre nettbrett. Alt kjører fra én lokal `panel.html` i Fully Kiosk, med blått badetema og eget thai-tema.

| Flis | Innhold |
|---|---|
| Kalender | Klokke, dato og påminnelser per dag |
| Vær | Yr for Dønfoss bru, med langtidsvarsel og nedbør neste time |
| Lytt | Gemini-stemmestyring på norsk og thai, timer og sanggjenkjenning |
| Radio | Fire favorittkanaler og søk i Radio Browser |
| YouTube | Søk og spillelister, avspilling direkte i panelet |

## Denne repoen

Repoen inneholder bare hjelpesiden `yt.html`. YouTube avviser innbygde videoer fra en lokal fil, så panelet laster spilleren via denne https-siden i stedet.

```
https://qeamer.github.io/QmrPad/yt.html#VIDEO_ID
```

`panel.html` ligger ikke her, fordi den inneholder API-nøkler.

## Oppsett

1. Legg `panel.html` i `/sdcard/panel/` på nettbrettet.
2. Sett Start URL i Fully til `file:///sdcard/panel/panel.html`.
3. Slå på i Fully:
   - Web Content Settings: *Microphone Access*, *Autoplay Videos*, *Read File Access*
   - Advanced Web Settings: *Mixed Content Mode* → Always allow
4. Fyll inn `ytWrap` i `CFG` i `panel.html`:
   ```js
   ytWrap: "https://qeamer.github.io/QmrPad/yt.html",
   ```

## Tjenester

Yr / MET Norway · Gemini API · YouTube Data API · Radio Browser · AudD · Wikipedia · hvakosterstrommen.no
