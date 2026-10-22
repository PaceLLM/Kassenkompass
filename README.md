# Kassenkompass

[Deutsch](#deutsch) · [English](#english)

<a id="deutsch"></a>

## Deutsch

**Vom Kassenbon zum Ausgabenüberblick.**

Meine iPhone-App für Belegerfassung, Ausgabenübersicht und Budgets – entwickelt mit Unterstützung von ChatGPT und Codex, auf dem iPhone erprobt.

<p align="center"><img src="screenshots/app-icon.png" alt="Kassenkompass App-Icon" width="160"></p>

## Die Idee

Wohin geht mein Geld im Alltag? Kassenkompass hilft dabei, Belege zu erfassen, Ausgaben nach Kategorien zu ordnen und das eigene Budget im Blick zu behalten.

Dieses Repository präsentiert die App mit Screenshots und Einblicken in ihre Entwicklung. Der App-Quellcode wird hier nicht veröffentlicht.

## Was die App kann

- **Belege fotografieren:** Kameraansicht mit Orientierungshilfe, Licht- und Zoomsteuerung.
- **Erkannte Angaben prüfen:** Geschäft, Datum, Gesamtbetrag und Kategorie vor dem Speichern bearbeiten.
- **Ausgaben kategorisieren:** Beispielsweise Lebensmittel, Drogerie, Gesundheit, Mobilität und Freizeit; zuletzt verwendete Kategorien und Geschäftsvorschläge erleichtern die Eingabe.
- **Zeiträume vergleichen:** Wochen-, Monats- und Jahresansicht sowie Auswahl vergangener Zeiträume.
- **Budgets verfolgen:** Kategorienbudgets, verbleibende Beträge und Hinweise auf Überschreitungen.
- **Ausgaben visualisieren:** Verlauf als Balkendiagramm und Verteilung als Kreisdiagramm.
- **Belege verwalten:** Nach Kategorien filtern, Einträge ändern oder löschen.

Laut App erfolgt die Texterkennung und Speicherung lokal auf dem iPhone; Belegfotos werden dafür nicht an einen Server gesendet. Die App ist für die Offline-Nutzung ausgelegt.

## Ein Rundgang durch die App

### 1. Überblick und Budget

Die Startansicht verbindet Zeitraum, Ausgaben und Budgetinformationen.

<img src="screenshots/ueberblick.png" alt="Monatsübersicht mit Budgetanzeige" width="300"> <img src="screenshots/budgetwarnung.png" alt="Wochenübersicht mit Budgetwarnung" width="300">

### 2. Beleg fotografieren und Angaben prüfen

Die Kamera öffnet auf Knopfdruck. Nach der Aufnahme können die erkannten Angaben geprüft und korrigiert werden.

<img src="screenshots/beleg-scannen.png" alt="Belegaufnahme mit Kamera" width="300"> <img src="screenshots/beleg-pruefen.png" alt="Prüfung von Geschäft, Datum, Betrag und Kategorie" width="300">

### 3. Ausgaben verstehen und Belege verwalten

Farben machen Kategorien im Verlauf unterscheidbar. Die Belegliste ermöglicht Änderungen und das Löschen von Einträgen.

<img src="screenshots/ausgabenverlauf.png" alt="Ausgabenverlauf nach Kategorien" width="300"> <img src="screenshots/belege.png" alt="Nach Kategorien filterbare Belegliste" width="300">

Hier ist die Ansicht im Querformat mit dem Kreisdiagramm zur Verteilung der Ausgaben.

<img src="screenshots/kategorien.png" alt="Kreisdiagramm zur Verteilung der Ausgaben im Querformat" width="700">

Die Screenshots zeigen unterschiedliche Ansichten und Aufnahmestände der App.

## Entwickelt mit KI – gelernt durch Testen

Ich habe Kassenkompass mit Unterstützung von **ChatGPT** entwickelt. Ich habe Funktionen beschrieben, Vorschläge ausprobiert und die Ergebnisse auf meinem iPhone überprüft. Xcode wurde für den iOS-Build und die Installation verwendet; die App basiert auf React Native und Expo.

Die größte Herausforderung war, aus KI-generierten Vorschlägen eine funktionierende App zu machen:

| Herausforderung | Anpassung und Erfahrung |
|---|---|
| Belegerkennung fand den Gesamtbetrag nicht zuverlässig | Die Auswertung wurde angepasst, damit „SUMME“ und Beträge auch über benachbarte Textzeilen zugeordnet werden können. |
| Roter Startbildschirm: „No script URL provided“ | Eine Release-Version mit eingebettetem JavaScript ermöglichte den Start ohne laufenden Entwicklungsserver auf dem Mac. |
| Xcode-Build und Installation scheiterten zeitweise | Abhängigkeiten, der richtige Workspace, Dateizugriffsrechte und Apple-Signierung mussten geprüft und eingerichtet werden. |
| Ein KI-Vorschlag enthielt einen Konfigurationsfehler | Die CocoaPods-Konfiguration musste korrigiert und erneut geprüft werden. |
| Budgetwarnungen waren zu pauschal | Überschreitungen wurden je Kategorie berechnet und die Darstellung entsprechend verfeinert. |

**Meine wichtigste Erfahrung:** Vibe Coding hilft, Ideen umzusetzen. Testen, Fehler verstehen und Ergebnisse kritisch prüfen bleiben ein wesentlicher Teil der Entwicklung.

## Projektstand

Persönliches Entwicklungsprojekt und Portfolio-Präsentation. Die App wurde auf einem iPhone installiert und erprobt. Dieses Repository bietet keine Installationsdatei und keine App-Store-Veröffentlichung an.

---

Entwickelt von [Stefan Kümmel / PaceLLM](https://github.com/PaceLLM).


---

<a id="english"></a>

## English

**From receipt to spending overview.**

My iPhone app for capturing receipts, tracking spending and managing budgets — developed with support from ChatGPT and Codex and tested on an iPhone.

### The idea

Where does my money go? Kassenkompass helps capture receipts, organise expenses by category and keep track of personal budgets.

This repository presents the app through screenshots and insights into its development. The app's source code is not published here.

### What the app can do

- **Photograph receipts:** Camera view with a positioning guide, light and zoom controls.
- **Review recognised details:** Edit the store, date, total amount and category before saving.
- **Categorise spending:** Categories include groceries, personal care, health, transport and leisure. Recent categories and store suggestions make entry easier.
- **Explore time periods:** Weekly, monthly and yearly views, with access to previous periods.
- **Track budgets:** Category budgets, remaining amounts and overspending alerts.
- **Visualise expenses:** Spending trends in bar charts and category shares in a pie chart.
- **Manage receipts:** Filter by category, edit entries or delete them.

According to the app, text recognition and storage take place locally on the iPhone, without sending receipt photos to a server. The app is designed to work offline.

### A tour of the app

#### 1. Overview and budgets

The main view combines the selected period, expenses and budget information.

<img src="screenshots/ueberblick.png" alt="Monthly overview with budget information" width="300"> <img src="screenshots/budgetwarnung.png" alt="Weekly overview with an overspending alert" width="300">

#### 2. Capture a receipt and review its details

The camera opens when requested. After taking a photo, the recognised details can be reviewed and corrected.

<img src="screenshots/beleg-scannen.png" alt="Receipt camera view" width="300"> <img src="screenshots/beleg-pruefen.png" alt="Reviewing the store, date, amount and category" width="300">

#### 3. Understand spending and manage receipts

Colours distinguish categories in the spending chart. The receipt list allows entries to be edited or deleted.

<img src="screenshots/ausgabenverlauf.png" alt="Spending trends by category" width="300"> <img src="screenshots/belege.png" alt="Receipt list with category filters" width="300">

This landscape view shows the distribution of spending by category.

<img src="screenshots/kategorien.png" alt="Landscape view of spending by category" width="700">

The screenshots show different views and capture stages of the app. The app interface shown is in German.

### Developed with AI — improved through testing

I developed Kassenkompass with support from **ChatGPT**. I described features, tried suggestions and checked the results on my iPhone. Xcode was used to build and install the iOS app, which is based on React Native and Expo.

The biggest challenge was turning AI-generated suggestions into a working app:

| Challenge | Adjustment and lesson |
|---|---|
| Receipt recognition did not reliably identify the total | The parsing logic was adjusted to associate “SUMME” with amounts found on neighbouring text lines. |
| Red startup screen: “No script URL provided” | A release build with embedded JavaScript enabled the app to start without a development server running on the Mac. |
| Xcode builds and installation sometimes failed | Dependencies, the correct workspace, file permissions and Apple code signing needed to be checked and configured. |
| An AI suggestion introduced a configuration error | The CocoaPods configuration had to be corrected and checked again. |
| Budget warnings were too broad | Overspending was calculated per category and the visual feedback was refined. |

**My main takeaway:** Vibe coding helps turn ideas into software. Testing, understanding errors and critically reviewing the results remain essential parts of development.

### Project status

A personal development project and portfolio presentation. The app has been installed and tested on an iPhone. This repository does not provide an installation file or an App Store release.

---

Developed by [Stefan Kümmel / PaceLLM](https://github.com/PaceLLM).
