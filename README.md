# Zampillo - App per le Fontanelle di Milano
![Zampillo](https://img.shields.io/badge/Version-1.0.0-teal)
![React](https://img.shields.io/badge/React-18+-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5+-blue)
![Tailwind](https://img.shields.io/badge/Tailwind-4.0-teal)  

**Progetto universitario** per il corso di **Fondamenti di Human-Computer Interaction** del **Politecnico di Milano**.

Gruppo EcoDevs

Zampillo e' un'applicazione web progressiva (PWA) mobile-first che aiuta i cittadini milanesi a scoprire, utilizzare e prendersi cura delle 719 vedovelle (fontanelle pubbliche) della citta', promuovendo la riduzione del consumo di bottiglie di plastica monouso attraverso un'esperienza social e gamificata.

## Indice

- [Panoramica](#panoramica)
- [Come Usare l'App](#come-usare-lapp)
- [Funzionalita'](#funzionalita)
- [Tecnologie Utilizzate](#tecnologie-utilizzate)
- [Installazione e Setup](#installazione-e-setup)
- [Dataset delle Fontanelle](#dataset-delle-fontanelle)
- [Struttura del Progetto](#struttura-del-progetto)
- [Design e UX](#design-e-ux)
- [Credits](#credits)

## Panoramica

Le vedovelle, o "draghi verdi", sono le iconiche fontanelle in ghisa a testa di drago di Milano, prodotte dalla Fonderia Lamperti dal 1908. Zampillo trasforma la loro scoperta in un'attivita' social e ludica: l'utente esplora la mappa, fa check-in alle fontanelle, guadagna punti e badge, partecipa a chat di quartiere e organizza eventi comunitari.

L'app e' pensata esclusivamente per smartphone in modalita' portrait (verticale) ed e' installabile come PWA dalla Home Screen di Safari/Browser.

## Come Usare l'App

### Primo avvio e Tutorial

Al primo accesso l'app mostra un tutorial guidato in 4 passaggi che spiega le funzionalita' principali:

1. **Benvenuto** - Introduzione all'app e alla sua missione
2. **Trova Fontanelle** - Come usare la mappa per trovare le vedovelle vicine
3. **Check-in e Punti** - Come guadagnare punti facendo check-in
4. **Filtra e Ordina** - Come usare i filtri per trovare fontanelle specifiche

Il tutorial puo' essere saltato e riattivato in qualsiasi momento dalle Impostazioni.

### Navigazione

L'app ha 4 schermate principali accessibili dalla barra di navigazione in basso:

- **Mappa** - Schermata principale con la mappa di tutte le fontanelle
- **Leaderboard** - Classifica delle fontanelle piu' popolari e degli utenti piu' attivi
- **Chat** - Chat di quartiere per la community
- **Profilo** - Dashboard personale con statistiche, badge e sfide

Le **Impostazioni** sono accessibili dall'icona ingranaggio nella barra superiore.

### Flusso tipico di utilizzo

1. Apri l'app e visualizza la mappa con tutte le fontanelle di Milano
2. Cerca una fontanella specifica o usa i filtri (distanza, popolarita', preferiti, accessibilita')
3. Tocca un marker sulla mappa per vedere un'anteprima con distanza e tempo a piedi
4. Premi "Vedi Dettagli" per aprire la scheda completa della fontanella
5. Premi "Indicazioni" per aprire la navigazione Google Maps verso la fontanella
6. Fai check-in alla fontanella per guadagnare punti (+15 punti)
7. Segnala eventuali problemi (fontanella rotta, sporca, danneggiata)
8. Partecipa alle chat di quartiere e agli eventi comunitari

## Funzionalita'

### Mappa Interattiva

- Mappa Google Maps personalizzata con stile a tema acqua/verde
- 719 fontanelle reali dal dataset ufficiale del Comune di Milano
- Marker SVG personalizzati con indicatore di posizione dell'utente
- Barra di ricerca per nome o localita'
- Filtri rapidi per distanza (500m, 1km) e popolarita'
- Pannello filtri avanzati: accessibilita', qualita' dell'acqua, condizione, ciotola per animali
- Filtro preferiti (fontanelle salvate con il cuore)
- Bottom sheet con anteprima della fontanella selezionata
- Navigazione GPS verso la fontanella tramite Google Maps

### Dettaglio Fontanella

- Informazioni complete: condizione, accessibilita', quartiere (NIL), municipio, CAP
- Galleria foto della community (carousel con miniature)
- Statistiche: check-in, contributi, membri chat, trend settimanale
- Qualita' dell'acqua: potabilita' certificata, temperatura, pressione
- Storia della vedovella e anno di installazione
- Eventi in programma nella zona
- Attivita' recente degli utenti
- Servizi disponibili: accesso H24, illuminazione, accessibilita' disabili, QR code
- Azioni rapide: check-in (+15 punti), chat, navigazione, segnalazione problemi

### Segnalazione Problemi

Dialog dedicato per segnalare problemi a una fontanella:

- 6 tipologie: Non Funzionante, Bassa Pressione, Sporca/Non Pulita, Danneggiata, Mancante, Altro
- Campo descrizione opzionale
- Conferma visiva con animazione di successo

### Sistema di Gamification

#### Punti e Livelli

- **Punti Esperienza (XP)**: si accumulano con le attivita' (check-in, contributi, segnalazioni)
- **Livelli**: ogni 200 XP si sale di livello, con barra di progresso visuale
- **Punti Spendibili**: valuta separata dagli XP, utilizzabile nel negozio premi

#### Badge (15 totali in 4 categorie)

- **Esplorazione** (5): dalla "Prima Goccia" (1 check-in) al "Maestro di Milano" (tutte le 719 fontanelle)
- **Sociale** (3): dalla "Farfalla Sociale" (5 chat) al "Leader Community" (top contributor)
- **Ecologico** (3): dal "Guerriero Eco" (100 litri risparmiati) all'"Eroe Verde" (1000 litri)
- **Speciale** (4): dal "Gufo Notturno" (check-in a mezzanotte) all'"Appassionato di Storia" (tutte le fontanelle storiche)

Ogni badge ha una rarita' (comune, raro, epico, leggendario) e un'animazione di sblocco con effetto confetti.

#### Sfide Attive

3 sfide contemporanee con progresso tracciato:

- "Esploratore Settimanale" - Visita 5 vedovelle diverse questa settimana
- "Il Percorso delle Stelle" - Traccia una stella sulla mappa visitando fontanelle
- "Archeologo Urbano" - Scopri le 3 vedovelle piu' antiche di Milano

#### Negozio Premi

- **Funzionalita' sbloccabili** (permanenti): Statistiche Avanzate, Percorsi Idratazione
- **Premi riscattabili** (con punti spendibili): Buono BikeMi, Buono ATM, Merchandising Lamperti

### Leaderboard

Due classifiche:

- **Fontanelle**: tutte le 719 fontanelle ordinate per check-in, con podio evidenziato (oro, argento, bronzo)
- **Utenti**: classifica dei membri piu' attivi della community con livello, punti e check-in

Toccando una fontanella si apre il dettaglio; toccando un utente si apre il suo profilo pubblico.

### Profilo Utente

- Avatar, nome, livello e barra progresso XP
- Saldo punti spendibili con link a "Come guadagnare?"
- Statistiche settimanali/mensili: XP, check-in, fontanelle visitate, distanza percorsa, litri risparmiati, contributi
- Grafico attivita' (bar chart SVG) con dati giornalieri o settimanali
- Collezione badge con stato sbloccato/bloccato e progresso
- Sfide attive con barra di avanzamento
- Sezione premi e negozio

### Chat di Quartiere

- 8 chat room organizzate per zona di Milano (Sempione, Navigli, Duomo, Brera, Isola, Porta Venezia, Citta' Studi, Buenos Aires)
- Filtri per quartiere e tipologia (con eventi, attive)
- Sezione "Le Tue Chat" (chat a cui si e' iscritti) e "Scopri Chat" (nuove chat da unirsi)
- Creazione nuove chat con nome, categoria, quartiere e descrizione
- Messaggi in tempo reale con bolle colorate (teal per i propri, bianco per gli altri)
- Invio messaggi con tasto Invio o pulsante

### Eventi Comunitari

- Calendario mensile navigabile con giorni evidenziati
- 4 tipologie di eventi: Pulizia, Passeggiata, Incontro, Workshop
- Filtri per tipo e quartiere
- Creazione eventi direttamente dalle chat room
- Schede evento con data, ora, partecipanti e pulsante "Partecipa"

### Impostazioni

- Gestione account (profilo, email, privacy)
- Preferenze: notifiche, suoni, posizione, modalita' scura
- Reset tutorial iniziale
- Informazioni app e help

## Tecnologie Utilizzate

| Tecnologia | Versione | Uso |
|---|---|---|
| React | 18.3.1 | Framework UI |
| TypeScript | 5.6.2 | Tipizzazione statica |
| Vite | 6.3.5 | Build tool e dev server |
| Tailwind CSS | 3.4.17 | Styling utility-first |
| Google Maps API | @react-google-maps/api | Mappa interattiva |
| Lucide React | 0.487.0 | Iconografia |
| Radix UI | - | Componenti primitivi accessibili |

## Installazione e Setup

### Installazione su iPhone/smartphone (PWA)

Per l'esperienza ottimale su iPhone:

1. Apri l'app nel browser **Safari**
2. Tocca il pulsante **Condividi** (icona con freccia in alto)
3. Seleziona **"Aggiungi a Home"**
4. Apri l'app dall'icona sulla Home Screen

Questo rimuove le barre del browser e offre un'esperienza simile a un'app nativa, con supporto per safe area (notch, home indicator).
La stessa procedura funziona anche per Android, e risulta la modalità piu fedele all'applicazione finale.

## Dataset delle Fontanelle

L'app utilizza il dataset ufficiale del **Comune di Milano** contenente **719 fontanelle pubbliche**:

- **Fonte**: [Open Data Milano - Fontanelle nel Comune di Milano](https://dati.comune.milano.it/dataset/ds502_fontanelle-nel-comune-di-milano)
- **Formato originale**: GeoJSON (FeatureCollection)
- **File locale**: `src/data/fountains.json`
- **Dati per fontanella**: coordinate GPS, CAP, municipio, quartiere (NIL)

Gli attributi aggiuntivi (condizione, accessibilita', qualita' dell'acqua, ciotola per animali) sono generati in modo deterministico a partire dall'ID della fontanella per garantire coerenza tra le sessioni.

### Aggiornare il Dataset

1. Scarica il file GeoJSON aggiornato dal portale [Open Data Milano](https://dati.comune.milano.it)
2. Sostituisci `src/data/fountains.json`
3. Riavvia il server di sviluppo

## Design e UX

### Palette Colori

- **Primario**: Teal/Verde Acqua (`#14b8a6`) - richiama l'acqua delle fontanelle
- **Secondario**: Ambra (`#f59e0b`) - segnalazioni e podio leaderboard
- **Accento**: Blu (`#2563eb`) - posizione utente sulla mappa
- **Sfondo**: Grigio chiaro (`#f9fafb`)

### Pattern UX Mobile-First

- **Backdrop Blur**: sfocatura su dialoghi e modali per profondita' visiva
- **Touch-Friendly**: pulsanti e aree di tocco ottimizzati per smartphone
- **Portrait Lock**: rilevamento orientamento con overlay "Ruota il dispositivo"
- **Mappa personalizzata**: stile Google Maps con colori a tema acqua/verde, marker SVG custom

## Credits

- **Dataset**: [Comune di Milano - Open Data](https://dati.comune.milano.it)

- **Sviluppatori**: Gruppo EcoDevs: Giorgio Brenna, Andrea Roberto Benvenuti, Valerio Cipolloni, Michelangelo Stefanini, Emanuele Viani, Matteo Primerano
---

Progetto sviluppato per il corso di **Fondamenti di Human-Computer Interaction** - **Politecnico di Milano**
