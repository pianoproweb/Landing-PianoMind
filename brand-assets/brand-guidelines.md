Brand assets
Logo: brand-assets/logo.png
Brand guidelines: brand-assets/brand-guidelines.md
Controlla SEMPRE la cartella brand-assets prima di iniziare qualsiasi
lavoro di design. Usa logo e colori esattamente come specificato.

Palette colori
Sfondo primario:   #080D1A  (quasi nero — sfondo principale)
Sfondo secondario: #0F1829  (blu notte — sezioni alternate)
Accento:           #E8E0D0  (avorio caldo — CTA, highlights, dettagli premium)
Blu notte:         #1B3A6B  (elementi secondari, bordi sottili)
Testo primario:    #F5F0E8  (bianco caldo — tutti i testi principali)
Testo secondario:  #8A95A8  (grigio bluastro — sottotitoli, caption, note)
Regola colori: usa #E8E0D0 con parsimonia — solo su CTA principale,
titoli hero e 2-3 elementi di massima enfasi. Non distribuirlo ovunque.

Tipografia
Titoli display: Playfair Display (serif — elegante, autorevole, accademico)
Titoli sezione: Playfair Display italic per variazione espressiva
Body text:      DM Sans (leggibile, moderno, non generico)
Caption/label:  DM Sans Light o DM Mono per dati e citazioni scientifiche
Fonte:          Google Fonts
VIETATO usare Inter, Arial, Roboto, System fonts per qualsiasi titolo.
Mai più di 3 font nel progetto.
Gerarchia: Playfair Display per titoli H1/H2, DM Sans per H3 e body.

Stile visivo
Tema:        Dark (sfondo quasi nero obbligatorio)
Estetica:    Editoriale premium — come una rivista scientifica di lusso
Registro:    Autorevole, caldo, diagnostico. Mai promesse magiche.
Mai "scopri il segreto". Mai "trasforma la tua vita in 7 giorni".
Ispirazione: Masterclass.com (estetica), Tonebase.co (struttura),
Stripe.com (qualità tecnica animazioni)
Mood:        Un maestro che conosce la materia meglio di chiunque altro
e te lo dimostra con i dati, non con le promesse.

Stack tecnologico obbligatorio

Tailwind CSS per tutto lo styling
ShadCN UI per i componenti (bottoni, card, accordion, form)
GSAP + ScrollTrigger per animazioni di scroll
Framer Motion per micro-interazioni (hover, click, transizioni)
Google Fonts per la tipografia
Puppeteer per screenshot loop durante la build
(DISABILITA lo screenshot loop quando lavori su animazioni e background
animati — scrivi esplicitamente "non usare screenshot loop per questa
modifica" nel prompt)


File di riferimento tecnico
Leggi SEMPRE prima di lavorare al design:
→ references/tecniche-design.md
Contiene: stack dettagliato, regole animazioni GSAP/Framer Motion,
tipografia Google Fonts, setup Puppeteer, tecniche background e profondità,
componenti da 21st.dev, regole anti-AI slop complete.

Regole obbligatorie di design

Sfondi sempre con profondità — gradienti radiali con 2-3 cerchi sfocati
(colori del brand, opacità 10-15%), texture grana leggera sovrapposta.
MAI sfondi piatti monocromatici.
Layout asimmetrico — evita griglie simmetriche a 3 colonne con icone
identiche. Usa sovrapposizioni, offset, elementi che rompono la griglia.
Animazioni con scopo — fade-in dal basso allo scroll (GSAP), stagger
0.15s tra elementi di griglia, counter per numeri/statistiche.
Hover su card e bottoni con scale 1.02 (Framer Motion, 300ms).
Tipografia come elemento di design — variazioni di peso, dimensione e
stile (italic Playfair) devono creare ritmo visivo, non uniformità.
CTA principale — testo: "Get the Course" o simile, colore #E8E0D0,
hover con alone luminoso sottile, sempre visibile above the fold.
Social proof — mostra sempre: 1.000+ pianisti, rating 4.8/5, Amazon
Bestseller. Questi elementi costruiscono fiducia con il target scettico.
Citazioni scientifiche — referenze a Ericsson, neuroscienze, biomeccanica
devono essere visivamente distinte (font mono o serif italic, bordo
sinistro sottile in #E8E0D0).


Struttura landing page — sezioni in ordine

HERO
Headline: promessa trasformativa basata su dati scientifici
Subheadline: chi è Michelangelo Salamone, credenziali
CTA primaria above the fold
Elemento visivo: copertina videocorso o immagine premium
PROBLEMA
Il dolore specifico: ore di studio senza progresso reale
Tono diagnostico, non consolatorio
Dati e ricerche a supporto (Ericsson, studi sul deliberate practice)
SOLUZIONE — IL METODO
Biomeccanica, neuroscienze, psicologia applicata al pianoforte
Come PianoPro è diverso dalla didattica tradizionale
Struttura visiva: 3-4 pilastri con icone essenziali
CONTENUTI DEL CORSO
Cosa trovi dentro — moduli, ore, formato
Lista visiva con gerarchia chiara
Bonus inclusi con valore percepito
AUTORITÀ
Michelangelo Salamone: pianista concertista, autore, metodista
Amazon Bestseller Piano Virtuoso
Citazioni da pianisti reali (testimonianze brevi e specifiche)
Foto professionale
TESTIMONIANZE
Social proof qualitativo — risultati concreti, non generici
Formato: nome, livello pianistico, risultato ottenuto
CTA FINALE
Prezzo, eventuale garanzia, bottone acquisto
Urgency se applicabile (countdown, posti limitati)
Ripetizione dei 3 elementi di fiducia principali


Divieti assoluti

Gradiente viola su sfondo bianco
Font Inter, Arial, Roboto, system fonts per i titoli
Layout simmetrico a 3 colonne con icone identiche in cerchio
Card tutte uguali senza variazione visiva
Sfondo piatto monocromatico
Animazioni decorative senza scopo funzionale
Linguaggio da "corso magico": "scopri il segreto", "trasforma la tua
vita", "metodo rivoluzionario", "risultati garantiti in X giorni"
Colori al di fuori della palette definita senza approvazione esplicita
Più di 3 font diversi nello stesso progetto


Note aggiornate nel tempo
Aggiungi qui ogni regola nuova che scopri funzionare nel progetto.
Esempio: "Le card dei moduli funzionano meglio con bordo sinistro
in #E8E0D0 spessore 2px invece del bordo completo."# Brand Guidelines
