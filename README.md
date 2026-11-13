<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/2/2c/Logo_Poste_Italiane.svg" alt="Poste Italiane" height="80">

# 📮 SortVox

### Assistente vocale per lo smistamento postale

**Dì la via. Ricevi il portalettere.**

[![Made with ❤️ in Italia](https://img.shields.io/badge/Made%20with%20%E2%9D%A4%EF%B8%8F-in%20Italia-009246?style=for-the-badge)](https://www.poste.it)
[![PWA Ready](https://img.shields.io/badge/PWA-Ready-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)]()
[![License](https://img.shields.io/badge/License-Proprietary-F3D829?style=for-the-badge)]()
[![Version](https://img.shields.io/badge/Version-3.0-0050B9?style=for-the-badge)]()

[✨ Funzionalità](#-funzionalità) · [🚀 Come si usa](#-come-si-usa) · [⚙️ Amministrazione](#%EF%B8%8F-pannello-amministratore) · [🛠️ Sviluppo](#%EF%B8%8F-sviluppo)

</div>

---

## 🎯 Il problema

Nel centro di smistamento, migliaia di lettere arrivano ogni giorno. Chi le smista deve capire **a quale portalettere** assegnare ogni pezzo, in base a **via, civico e comune**. Farlo a mano significa consultare tabelle, cercare su carta, perdere tempo — e sbagliare.

## 💡 La soluzione

**SortVox** è un assistente vocale che risponde in un secondo:

> 🎙️ **Operatore:** *"Via Roma centoundici, Gravina di Catania"*
>
> 🔊 **SortVox:** *"Trentanove"*
>
> 📺 **Schermo:** **39**

Una voce, un numero, zero errori.

---

## ✨ Funzionalità

<table>
<tr>
<td width="50%">

### 🎤 Riconoscimento vocale continuo
- Ascolto **persistente** con auto-riavvio
- Lingua italiana nativa
- Anti-eco: mette in pausa mentre parla
- Bip sonori di conferma

### 🔊 Risposta vocale naturale
- Sintesi vocale italiana
- Numeri pronunciati per esteso (*"quarantatré"*, non *"quattro tre"*)
- Codici alfanumerici letti correttamente (*"undici A"*)

### 🧠 Ricerca intelligente
- **Fuzzy matching** con correzione automatica degli errori
- Riconosce abbreviazioni (`S. GIORGIO B.` → `San Giorgio in Bosco`)
- Ignora il DUG (`VIA`, `PIAZZA`, `VIC.`) quando non serve
- Priorità alle vie all'inizio della frase

</td>
<td width="50%">

### 📊 Gestione avanzata
- **CSV dinamico**: aggiornabile senza toccare il codice
- **CAP automatici** per tutti i comuni italiani
- Range di civici supportati
- Righe "via intera" senza civico

### 🔐 Sicurezza
- Pannello admin protetto da password
- Password modificabile dal browser
- No-index sui motori di ricerca
- Dati locali (nessun tracciamento esterno)

### 📈 Report e statistiche
- Top 10 vie, comuni, portalettere più cercati
- Log completo delle ricerche
- Esportazione in CSV
- Match rate e correzioni fuzzy

</td>
</tr>
</table>

---

## 🚀 Come si usa

### Per l'operatore

1. Apri l'app nel browser (Chrome o Edge)
2. Clicca **🎙️ Attiva microfono** (una volta sola)
3. Concedi il permesso al microfono
4. Dì la via, il civico e il comune:
   > *"Via Roma centoundici, Gravina di Catania"*
5. Leggi il numero grande e ascolta la risposta vocale

**Il microfono resta attivo** fino a quando non lo fermi. Ogni ricerca è indipendente: puoi fare 10, 100, 1000 ricerche senza ricaricare la pagina.

### Comandi supportati

| Comando vocale | Risposta |
|---|---|
| *"Via Roma 111, Gravina di Catania"* | Portalettere della via |
| *"Bocchi, Adria"* | Portalettere della via Bocchi ad Adria |
| *"San Giorgio in Bosco"* | Riconosce il comune anche se nel CSV è `S. GIORGIO B.` |
| *"Che ore sono?"* | 🕐 Legge l'ora italiana |
| *"Via Marconi, Campo San Martino"* | Gestisce comuni con più omonimie |

### Scorciatoie

- **Invio** nel campo manuale → cerca
- **Ferma microfono** → interrompe l'ascolto
- **Admin** → apre il pannello protetto (default: `123456`)

---

## 🎨 Design

Ispirato alla **identità visiva di Poste Italiane**:

| Colore | Codice | Uso |
|---|---|---|
| 🟡 Giallo Poste | `#F3D829` | Header, accenti, numero grande |
| 🔵 Blu Poste | `#0050B9` | Sfondo card, bottoni secondari |
| 🔷 Blu scuro | `#003B8A` | Riquadri, contrasto |
| ⚫ Blu notte | `#001F3F` | Sfondo pagina |

Interfaccia **scura** per ridurre l'affaticamento visivo nelle giornate lunghe in ufficio.

---

## ⚙️ Pannello amministratore

Clicca **🔒 Admin** in alto a destra e inserisci la password.

### Tab disponibili

| Tab | Cosa puoi fare |
|---|---|
| **Database** | Caricare/scaricare il CSV, ricaricarlo dal server, vedere il numero di righe |
| **Statistiche** | Top 10 vie, comuni, portalettere; contatori giornalieri; match rate |
| **Log ricerche** | Ultime 50 ricerche, esportabili in CSV per analisi |
| **Sicurezza** | Cambiare la password admin |

### Password default
