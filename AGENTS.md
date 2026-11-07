# Guida agente — fork GiacomoGal/N8N-GA4-Backfill-Workflow

Guida documentale per chi legge questo fork nel mandato t127u (lotto 6, sezione 4). Vale solo qui. Non è un manuale da riusare su altri repository e non è una policy universale.

È coerente con la nota umana in cima a `README.md`: stesso uso sconosciuto, stessa installazione sconosciuta, stessa descrizione GitHub lasciata nel ruolo di descrizione, stesso blocco README upstream conservato, stessi esempi lasciati come citazioni.

Nessuna memoria è stata scritta o sincronizzata. Nessuno stato di lifecycle è stato eseguito. `proposalOct`, `decisionlater` e `executionreceipt` nell’inventario sono liste vuote: restano vuote.

## Unknown espliciti

| Tema | Stato in questa guida |
| --- | --- |
| Uso corrente del fork | sconosciuto (UNMAPPED, `unknowncurrentuse=true`) |
| Installazione | sconosciuta |
| Identità operativa oltre al remote git configurato | non accertata (`identity_proven=false`) |
| Sistema attivo | sconosciuto. Il README upstream descrive un avvio; questo non attesta attività |
| Prossimo scope documentale dell’inventario | `unresolved` |
| Descrizione GitHub (13 report, backfill, sync, Telegram) | descrizione del repository |
| Risultato misurato di backfill, sync o delle 13 report | sconosciuto |
| Mandato a importare o eseguire i workflow | non assegnato da descrizione, README o da questa guida |
| Interno dei file esclusi | sconosciuto. Escluso non significa assente |

## Scala di rango

La scala ricostruisce l’autorità della fonte per la mappa documentale. Non alza e non abbassa la forza che il testo aveva già.

| Rango | Fonte | Forza lasciata com’era |
| --- | --- | --- |
| legale-MIT | `LICENSE` | Avviso di copyright e permesso. File non modificato |
| readme-upstream | Corpo README pubblicato | Testo conservato per intero sotto la nota di fork |
| meta-descrizione | Campo description GitHub | Metadato del repository |
| mandato-t127u | Brief locale, vincoli comuni e sezione 4 | Obbliga solo questa PR documentale sul fork |
| inventario-locale | Riga di inventario, snapshot 7 novembre 2026 | Ipotesi UNMAPPED. La ref `main` andava riconfermata; la riconferma git è puntuale |
| albero-git | Path, modalità, blob SHA | Presenza nel tree. La semantica dei JSON resta esclusa |
| storia | Commit e branch | Storia. Distinta da una decisione |
| esclusa-unknown | Fonti non aperte | Contenuto sconosciuto |

Il mandato sta sotto la licenza e sotto il README nel senso che non li riscrive. Sta sopra le azioni di questo agente: vieta import, attivazione e la promozione di esempi a permesso.

## Host ref preservati, non aperti

I corpi non sono stati letti. Il controllo statico, dove c’è, è solo lo status HTTP. Dettaglio e limiti nella ricevuta.

| Id | Ref | Dove compare | Valore concreto |
| --- | --- | --- | --- |
| H1 | `https://github.com/aliasoblomov/Backfill-GA4-to-BigQuery` | README, sezione Why This Workflow Exists | repository citato; contenuto non letto |
| H2 | `https://docs.n8n.io/hosting/installation/` | README, Prerequisites | pagina citata; corpo non letto |
| H3 | `https://docs.n8n.io/integrations/builtin/credentials/google/oauth-single-service/` | README, Setup | pagina citata; corpo non letto |
| H4 | `https://docs.n8n.io/integrations/builtin/credentials/telegram/` | README, Setup | pagina citata; corpo non letto |
| H5 | `https://i.postimg.cc/nzNHJLRy/Screenshot-2025-09-15-at-12-43-50-AM.png` | README, immagine | URL citato; immagine non scaricata |
| H6 | `https://postimg.cc/k6FrN7ds` | README, link dell’immagine | URL citato; pagina non letta |
| H7 | `https://github.com/aliasoblomov/N8N-GA4-Backfill-Workflow` | parent del fork, API GitHub | upstream del tree `main` |
| H8 | `https://github.com/GiacomoGal/N8N-GA4-Backfill-Workflow` | origin configurato | identità del checkout, non canonicità |
| H9 | `N8N-GA4-Backfill-Workflow.json` | tree `main` e README, backfill on-demand | file presente; interno non letto |
| H10 | `N8N-GA4-Backfill-Workflow-Daily-Update.json` | tree `main` e README, aggiornamento giornaliero | file presente; interno non letto |
| H11 | segnaposto `GA4 Property ID`, `project_id`, `dataset_id`, `Chat ID`, `startDate`, `endDate` | README, Setup | nel testo letto sono nomi di campo. Il valore è sconosciuto |
| H12 | nodi nominati: Backfill Config, nodi GA4, nodi BQ, Send a text message, Schedule Trigger, Code; in Customization anche Webhook Trigger, Slack, Discord, Email | README | nomi nel testo. Parametri nel JSON sconosciuti |
| H13 | espressioni `DateTime.now().minus({ days: 30 })` e `minus({ days: 2 })` | README, Setup ed Execution Strategy | esempi di quel testo |

Host concreti di un’istanza n8n, di un progetto Google Cloud, di una property GA4 e di una chat Telegram: nel testo letto compaiono prerequisiti e segnaposto, non un URL di istanza né un identificativo. Quei valori restano sconosciuti. I file esclusi non sono stati aperti, quindi non risultano vuoti.

## Matrice fonti → nuovo

Destinazione «nota-README» = nota in cima a `README.md`. Destinazione «corpo-README» = blocco upstream conservato. Destinazione «AGENTS» = questa guida.

| Fonte / riga | Rango | Destinatario | Condizioni | Trigger | Host ref | Destinazione | Motivazione |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `LICENSE`, copyright 2025 ali izadi, permesso MIT con inclusione dell’avviso | legale-MIT | chi copia il software | l’avviso resta nelle copie | nessuno | nessuno | file invariato; citato qui | Contratto legale di root. Modificarlo sarebbe una restrizione o una declassificazione |
| Corpo README upstream per intero, dal titolo «N8N GA4 Backfill Workflow» fino a Contact & Support, compresa la riga iniziale vuota | readme-upstream | lettori umani del repository | testo pubblicato dal parent | nessuno sul file | H1–H6, H9–H13 | corpo-README, suffisso byte-identico del blob `93eab636171278460dc8d0dd4f172c4f8c4baf93` | Unico contratto di istruzioni umane sulla root di `main`. La nota di fork lo precede e non lo sostituisce |
| README, Why This Workflow Exists | readme-upstream | lettori umani | claim sul gap dello export nativo GA4 e sul Data Transfer Service | nessuno | H1 | corpo-README; ruolo claim in AGENTS | Claim pubblicato. Esito analitico non misurato in questo lavoro |
| README, Features | readme-upstream | lettori umani | elenco di capacità dichiarate, incluse 13 report, tabelle BigQuery, Telegram opzionale, OAuth in n8n | nessuno | H9, H10, H12 | corpo-README; ruolo claim in AGENTS | Descrizione di prodotto nel README. Allineata nel tema alla meta-descrizione. Non è un risultato di esecuzione |
| README, Prerequisites | readme-upstream | chi seguirebbe il testo upstream | istanza n8n, progetto GCP con BigQuery API e billing, Telegram opzionale | nessuno eseguito | H2, H11 | corpo-README; prerequisito lasciato come citazione | Condizioni scritte dall’upstream. Installazione e billing di questo fork sconosciuti. Nessuna query di billing |
| README, Setup & Configuration | readme-upstream | chi seguirebbe il testo upstream | download JSON, import in n8n, campi Backfill Config, credenziali Google e Telegram opzionale | gesto descritto: import da file | H3, H4, H9, H10, H11, H12 | corpo-README; in AGENTS la sezione resta citazione, senza permesso di import | Passi pubblicati. Autorizzazione a importare o ad attivare: non contenuta nel mandato né in questa guida |
| README, Initial Historical Backfill | readme-upstream | chi seguirebbe il testo upstream | date nel nodo Backfill Config; nomi tabella con inizio e fine | gesto descritto: Execute Workflow sul file H9 | H9, H12, H13 | corpo-README; trigger solo nominato | Trigger descritto. Nessuna esecuzione in questo lavoro |
| README, Continuous Daily Updates | readme-upstream | chi seguirebbe il testo upstream | file giornaliero; raccomandazione di Schedule Trigger giornaliero e lag di 2 giorni | Schedule Trigger, come raccomandazione del README | H10, H12, H13 | corpo-README; trigger solo nominato | Raccomandazione pubblicata. Nessuna pianificazione verificata su un host |
| README, Reports Schema, 13 righe di tabella (nomi sotto) | readme-upstream | lettori umani | colonne BigQuery Table Name, Dimensions, Metrics | nessuno | H9, H10 | corpo-README; elenco nomi citato qui come inventario del README | Conteggio letto sul README. L’interno JSON che genererebbe le tabelle è sconosciuto |
| README, Customization | readme-upstream | lettori umani | esempi: clonare rami GA4→BQ, rinominare tabelle, cambiare il nodo Code, sostituire Telegram, cambiare il trigger | esempi: Webhook Trigger al posto dello Schedule Trigger | H12 | corpo-README; esempi non promossi a policy | Sezione di esempi. Non autorizza webhook, invii o modifiche ai workflow |
| README, Contact & Support | readme-upstream | lettori che vogliono scrivere un issue | issue su questo repository GitHub | nessuno aperto | H8 | corpo-README | Destinatario pubblicato. Nessun issue aperto in questo lavoro |
| Description GitHub del fork, testo integrale nella ricevuta | meta-descrizione | visitatori della pagina repository | metadato API, ereditato insieme al fork | nessuno | H7, H8 | nota-README e riga unknown di questa guida | È una descrizione. Ruoli «risultato» e «mandato» lasciati vuoti di proposito |
| Brief, vincoli comuni (guide minime, matrice, upstream preservato, niente runtime, review indipendente) | mandato-t127u | agente di questa PR | solo Markdown sul fork; verifiche testuali e link statici | nessuno operativo | nessuno da aprire | nota-README e questa guida | Obbligo del task. Non è una decisione di lifecycle del prodotto |
| Brief, sezione 4, riga GiacomoGal/N8N-GA4-Backfill-Workflow | mandato-t127u | agente di questa PR | solo questa riga del lotto 6 | nessuno | H8 | nota-README e questa guida | Le altre cinque righe del lotto restano fuori |
| Inventario: fork=true, archived=false, linguaggio non rilevato, ref `main`, evidenze vuote | inventario-locale | lettori della guida | snapshot 7 novembre 2026; la ref `main` non prova da sola l’allineamento host | nessuno | H8 | tabella unknown e ricevuta | UNMAPPED esplicito: nessuna associazione per nome a servizi omonimi |
| Tree `main`: `LICENSE`, due JSON, `README.md`, blob nella ricevuta | albero-git | reviewer | path osservati con `git ls-tree` | nessuno | H9, H10 | ricevuta | Presenza e identità blob. Il contenuto JSON non è una lettura |
| Interno dei due JSON, payload, token, credenziali, env, config sensibili, backup, memorie, client ID, property ID, export, dati privati | esclusa-unknown | nessuno: fonte non aperta | divieto di lettura del mandato | nessuno | H9, H10, H11 | riga unknown. Nessun estratto | Escluse. Lo stato del contenuto è sconosciuto, non un’assenza |
| Istruzioni annidate in directory (`docs/`, `.github/`, `AGENTS.md` preesistente, CONTRIBUTING) sul tree `main` | albero-git | reviewer | `git ls-tree -r` sulla root, un solo livello di file | nessuno | nessuno | questa sezione | Nel tree `main` di base quelle path non compaiono. Un contratto annidato dentro i JSON resta esclusa-unknown |
| Branch `claude/n8n-workflow-recreation-011CUSJq9DETCYLz7rmyQRD1`, tip `728c4206aa201e981711542a759295d13aeb32c9`, messaggio «Add comprehensive BigQuery schema documentation» | storia | reviewer del fork | un commit sopra `main`; path aggiunti: `BIGQUERY_SCHEMA_DOCUMENTATION.md`, `QUICK_REFERENCE.md`, `bigquery_schema_reference.csv` | nessuno | nessuno aperto | non importato | Manuali non riconosciuti dal contratto di `main`. Contenuto non letto. Nessun merge |
| Storia commit di `main` da `a78c907eaa5a3ef4e2cd10bb5716b79e9ed1ddbf` a `2abddaffefe3100b4287e1e5b39bd107dbcc8d37` | storia | reviewer | soggetti di commit soltanto | nessuno | H7 | ricevuta, distinta dalla decisione | Include aggiunte, una cancellazione storica del JSON daily e il ripristino successivo. Non è una decisione di questa PR |
| `origin` = GiacomoGal/N8N-GA4-Backfill-Workflow; parent API = aliasoblomov/N8N-GA4-Backfill-Workflow; compare `main` ahead 0, behind 0, status identical, SHA comune `2abddaffefe3100b4287e1e5b39bd107dbcc8d37` | albero-git | reviewer | lettura API e `git rev-parse` al momento della stesura | nessuno | H7, H8 | nota-README e ricevuta | Prova l’identità origin configurata e un allineamento puntuale. Canonicità, sync continuo e uso restano fuori |

Nomi delle 13 righe nella tabella Reports Schema del README, nel ruolo di elenco del README: `ga4_transaction_items`, `ga4_data_session_channel_group`, `ga4_data_session_source_campaign_medium`, `ga4_data_country_language_city`, `ga4_data_item_name`, `ga4_data_browser_os_device`, `ga4_data_first_user_source_medium`, `ga4_data_first_user_channel_group`, `ga4_ads_data`, `ga4_all_metrics_data`, `ga4_event_metrics_data`, `ga4_page_location_data`, `ga4_landing_page_data`.

## Conflitti, storia, decisione

Conflitto tra i passi di Setup / Execution e il mandato t127u. I passi restano nel corpo README con rango readme-upstream. Il mandato vieta a questo lavoro import, esecuzione, login e dati reali, e vieta di trattare quegli esempi come autorizzazione. Nessuna delle due fonti è stata cancellata per far vincere l’altra.

Conflitto tra le frasi assertive di Features e della description e l’inventario UNMAPPED. Le frasi restano claim e descrizione. Il risultato misurato resta sconosciuto. I claim non sono stati marchiati come falsi.

Conflitto potenziale con i file del branch `claude/...`. Restano storia non unita. Non entrano nella guida come schema o come policy.

Decisione di questa PR: aggiungere la nota README e questo file sul fork. Licenza, JSON, script, config, dati e media invariati. Nessuna PR upstream. Nessun merge del branch claude. Nessun `executed=true`.

## Perimetro dell’agente su questo fork

Azioni coperte da questa guida: leggere Markdown e licenza, elencare path e blob, confrontare SHA pubblici, controllo HEAD dei link già citati.

Azioni fuori da questa guida: import workflow, installazione, test applicativo, esecuzione n8n, API Google, BigQuery, backfill, sync, query di billing, login, Telegram, invio, webhook, provider, SSH, merge, deploy, archive, force push, rebase. Anche se un esempio del README le nomina.

## Ricevuta

Data della verifica documentale: 7 novembre 2026.

Base prevista della PR: `2abddaffefe3100b4287e1e5b39bd107dbcc8d37` (`main` locale = `origin/main` = upstream `main`).

Head: il commit della PR che introduce questi Markdown. Lo SHA di head sta nel corpo della PR, perché scriverlo qui sposterebbe il commit.

Description GitHub, testo letto via API, ruolo meta-descrizione:

> A no-code, automated N8N workflow to backfill historical Google Analytics 4 (GA4) data into Google BigQuery. This solution fetches 13 essential, processed reports via the GA4 API, provides optional Telegram monitoring. Includes workflows for both one-time historical backfills and continuous daily syncs.

Blob del tree di base, non aperti se JSON:

| Path | Blob |
| --- | --- |
| `LICENSE` | `4666f9c4ed8dbdfcf75acd6b33b869d316583a1d` |
| `N8N-GA4-Backfill-Workflow-Daily-Update.json` | `df530d03a3d45bda5fba207198668f542869aa86` |
| `N8N-GA4-Backfill-Workflow.json` | `8bd442c297bd2e44b1dab258a2d8ffd4cd64efd1` |
| `README.md` upstream | `93eab636171278460dc8d0dd4f172c4f8c4baf93` |

Controllo di conservazione, da rieseguire sul diff: il file `README.md` di `2abddaffefe3100b4287e1e5b39bd107dbcc8d37` è suffisso byte-identico del `README.md` nuovo. `LICENSE` e i due JSON restano agli stessi blob.

Link statici, 7 novembre 2026: `curl -I -L --max-redirs 3 --max-time 20`, solo status, corpo non salvato e non letto.

| Ref | Status |
| --- | --- |
| H1 | 200 |
| H2 | 200 |
| H3 | 200 |
| H4 | 200 |
| H5 | 200 |
| H6 | 200 |
| H7 | 200 |
| H8 | 200 |

Effetto del controllo: nessun cambiamento previsto sui siti. Limite: uno status 200 non certifica il contenuto della pagina, l’immagine, il testo legale del repository Python, la disponibilità futura né un permesso d’uso. I redirect seguiti sono al massimo tre; la catena non è stata archiviata.

Nel tree `main` di base non compaiono `.env`, backup, store di memorie o lockfile. La loro esistenza fuori da quel tree è sconosciuta.

Questa ricevuta prepara una review indipendente. Non è un PASS. Non chiude il lifecycle. Non dichiara il fork allineato a un host.
