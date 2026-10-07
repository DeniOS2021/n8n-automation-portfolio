# n8n-Automatisierungen – Sammlung

**[DE](#deutsch) · [EN](#english)** · Projekte auf [denpilot.de](https://denpilot.de/#projekte)

> Bereinigte Kopien: ohne Zugangsdaten, IDs und Kontaktdaten. Fallstudien mit fiktiven Unternehmen, keine Kundendaten.

## Deutsch

| Ordner | Workflow | Was er tut | Knoten | Karte |
|---|---|---|---|---|
| `03_e-mail-assistant` | P3.1 Smart Secretary v1.4 | E-Mails klassifizieren, Termine prüfen, Antwort im Thread oder Entwurf, Anhänge je Kunde | 54 (27 funktional) | [E-Mail-Assistent](https://denpilot.de/#projekt-email-assistent) |
| `03_e-mail-assistant` | Error Handler | Fehler-Workflow → Telegram | 4 | – |
| `05_recruiting-rag` | Block 1 · Erfassung | Lebenslauf (PDF/Bild) → 8 Kernangaben → Tabelle + Pinecone | 35 | [Recruiting](https://denpilot.de/#projekt-recruiting) |
| `05_recruiting-rag` | Block 2 · Suche | Chatfrage → semantische Suche | 7 | [Recruiting](https://denpilot.de/#projekt-recruiting) |
| `05a_labs` | AIM-87 | Interview-Audio → Transkript → Analyse | 15 | – |
| `05a_labs` | AIM-91 | FAQ-Dokument → Pinecone | 5 | – |
| `05a_labs` | AIM-95 | HR-FAQ-Agent mit Weiterleitung an HR | 14 | – |
| `08_structured-output` | Structured AI Output | Screenshots, PDFs, Audio → strukturierte Daten, Map-Reduce, Self-Correcting Parser | 41 | [Structured Output](https://denpilot.de/#projekt-structured-ai-output) |
| `14a_id-ocr-hitl` | Ausweis-OCR | Vision liest 8 Felder, Mensch bestätigt | 19 | [Ausweis-OCR](https://denpilot.de/#projekt-ausweis-ocr) |

Architekturdiagramme: [`docs/architecture.md`](docs/architecture.md).

### Demo starten
1. n8n (self-hosted, aktuelle 1.x/2.x) starten.
2. **Neuen, leeren** Workflow anlegen → Menü **⋯ → Import from File** → JSON aus `workflows/` wählen.
   Wichtig: Import in einen bereits gefüllten Workflow fügt Knoten hinzu, statt ihn zu ersetzen.
3. Zugangsdaten (Credentials) in n8n anlegen und an den markierten Knoten auswählen – im JSON sind sie bewusst leer.
4. Platzhalter ersetzen (siehe `.env.example`): `YOUR_LOCAL_HOST`, `YOUR_CHAT_ID`, `YOUR_SHEET_ID` usw.
5. Erst testen, dann aktivieren. Alle Workflows sind im Export **inaktiv**.

### Grenzen
- Lern- und Prototyp-Workflows; getestet mit Testdaten, nicht im Dauerbetrieb.
- Recruiting: KI in der Bewerberauswahl ist Hochrisiko nach Anhang III KI-Verordnung – nur mit Testdaten verwenden, Entscheidung beim Menschen.
- Deepgram-Header enthält einen Platzhalter – eigenen Schlüssel als Header-Auth-Credential anlegen, nie im JSON speichern.

---

## English

| Folder | Workflow | What it does | Nodes | Card |
|---|---|---|---|---|
| `03_e-mail-assistant` | P3.1 Smart Secretary v1.4 | Classify e-mails, check appointments, reply in thread or draft, file attachments per client | 54 (27 functional) | [E-mail assistant](https://denpilot.de/en/#projekt-email-assistent) |
| `03_e-mail-assistant` | Error handler | Error workflow → Telegram | 4 | – |
| `05_recruiting-rag` | Block 1 · intake | CV (PDF/image) → 8 key facts → sheet + Pinecone | 35 | [Recruiting](https://denpilot.de/en/#projekt-recruiting) |
| `05_recruiting-rag` | Block 2 · search | Chat question → semantic search | 7 | [Recruiting](https://denpilot.de/en/#projekt-recruiting) |
| `05a_labs` | AIM-87 | Interview audio → transcript → analysis | 15 | – |
| `05a_labs` | AIM-91 | FAQ document → Pinecone | 5 | – |
| `05a_labs` | AIM-95 | HR FAQ agent with hand-over to HR | 14 | – |
| `08_structured-output` | Structured AI output | Screenshots, PDFs, audio → structured data, map-reduce, self-correcting parser | 41 | [Structured output](https://denpilot.de/en/#projekt-structured-ai-output) |
| `14a_id-ocr-hitl` | ID OCR | Vision reads 8 fields, a person confirms | 19 | [ID OCR](https://denpilot.de/en/#projekt-ausweis-ocr) |

Architecture diagrams: [`docs/architecture.md`](docs/architecture.md).

### Run the demo
1. Start n8n (self-hosted, current 1.x/2.x).
2. Create a **new, empty** workflow → menu **⋯ → Import from File** → pick a JSON from `workflows/`.
   Note: importing into a non-empty workflow adds nodes instead of replacing them.
3. Create the credentials in n8n and select them on the marked nodes – they are deliberately empty in the JSON.
4. Replace the placeholders (see `.env.example`): `YOUR_LOCAL_HOST`, `YOUR_CHAT_ID`, `YOUR_SHEET_ID`, etc.
5. Test first, then activate. All workflows are exported **inactive**.

### Limitations
- Learning and prototype workflows; tested with test data, not in continuous operation.
- Recruiting: AI in candidate selection is high-risk under Annex III AI Act – use with test data only, decision stays human.
- The Deepgram header contains a placeholder – create your own key as a header-auth credential, never store it in the JSON.

---
Cleaned copies: no credentials, IDs or contact details. Case studies with fictitious companies, no customer data. · Licence: MIT · [LinkedIn](https://www.linkedin.com/in/denys-kopyl-ai-automation/)
