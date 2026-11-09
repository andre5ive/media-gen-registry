# media-gen-registry

Registro modelli fal.ai usato dallo skill **media-gen**. Lo script `generate.py` legge
`models.json` da qui a ogni avvio (`raw.githubusercontent.com/andre5ive/media-gen-registry/main/models.json`);
se il repo non risponde usa l'ultima copia in cache e poi quella inclusa nello skill.

## Come si aggiorna

Un'attività programmata gira ogni mattina:

1. legge https://fal.ai/explore/recently-added;
2. per ogni modello nuovo di immagini, image-to-video o upscale apre la sua pagina fal e ne
   ricava `fal_id`, parametri, campo di output e prezzo;
3. lo aggiunge come voce **non predefinita** nella sezione giusta;
4. ricontrolla i prezzi più vecchi di 30 giorni;
5. registra tutto in `CHANGELOG.md` e fa commit.

I modelli predefiniti (`default`) non vengono mai cambiati in automatico: le proposte finiscono
nel changelog sotto "Proposte" e si applicano solo dopo un tuo sì.

## Prezzi

Ogni modello ha un blocco `pricing`:

| campo | significato |
| --- | --- |
| `unit` | `image`, `second`, `image_tier` o `tokens` |
| `usd` | prezzo di listino base |
| `by_resolution` | prezzo per risoluzione (`720p`, `1080p`, `4K`…) |
| `verified` | data dell'ultima verifica su fal.ai |

Lo script usa questi valori per stimare `cost_usd` di ogni generazione.
