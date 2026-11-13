# Changelog del registro

## 2026-11-13

Primo controllo di fal.ai/explore/recently-added (pagine 1 e 2, 48 modelli).

### Modelli aggiunti (nessuno è predefinito)

**image**
- `nano-banana-2-1` (google/nano-banana-2.1): ~$0,04 (1K), $0,059 (2K), $0,134 (4K) a immagine, stime fal, fatturazione a token.
- `nano-banana-2-1-edit` (google/nano-banana-2.1/edit): ~$0,044 / $0,063 / $0,138 a immagine (1K/2K/4K).
- `flux-3` (blackforestlabs/flux-3/text-to-image): $0,048 a 1K; 2K/4K non indicati.
- `flux-3-edit` (blackforestlabs/flux-3/edit-image): $0,048 a 1K.
- `minimax-h3-image`, `minimax-h3-image-edit`, `minimax-h3-highspeed`, `minimax-h3-highspeed-edit`: solo prezzo a token, nessun prezzo fisso (`usd: null`).

**video_image_to_video**
- `pixverse-v6-max`: $0,252/s a 1080p con audio ($0,198 senza).
- `vidu-q4`: $0,084/s a 1080p, audio nativo; da $0,0315 (540p) a $0,273 (4K).
- `kandinsky6-pro`: $1,40 a clip 5 s 480p (~$0,28/s).
- `kandinsky6-lite`: $0,17 a clip 5 s 480p (~$0,034/s).
- `grok-imagine-1-5-lite`: $0,03/s a 720p, $0,14/s a 1080p, +$0,01 per immagine.

**upscale_video**
- `ltx-2-5-upscale`: $0,08/s (1080p), $0,30/s (4K), $1,20/s (8K).
- `flashvsr-plus`: $0,0005 per megapixel × frame (`usd: null`, vedi nota).
- `kandinsky6-vsr`, `kandinsky6-vsr-lite`: $0,00036 per megapixel × frame (`usd: null`); parametri non verificati.

### Prezzi ricontrollati (invariati, data aggiornata)
- `seedance-2-fast`: $0,2419/s (720p).
- `kling-v3-pro`: $0,168/s con audio, $0,112 senza; aggiunto voice control $0,196/s.
- `kling-v3-4k`: $0,42/s, uguale con o senza audio.
- `topaz-video`: $0,01 / $0,02 / $0,08 al secondo; aggiunto blocco `pricing`. Gaia 2 costa la metà.

### Non aggiunti
- Seedream 5.5 text-to-image ed edit: pagine fal non leggibili oggi. Lasciati fuori da `seen` per riprovarli domani.

### Scartati per categoria
- 3D: meshy/rigging, meshy/rigging/multi-animation, meshy/t2 (text/image-to-3d), meshy/t2.5 (text/image-to-3d), meshy/relief, meshy/n1/retexture, meshy/v6-lite/retexture, microsoft/moge-3, microsoft/moge-2.
- Audio/testo: mureka podcast, song, instrumental, lyrics, lyrics-video.
- Text-to-video: pixverse/v6/max, kandinsky6-pro, kandinsky6-lite, grok-imagine-video/v1.5/lite.
- Video-to-video: ltx-2.5 hdr, reframe, alpha-gen; minimax h3-max relight, recast, h3-max-turbo extend-video; vidu/q4/reference-to-video.
- Altro: bytedance/seedream/v5.5/layerize (scomposizione in livelli), fal-ai/marigold-v2 (stima di profondità).

### Proposte
Vedi sotto: Nano Banana 2.1 per "image" e Vidu Q4 per "video_image_to_video".

## 2026-11-09 — prima versione

- Aggiunto il blocco `pricing` a ogni modello.
- Nano Banana Pro e Nano Banana Pro Edit: $0,15/immagine (4K il doppio). Il vecchio "~$0,04" era sbagliato.
- Seedance 2.0 Pro: 720p $0,3034/s, 1080p $0,682/s.
- GPT Image 2: prezzo a token, nessun prezzo fisso per immagine.
- Topaz image upscale: $0,08 fino a 24MP, $0,16 fino a 48MP, $0,32 fino a 96MP, $1,36 fino a 512MP.
- Aggiunta la sezione `recently_added` per tenere traccia dei modelli già esaminati.

## Proposte

- **2026-11-13, image: valutare `nano-banana-2-1` come default al posto di `nano-banana-pro`.** È il modello Google più recente, forte sul testo nelle immagini e sui formati larghi, e costa molto meno: ~$0,059 a 2K contro $0,15 (4K: $0,134 contro $0,30). Da provare prima su qualche prompt realistico, perché la qualità fotografica rispetto al Pro non è verificata.
- **2026-11-13, video_image_to_video: valutare `vidu-q4` al posto di `seedance-2-pro`.** Audio nativo, fino a 4K e 16 s, a $0,084/s a 1080p contro $0,682/s (circa 8 volte meno: clip 5 s ~$0,42 contro ~$3,41). Da confrontare sulla qualità del movimento prima di cambiare.
