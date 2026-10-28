# 📖 Guida alla Sintassi Base di Markdown

> Questa è la traduzione completa e ufficiale in italiano della guida alla sintassi base di [Markdown Guide](https://www.markdownguide.org/basic-syntax/), progettata per aiutarti a formattare documenti e repository su GitHub e altre piattaforme.

---

## 📋 Indice dei Contenuti
- [Panoramica](#-panoramica)
- [Intestazioni (Headings)](#-intestazioni-headings)
- [Paragrafi](#-paragrafi)
- [Interruzioni di Linea (Line Breaks)](#-interruzioni-di-linea-line-breaks)
- [Enfasi (Emphasis)](#-enfasi-emphasis)
- [Citazioni (Blockquotes)](#-citazioni-blockquotes)
- [Elenchi (Lists)](#-elenchi-lists)
- [Codice (Code)](#-codice-code)
- [Linee Orizzontali (Horizontal Rules)](#-linee-orizzontali-horizontal-rules)
- [Link (Links)](#-link-links)
- [Immagini (Images)](#-immagini-images)
- [Caratteri di Escape (Escaping Characters)](#-caratteri-di-escape-escaping-characters)
- [HTML HTML](#-html)
- [Licenza](#-licenza)

---

## 📌 Panoramica

Quasi tutte le applicazioni Markdown supportano la sintassi di base delineata nel documento di progettazione originale di John Gruber. Possono esserci lievi variazioni e discrepanze tra i vari processori e parser Markdown: ove possibile, queste sono segnalate direttamente nel testo.

---

## 📑 Intestazioni (Headings)

Per creare un'intestazione, aggiungi uno o più cancelletti (`#`) davanti a una parola o frase. Il numero di cancelletti corrisponde al livello dell'intestazione (da `<h1>` a `<h6>`).

| Markdown | HTML equivalente | Risultato Renderizzato |
| :--- | :--- | :--- |
| `# Intestazione di Livello 1` | `<h1>Intestazione di Livello 1</h1>` | **Intestazione di Livello 1** |
| `## Intestazione di Livello 2` | `<h2>Intestazione di Livello 2</h2>` | **Intestazione di Livello 2** |
| `### Intestazione di Livello 3` | `<h3>Intestazione di Livello 3</h3>` | **Intestazione di Livello 3** |
| `#### Intestazione di Livello 4` | `<h4>Intestazione di Livello 4</h4>` | **Intestazione di Livello 4** |
| `##### Intestazione di Livello 5` | `<h5>Intestazione di Livello 5</h5>` | **Intestazione di Livello 5** |
| `###### Intestazione di Livello 6` | `<h6>Intestazione di Livello 6</h6>` | **Intestazione di Livello 6** |

### 🛠️ Sintassi Alternativa (Setext)
In alternativa, puoi inserire qualsiasi numero di caratteri `=` sulla riga sottostante per creare un'intestazione di livello 1, oppure `-` per un'intestazione di livello 2.

```markdown
Intestazione di Livello 1
=========================

Intestazione di Livello 2
-------------------------
```

### 💡 Best Practices per le Intestazioni
Alcuni parser Markdown richiedono uno spazio tra i cancelletti (`#`) e il testo dell'intestazione. Per garantire la massima compatibilità tra diverse applicazioni, **inserisci sempre uno spazio**.

| ✅ Corretto | ❌ Da evitare |
| :--- | :--- |
| `# La mia intestazione` | `#Lamiaintestazione` |

È inoltre raccomandato separare le intestazioni dal testo circostante con righe vuote.

---

## 📝 Paragrafi

Per creare dei paragrafi, separa uno o più blocchi di testo con una o più **righe vuote**.

```markdown
Mi piace molto usare Markdown per documentare i progetti.

Rende la formattazione pulita e velocissima.
```

### 💡 Best Practices per i Paragrafi
A meno che il paragrafo non sia all'interno di un elenco o di un blocco particolare, **non indentare mai** le righe con spazi o tabulazioni.

| ✅ Corretto | ❌ Da evitare |
| :--- | :--- |
| `Questo è un paragrafo regolare.` | `  Questo è un paragrafo con rientro.` |

---

## ↵ Interruzioni di Linea (Line Breaks)

Per inserire un'interruzione di linea (`<br>`), termina la riga inserendo **due o più spazi** e premi **Invio**.

```markdown
Questa è la prima riga.  
E questa è la seconda riga nella stessa riga di paragrafo.
```

### 💡 Best Practices per le Interruzioni di Linea
Poiché gli spazi finali sono invisibili negli editor, molte persone preferiscono inserire direttamente il tag HTML `<br>` per garantire la massima chiarezza e compatibilità.

```markdown
Prima riga del testo.<br>
Seconda riga del testo.
```

---

## 🔤 Enfasi (Emphasis)

Puoi evidenziare il testo applicando lo stile **grassetto**, *corsivo* o una combinazione di entrambi.

### ◼️ Grassetto
Per rendere il testo in **grassetto**, inserisci due asterischi (`**`) o due trattini bassi (`__`) prima e dopo la parola o frase.

```markdown
Questo testo è **molto importante**.
Questo testo è __molto importante__.
```

### 📐 Corsivo
Per mettere il testo in *corsivo*, inserisci un singolo asterisco (`*`) o un singolo trattino basso (`_`) prima e dopo la parola o frase.

```markdown
Questo testo è *in corsivo*.
Questo testo è _in corsivo_.
```

### 🔲 Grassetto e Corsivo
Per applicare contemporaneamente **_grassetto e corsivo_**, utilizza tre asterischi (`***`) o tre trattini bassi (`___`).

```markdown
Questo testo è ***estremamente importante***.
Questo testo è ___estremamente importante___.
```

> ⚠️ **Nota di compatibilità:** Per evitare comportamenti inattesi, è preferibile utilizzare gli asterischi (`*` o `**`) se l'enfasi deve essere applicata a una porzione *interna* a una singola parola (es. `par**ol**a`).

---

## 💬 Citazioni (Blockquotes)

Per creare un blocco di citazione, aggiungi il simbolo `>` all'inizio di una riga.

```markdown
> La semplicità è il presupposto della stabilità.
```

### Citazioni con Paragrafi Multipli
Le citazioni possono contenere più paragrafi. Ricordati di aggiungere il carattere `>` anche sulle righe vuote tra un paragrafo e l'altro.

```markdown
> Questo è il primo paragrafo della citazione.
>
> Questo è il secondo paragrafo all'interno della stessa citazione.
```

### Citazioni Annidate
Puoi annidare una citazione all'interno di un'altra aggiungendo `>>`.

```markdown
> Citazione principale
>> Questa è una citazione annidata all'interno della citazione principale.
```

### Citazioni con Altri Elementi
Le citazioni possono contenere altri elementi formattati in Markdown, come intestazioni, elenchi e testo in grassetto.

```markdown
> #### Il Principio della Citazione
>
> 1. Primo punto fondamentale.
> 2. Secondo punto con testo in **grassetto**.
```

---

## 📋 Elenchi (Lists)

Puoi organizzare gli elementi in elenchi ordinati (numerati) o non ordinati (puntati).

### 🔢 Elenchi Ordinati
Per creare un elenco ordinato, fai precedere ogni voce da un numero seguito da un punto e uno spazio. I numeri non devono necessariamente essere in sequenza, ma l'elenco deve iniziare con il numero `1`.

```markdown
1. Primo elemento
2. Secondo elemento
3. Terzo elemento
4. Quarto elemento
```

I parser tradurranno automaticamente la sequenza numerica in modo corretto nell'HTML generato.

### 🔘 Elenchi Non Ordinati
Per creare un elenco non ordinato, inserisci un trattino (`-`), un asterisco (`*`) o un segno più (`+`) seguito da uno spazio prima di ogni voce.

```markdown
- Primo elemento
- Secondo elemento
- Terzo elemento
```

### 🔀 Elenchi Annidati (Sotto-elenchi)
Per annidare un elemento all'interno di un altro, applica un rientro di **2 o 4 spazi** (o una tabulazione).

```markdown
1. Primo elemento
2. Secondo elemento
   - Sotto-elemento A
   - Sotto-elemento B
3. Terzo elemento
```

---

## 💻 Codice (Code)

### 🔹 Codice In-line
Per evidenziare una parola o una frase come codice all'interno di un paragrafo, racchiudila tra due accenti gravi (backtick `` ` ``).

```markdown
Per installare il pacchetto, usa il comando `npm install`.
```

Se la stringa di codice contiene già un backtick, puoi racchiuderla tra doppi backtick.

```markdown
Usare il comando `` `code` `` per mostrare il backtick.
```

### 📦 Blocchi di Codice (Code Blocks)
Per creare blocchi di codice su più righe, puoi rientrare ogni riga di almeno 4 spazi o usare tre backtick (```) prima e dopo il blocco.

````markdown
```
{
  "firstName": "Mario",
  "lastName": "Rossi",
  "age": 30
}
```
````

---

## ➖ Linee Orizzontali (Horizontal Rules)

Per creare una linea di separazione orizzontale (`<hr>`), inserisci tre o più asterischi (`***`), trattini (`---`) o trattini bassi (`___`) su una riga separata.

```markdown
***

---

___
```

---

## 🔗 Link (Links)

Per creare un collegamento ipertestuale, racchiudi il testo del link tra parentesi quadre `[ ]`, seguito dall'URL tra parentesi tonde `( )`.

```markdown
Visita la [Guida Markdown](https://www.markdownguide.org).
```

### 🏷️ Aggiungere un Titolo al Link
Puoi aggiungere facoltativamente un titolo al link (visibile al passaggio del mouse). Inserisci il titolo tra virgolette dopo l'URL.

```markdown
Visita il [Sito Ufficiale](https://www.markdownguide.org "Vai alla home page").
```

### ✉️ Indirizzi Email e URL Diretti
Per convertire rapidamente un URL o un indirizzo e-mail in un link cliccabile, racchiudilo tra parentesi angolari `< >`.

```markdown
<https://www.markdownguide.org>
<esempio@email.it>
```

---

## 🖼️ Immagini (Images)

Per inserire un'immagine, la sintassi è simile a quella dei link, preceduta da un punto esclamativo (`!`):

`![Testo Alternativo](URL_o_Percorso_Immagine "Titolo opzionale")`

```markdown
![Logo Markdown](https://www.markdownguide.org/assets/images/markdown-mark-white.svg "Logo Ufficiale Markdown")
```

Per creare un'immagine che funzioni anche come link, racchiudi la sintassi dell'immagine all'interno delle parentesi quadre di un link standard:

```markdown
[![Logo Markdown](https://www.markdownguide.org/assets/images/markdown-mark-white.svg)](https://www.markdownguide.org)
```

---

## 🛡️ Caratteri di Escape (Escaping Characters)

Per mostrare un carattere speciale letterale che verrebbe altrimenti interpretato come sintassi Markdown, inserisci una barra rovesciata (`\`) davanti al carattere.

```markdown
\* Questo testo non sarà in corsivo, mostrerà l'asterisco letterale. \*
```

### Caratteri Escapabili
Puoi applicare l'escape tramite barra rovesciata `\` ai seguenti caratteri:

| Carattere | Nome |
| :---: | :--- |
| `\` | Barra rovesciata (Backslash) |
| \` | Accento grave (Backtick) |
| `*` | Asterisco |
| `_` | Trattino basso (Underscore) |
| `{ }` | Parentesi graffe |
| `[ ]` | Parentesi quadre |
| `( )` | Parentesi tonde |
| `#` | Cancelletto |
| `+` | Segno più |
| `-` | Trattino / Meno |
| `.` | Punto |
| `!` | Punto esclamativo |
| `|` | Barra verticale (Pipe) |

---

## 🌐 HTML

Molti parser Markdown ti consentono di inserire direttamente codice HTML all'interno dei tuoi file per realizzare personalizzazioni avanzate non coperte dalla sintassi base.

```markdown
Questo è un paragrafo in sintassi standard con un testo <span style="color:red;">colorato in rosso via HTML</span>.
```

---

## 📜 Licenza

Questo documento e la relativa traduzione sono rilasciati sotto licenza **Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA-4.0)**.

Puoi condividere, modificare e riutilizzare liberamente questo materiale per qualsiasi scopo, a condizione di attribuire la paternità dell'opera originale a [Markdown Guide](https://www.markdownguide.org) e di distribuire eventuali opere derivate sotto la medesima licenza.