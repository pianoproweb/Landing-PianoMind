# Vimeo Setup — PianoMind Course Player

## 1. Piano richiesto

Il player Vimeo incorporato mostra un overlay "Sign in to Vimeo" su account **Free**.  
Per sopprimerlo completamente è necessario un piano **Vimeo Plus** (o superiore).

**Alternativa:** migrare a Bunny Stream — cambia `VIDEO_PROVIDER = 'bunny'` in `course/index.html` e inserisci i valori `libraryId` e `videoId` nel campo `bunny` di ogni entry in `videoConfig`.

---

## 2. Privacy — impostazione obbligatoria per ogni video

1. Vai su **vimeo.com** → apri il video
2. Seleziona **Settings → Privacy**
3. In "Who can watch this video" scegli **"Hide from Vimeo.com"**  
   *(richiede Vimeo Plus o superiore)*
4. Lascia "Where can this be embedded" su **"Specific domains"**

---

## 3. Domini autorizzati per l'embed

Per ogni video, in **Settings → Embed → Privacy → Where can this be embedded**, aggiungi:

```
pianopro.it
pianomind.pianopro.it
localhost
127.0.0.1
```

Senza questa configurazione il player non si avvia su domini non autorizzati.

---

## 4. Parametri URL già configurati nel player

Il player in `course/index.html` usa i seguenti parametri nell'URL dell'iframe:

| Parametro     | Valore | Effetto                                     |
|---------------|--------|---------------------------------------------|
| `title`       | `0`    | Nasconde il titolo del video                |
| `byline`      | `0`    | Nasconde il nome dell'autore Vimeo          |
| `portrait`    | `0`    | Nasconde l'avatar Vimeo                     |
| `dnt`         | `1`    | Do Not Track — disabilita cookie Vimeo      |
| `transparent` | `0`    | Background opaco (evita artefatti visivi)   |
| `app_id`      | `58479`| Identificativo app per le API Vimeo         |

---

## 5. Attributi iframe già configurati

```html
allow="autoplay; fullscreen; picture-in-picture; encrypted-media"
referrerpolicy="strict-origin-when-cross-origin"
```

---

## 6. Vimeo ID da inserire

Apri `videoConfig` in `course/index.html` e sostituisci `VIMEO_ID_PLACEHOLDER` con gli ID reali:

| Lezione | Titolo                              | Vimeo ID attuale   |
|---------|-------------------------------------|--------------------|
| 1.1     | Cultivating the Zone                | `1190747389` ✓     |
| 1.2     | ACT and Psychological Flexibility   | `1190747443` ✓     |
| 1.3     | Self-talk Strategies                | `1190747481` ✓     |
| 1.4     | Imagery and Exposure Therapy        | da inserire        |
| 1.5     | Career Alignment with Values        | da inserire        |
| 2.1     | State-dependent Learning            | `1190747511` ✓     |
| 2.2     | Memory Encoding and Retrieval       | `1190747591` ✓     |
| 2.3     | Autonomic Nervous System Control    | `1190747621` ✓     |
| 3.1     | Force Distribution Efficiency       | da inserire        |
| 3.2     | Injury Prevention Protocols         | da inserire        |
| 3.3     | Movement Economy Analysis           | da inserire        |
| 4.1     | Complex Passage Diagnostic Protocol | da inserire        |
| 4.2     | Context-Independent Practice        | da inserire        |
| 4.3     | Performance Simulation Techniques   | da inserire        |

---

## 7. Riepilogo: se il login overlay persiste

| Situazione                           | Soluzione                                          |
|--------------------------------------|----------------------------------------------------|
| Account Vimeo Free                   | Aggiornare a Vimeo Plus o migrare a Bunny Stream   |
| Video non impostato su "Hide"        | Cambiare Privacy → "Hide from Vimeo.com"           |
| Dominio non in whitelist             | Aggiungere il dominio in Embed → Specific domains  |
| Vimeo Plus attivo ma overlay persiste | Verificare che tutti e 3 i punti sopra siano ok   |
