# Tecniche di design per Claude Code — PianoPro Landing Page

Questo file contiene le istruzioni tecniche per costruire interfacce web
professionali. Claude Code legge questo file automaticamente e applica
queste regole su ogni sessione di lavoro al design della landing page.

---

## Stack tecnologico

### Tailwind CSS — styling utility-first
Usa Tailwind CSS per tutto lo styling. Produce codice più pulito e veloce
del CSS custom. Definisci i colori del brand nella configurazione di Tailwind:

```js
colors: {
  'bg-primary':   '#080D1A',
  'bg-secondary': '#0F1829',
  'accent':       '#E8E0D0',
  'blue-night':   '#1B3A6B',
  'text-primary': '#F5F0E8',
  'text-muted':   '#8A95A8',
}
```

### ShadCN UI — componenti riutilizzabili
Per componenti di interfaccia (bottoni, card, accordion, form, dropdown)
usa ShadCN UI. Copia i componenti direttamente nel progetto e personalizzali
con i colori del brand PianoPro.

### Quando usarli
- Progetto con più sezioni e componenti ripetuti: Tailwind + ShadCN come base
- Qualsiasi componente interattivo (accordion FAQ, form, bottoni): ShadCN
- CSS custom solo per effetti molto specifici non coperti da Tailwind

---

## Animazioni

### GSAP + ScrollTrigger — animazioni di scroll
Usa GSAP per tutte le animazioni attivate dallo scroll:
- Elementi che appaiono con fade-in dal basso quando entrano nel viewport
- Stagger di 0.15–0.2s tra elementi di una griglia
- Counter animation per numeri e statistiche (es. "1.000+ pianisti" conta
  da 0 al valore finale quando la sezione entra nello schermo)
- Parallax leggero su elementi decorativi di sfondo

CDN:
https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js
https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js

### Framer Motion — micro-interazioni
Usa Framer Motion per:
- Hover effects su card e bottoni (scale 1.02–1.03, durata 300ms)
- Feedback visivo al click su CTA
- Transizioni fluide tra stati
- Toggle e switch animati

### Regola importante sulle animazioni
Quando lavori su animazioni (background animati, elementi in movimento),
NON usare lo screenshot loop per confrontare. Gli screenshot catturano un
frame statico e il loop impazzisce cercando di "correggere" qualcosa che
funziona perfettamente.
→ Quando aggiungi animazioni scrivi sempre: "Non usare screenshot loop
  per questa modifica."

## Grafica 3D

###Three.js
Per grafiche 3D custom (particelle, geometrie, effetti tipo Stripe.com), CDN: https://cdnjs.cloudflare.com/ajax/libs/three.js/rl128/three.min.js

###Spline (spline.design)
Per grafiche 3D precostruite dalla community. Workflow:
1. Spline.design → community → trova grafica
2. Remix → modifica → Export → Code export
3. Incolla il link nel prompt

## Tipografia

Usa Google Fonts. Regole fisse per PianoPro:
- Titoli H1/H2: Playfair Display (serif, elegante, autorevole)
- Titoli H2 con variazione: Playfair Display italic
- Body e H3: DM Sans (leggibile, moderno)
- Caption, dati, citazioni scientifiche: DM Mono (distingue i riferimenti
  accademici dal testo normale)
- MAI usare Inter, Arial, Roboto, system fonts per i titoli
- Massimo 3 font per progetto (Playfair Display + DM Sans + DM Mono)

Gerarchia dimensioni consigliata:
- H1 hero: 64–80px
- H2 sezione: 40–52px
- H3 sottosezione: 24–28px
- Body: 16–18px, line-height 1.7
- Caption/label: 13–14px

---

## Puppeteer e screenshot loop

Usa Puppeteer per scattare screenshot durante la costruzione del sito.
Dopo ogni fase importante:
1. Avvia il server locale
2. Scatta screenshot delle sezioni modificate
3. Confronta con il risultato desiderato
4. Fai almeno due passate di revisione e correzione prima di mostrare
   il risultato

Installazione: npm install -g puppeteer

ATTENZIONE: disabilita lo screenshot loop esplicitamente ogni volta che
lavori su background animati, gradienti in movimento o qualsiasi elemento
con animazione CSS/JS. Scrivi nel prompt: "Non usare screenshot loop per
questa modifica. Lavora direttamente sul codice e poi mostrami il risultato."

---

## Background e profondità

Non usare MAI sfondi piatti e solidi. Aggiungi sempre profondità visiva:

### Gradienti radiali
2–3 cerchi sfocati con i colori del brand (opacità 10–15%), posizionati
asimmetricamente. Effetto: lampade colorate dietro un vetro smerigliato.

Prompt esempio:
"Aggiungi un background con gradienti radiali. Usa 2–3 cerchi sfocati con
i colori #1B3A6B e #E8E0D0, opacità 10–12%, posizionati asimmetricamente.
Effetto sottile, non deve distrarre dal contenuto."

### Texture grana
Leggerissimo effetto rumore sovrapposto al background (mix-blend-mode
overlay, opacità bassa). Dà al sito una sensazione più tattile e reale —
la differenza tra una foto digitale perfetta e una su pellicola.

Prompt esempio:
"Aggiungi una texture grana leggerissima sovrapposta al background con
mix-blend-mode overlay e opacità 3–5%. Deve essere appena percepibile."

---

## Citazioni scientifiche

Il target di PianoPro risponde all'autorità accademica. Le citazioni
scientifiche (Ericsson, neuroscienze, biomeccanica) devono essere
visivamente distinte dal body text:
- Font: DM Mono o Playfair Display italic
- Bordo sinistro sottile 2px in #E8E0D0
- Padding left 16–20px
- Testo secondario #8A95A8, dimensione leggermente ridotta

---

## Componenti da 21st.dev

Per upgrade puntuali (bottoni animati, background con particelle, hover
effects), cerca componenti su 21st.dev. Ogni componente ha un pulsante
"Copy Prompt" — incollalo direttamente a Claude Code:

"Integra questo componente nella sezione [nome sezione] del sito:
[codice copiato da 21st.dev]"

Claude Code lo adatta ai colori e al layout del progetto automaticamente.

---

## Cloning di siti di riferimento

Quando usi uno screenshot di un sito di riferimento come ispirazione:
1. Usa lo screenshot come guida visiva per layout e proporzioni
2. Replica la struttura con i colori e il brand PianoPro
3. Usa lo screenshot loop (se Puppeteer è attivo) per confrontare
   sezione per sezione
4. Non copiare mai testi o elementi grafici — solo la struttura

Riferimenti per ispirazione:
- Masterclass.com — estetica dark premium
- Tonebase.co — struttura landing corsi musicali
- Stripe.com — qualità animazioni e profondità visiva
- Dribbble / Godly Website / Awwwards — ispirazione componenti

---

## Regole anti-AI slop — EVITA SEMPRE

- Font generici (Inter, Arial, Roboto) per i titoli
- Gradiente viola su sfondo bianco
- Layout simmetrico con 3 colonne e icone identiche in cerchio
- Card tutte uguali senza variazione visiva
- Zero animazioni o interazioni
- Sfondi piatti monocromatici
- Bottone CTA generico senza hover effect
- Linguaggio da "corso magico": segreto, trasforma, rivoluzionario

## Cerca SEMPRE

- Tipografia distintiva con gerarchia visiva forte (Playfair + DM Sans)
- Layout asimmetrico con elementi che rompono la griglia
- Animazioni con scopo (fade-in scroll, counter statistiche, hover card)
- Profondità visiva (gradienti radiali, texture grana, ombre sottili)
- Micro-interazioni su ogni elemento interattivo
- Citazioni scientifiche visivamente distinte
- Social proof (1.000+ pianisti, 4.8/5, Amazon Bestseller) sempre visibile# Tecniche di Design
