<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logo di bestimage.ai"></a></p>

# Awesome Wan 3.0 Prompts — Guida italiana

**148 tracce di regia video in 14 categorie, adattate e curate dal gruppo di [bestimage.ai](https://bestimage.ai/).** Definisci un evento chiaro, assegna un ruolo agli elementi in ingresso e guida la ripresa, il suono e la continuità.

[Guida in inglese](README.md) · [Le 15 lingue](locales/README.md) · [Indice completo](prompts/README.md) · [Contribuire](CONTRIBUTING.md)

![Illustrazione concettuale: una persona dell’archivio apre una mappa stellare in un osservatorio all’alba](assets/wan-3-prompt-collection-hero.png)

*Illustrazione statica realizzata con lo strumento integrato di generazione di immagini, non un video prodotto da Wan 3.0. Consulta le [istruzioni delle immagini e la loro provenienza](assets/README.md).*

## Contenuti e primi passi

**148 tracce di regia video in 14 categorie**. Le prime sei categorie contengono indicazioni di regia in cinese, le altre otto in inglese. Le 15 lingue riguardano le guide introduttive e un esempio comparativo comune, **non la traduzione integrale di tutte le 148 tracce**. Le traduzioni e l’esempio comparativo non vengono conteggiati come voci aggiuntive.

1. Scegli una traccia nell’[indice completo](prompts/README.md).
2. Modifica le variabili e prepara tutti gli elementi richiesti. I riferimenti descrivono ruoli; i relativi file non sono inclusi nel repository.
3. Seleziona la modalità adatta e imposta durata, proporzioni, risoluzione e suono nell’interfaccia. Il solo testo non configura una richiesta API.
4. Esegui una piccola prova e controlla azione, geometria, identità, tempi e suono secondo gli obiettivi di verifica della traccia.

## Formula in otto livelli

```text
[Uscita] durata + proporzioni + linguaggio visivo
[Soggetto] tratti di identità riutilizzabili + dettagli immutabili
[Ambiente] momento + luogo + meteo + profondità spaziale
[Azione] innesco → movimento continuo → risultato visibile
[Camera] tipo di inquadratura + angolo + un percorso + quadro finale
[Aspetto] luce + tavolozza + materiali + resa del movimento
[Suono] ambiente + effetti + musica + dialogo
[Vincoli] elementi da preservare + errori più probabili
```

Usa una lingua principale per la descrizione visiva e specifica separatamente la lingua e le battute esatte del dialogo. Funzioni e impostazioni possono variare in base a prodotto, area geografica e piattaforma.

## Esempio comparativo completo

**Modalità:** testo in video · **Impostazioni:** 10 secondi, 16:9, suono attivo · **Elementi in ingresso:** nessuno

```text
Crea una ripresa documentaristica di 10 secondi in formato 16:9 in una tranquilla biblioteca di attrezzi di quartiere. Una persona adulta che fa volontariato, con capelli corti e ricci, un grembiule color senape e una camicia blu marino con le maniche rimboccate, ripara un piccolo ventilatore da tavolo rosso scollegato dalla presa. Da 0 a 3 secondi, appoggia la griglia protettiva smontata accanto al ventilatore fermo. Da 3 a 7 secondi, rimuove la polvere da una pala con un panno morbido mentre la camera scorre lentamente verso destra all’altezza del piano del tavolo. Da 7 a 10 secondi, posa il panno e allinea la griglia con la scocca, senza collegare alla presa né accendere il ventilatore. La luce della finestra rivela il metallo consumato e la trama del cotone. Suono: sfregamento del panno, un lieve clic della griglia, ambiente tranquillo della stanza; niente parlato né musica. Mantieni la stessa persona, lo stesso ventilatore, le sue tre pale, la scocca rossa e il cavo scollegato. Niente pale in rotazione, attrezzi aggiuntivi, etichette leggibili, sottotitoli o tagli.
```

**Variabili:** colore del grembiule, colore del ventilatore, luce della stanza. **Verifica:** il ventilatore rimane scollegato e fermo; il numero di pale e il contatto delle mani restano coerenti. È un concetto creativo, non un’istruzione per riparazioni elettriche.

## API Wan 3.0 su bestimage.ai

Queste pagine in inglese presentano l’interfaccia di prova e gli esempi pubblici di richieste.

| Modalità | Preparazione e scopo |
|---|---|
| [Testo in video](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Una scena completa con causa, azione intermedia e risultato visibile. |
| [Immagine in video](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Immagine iniziale **e immagine finale** per la modalità documentata; descrivere la transizione e preservare geometria e composizione. |
| [Riferimenti in video](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Riferimenti facoltativi di identità, oggetti, spazio, movimento o suono; assegnare un ruolo a ogni risorsa. |
| [Modifica video](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Filmato originale e una modifica circoscritta; preservare recitazione, durata, camera e zone non modificate. |

La [guida API e controllo dei costi](guides/bestimage-wan-3-api.md) spiega richieste, interrogazioni sullo stato delle attività e pianificazione delle prove. **Il server API di bestimage.ai è `https://api.flaq.ai`.** Usa una chiave API emessa dal tuo account bestimage.ai.

Controlla la pagina del modello e il tuo account prima di consumare crediti. Queste sono le modalità documentate da bestimage.ai; ciò non implica che tutti i prodotti Wan espongano gli stessi controlli.

## GPT Image 2 per preparare fotogrammi di riferimento

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) genera immagini statiche; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) modifica immagini e combina riferimenti visivi. Usali per preparare schede di personaggi, riferimenti di prodotti o composizioni iniziali e finali approvate prima di un’attività video.

Sono **modelli di immagine separati**, non interfacce video di Wan. Esporta e controlla le immagini prima di fornirle alla modalità Wan appropriata. Il repository non automatizza il passaggio e non afferma che le illustrazioni concettuali siano state generate tramite queste API. Consulta il [flusso di preparazione dei riferimenti](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Navigazione, guide e contributi

L’[indice delle 148 tracce](prompts/README.md) comprende narrazione cinematografica, prodotti, contenuti degli utenti, cibo e viaggi, sport, animazione, musica, servizi, scienza, architettura, produzione, commercio, dialoghi, natura e industria.

Le guide alla [scrittura delle istruzioni](guides/prompting-guide.md), alle [capacità e ai limiti](guides/model-capabilities.md) e alla [risoluzione dei problemi](guides/troubleshooting.md) sono in cinese semplificato. La guida API è in inglese. Un’immagine concettuale non dimostra continuità temporale, sincronizzazione labiale, precisione del modello o sicurezza del processo rappresentato.

Leggi le [indicazioni per contribuire](CONTRIBUTING.md) prima di condividere testi o contenuti multimediali. Includi impostazioni esatte, ruoli degli elementi in ingresso, diritti d’uso, osservazioni e un’indicazione veritiera dell’avvenuta prova o della sua assenza. Non condividere credenziali, documenti privati o URL firmati di contenuti multimediali con scadenza. Usa il [modulo di proposta](.github/ISSUE_TEMPLATE/prompt.yml) per preparare le informazioni richieste.

## Informazioni su bestimage.ai

Il team di [bestimage.ai](https://bestimage.ai/) cura e mantiene questa raccolta di prompt, collegando i flussi di lavoro creativi alle API dei modelli di immagini e video.

## Guadagna con il programma di affiliazione bestimage.ai

Pubblichi tutorial, prompt o integrazioni API? Iscriviti al [programma di affiliazione bestimage.ai](https://bestimage.ai/affiliate-program/) e ricevi commissioni consigliando bestimage.ai al tuo pubblico.

- **20%** sul primo ordine a pagamento valido di un utente segnalato.
- **10%** sui suoi successivi ordini a pagamento validi effettuati entro **60 giorni dalla registrazione**.

L’idoneità degli ordini e i pagamenti seguono l’[accordo di affiliazione vigente](https://bestimage.ai/affiliate-agreement/).

## Licenza

[MIT](LICENSE).
