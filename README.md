# 🏠 Airbnb Market Analysis – Kommerz statt Community?

## 💻 Code-Beispiel (Python/Jupyter Notebook)
![Airbnb Python Code Preview](airbnb_code_preview.png)

## 📊 Analyse-Ergebnisse
![Airbnb Analysis Results](airbnb_results_preview.png)

---

## 🧾 Projektübersicht

| Kategorie | Details |
|------------|----------|
| 🧠 **Thema** | Datenbasierte Analyse der Airbnb-Kommerzialisierung in europäischen Großstädten |
| 🧰 **Tools** | Python (Pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook |
| 📊 **Datengrundlage** | 20 CSV-Dateien aus 10 europäischen Großstädten (Wochentags/Wochenende) |
| ⏱️ **Zeitraum** | Juli 2025 |
| 🎯 **Ziel** | Analyse der Professionalisierung von Airbnb und deren Auswirkungen auf Wohnungsmarkt |
| 💡 **Schwierigkeitsgrad** | Fortgeschritten – Fokus auf Feature Engineering, Korrelationsanalyse & Datenvisualisierung |

---

## 🎯 Projektziel
Ziel des Projekts war die Analyse von **Airbnb-Angeboten in 10 europäischen Städten** mit Python, um zu untersuchen, wie stark sich der Anteil professioneller Vermietungen gegenüber privaten Gastgebern entwickelt hat und welche **wirtschaftlichen und sozialen Folgen** dies für Bewohner, Tourismus und Stadtstruktur hat.

### **Fokus:**
- Wie stark ist Airbnb **kommerzialisiert**?
- Welche Unterschiede gibt es zwischen **privaten und professionellen Anbietern**?
- Welche **Preistreiber** dominieren den Markt?
- Wie unterscheiden sich **touristische und geschäftliche Viertel**?

---

## 🧩 Aufgabenstellung
Analysiere Airbnb-Angebote in 10 europäischen Großstädten, um:
- den **Anteil professioneller vs. privater Anbieter** zu quantifizieren,  
- **Preismuster und Preistreiber** zu identifizieren,  
- **Marktverzerrungen und Kommerzialisierungstendenzen** zu erkennen,  
- **datenbasierte Handlungsempfehlungen** für Regulierungsbehörden abzuleiten.

### **Projektnutzen:**
- Erkennung von Marktverzerrungen und Kommerzialisierungstendenzen  
- Beitrag zur Debatte über **Gentrifizierung**  
- Grundlage für datenbasierte Handlungsempfehlungen  
- Wirtschaftliche Implikationen auf lokaler Ebene

---

## 🧮 Datengrundlage
- **Quelle:** 20 CSV-Dateien (Wochentags/Wochenende) aus 10 europäischen Großstädten  
- **Städte:** Amsterdam, Berlin, Paris, London, Rom, Barcelona, Budapest, Athen, Lissabon, Wien  
- **Struktur:** Querschnittsdaten (kein Zeitverlauf)  
- **Preiseinheit:** 2 Nächte für 2 Personen  
- **Wichtige Variablen:**
  - Unterkunftstyp (Appartement, Privatzimmer, Gemeinschaftszimmer)
  - Anbieterform (Einzel-, Multi-, Profianbieter)
  - Superhost-Status, Bewertungen, Ausstattung, Lage
- **Tools:** Python (Pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook

---

## 🔍 Analyseschritte

### 1️⃣ **Datenbereinigung**
- Zusammenführung aller 20 CSV-Dateien zu einem einheitlichen Dataset  
- Spalten vereinheitlicht und ins Deutsche übersetzt  
- Behandlung fehlender Werte und Duplikate  
- Datentypen korrigiert und standardisiert

### 2️⃣ **Feature Engineering**
Neue Features erstellt zur besseren Analyse:
- **Preiskategorie** (Budget, Mittel, Gehoben, Luxus)  
- **Anbieter-Typ** (Einzelanbieter, Multianbieter, Profianbieter)  
- **Stadtteil-Typ** (Touristisch, Wirtschaftlich, Gemischt, Wohnorientiert)  
- **Häufigkeit der Angebote** (Buchungsstatistiken)  
- **Reverse Geocoding** zur Standortklassifizierung

### 3️⃣ **Verteilung der Unterkunftstypen und Anbietertypen**
- **Top-Städte:** London, Rom und Paris dominieren bei Angebot und Buchungen  
- **Schwaches Schlussfeld:** Amsterdam und Berlin mit geringster Aktivität  
- **Dominanz von Appartements:** Über 70 % des Angebots  
- **Professionalisierung:** Hohe Korrelation zwischen Angebot und Nachfrage  
- **Ausgewogene Verteilung** zwischen Einzel-, Multi- und Profianbietern (je ~33 %)

### 4️⃣ **Preisbildung & Preisanalyse**

#### **Einflussfaktoren auf den Airbnb-Preis:**
| Faktor | Korrelation | Einfluss |
|--------|-------------|----------|
| **Lageattraktivität** | +0,29 | 🟢 Stärkster Preistreiber |
| **Anzahl Schlafzimmer** | +0,22 | 🟢 Starker Einfluss |
| **Personenanzahl** | +0,20 | 🟢 Starker Einfluss |
| **Gästebewertung** | ~0 | 🔴 Kein Einfluss |
| **Superhost-Status** | ~0 | 🔴 Kein Einfluss |
| **Metro-Nähe** | ~0 | 🔴 Kein Einfluss |

#### **Preisunterschiede zwischen Städten:**
- **Höchste Medianpreise:** Paris, London, Amsterdam  
- **Niedrigste Preise:** Budapest, Athen, Lissabon  
- **Preisschwelle:** 1.000 € für zwei Nächte als Ausreißer-Grenze  
- **Amsterdam als Ausreißer-Stadt:** Durchgehend höchstes Preisniveau  
- **Barcelona:** Stärkster Preisaufschlag am Wochenende (+172 € bei Appartements)

#### **Ausreißerverhalten (Top 10 Hochpreisangebote):**
- Überwiegend von **professionellen Anbietern**  
- Meist **Appartements mit Luxusstandard**  
- Trotz kleiner Kapazität (2–3 Personen) extrem hohe Preise  
- Hohe Bewertungen und Sauberkeitsstandards (oft ohne Superhost-Status)  
- Klarer Hinweis auf **Kommerzialisierung**

### 5️⃣ **Geschäftsreisende vs. Touristen (Amsterdam-Fallstudie)**

| Stadtteil-Typ | Appartement (Wochentags) | Appartement (Wochenende) | Privatzimmer (Wochentags) | Privatzimmer (Wochenende) |
|---------------|--------------------------|--------------------------|---------------------------|---------------------------|
| **Wirtschaftlich** | 1.002 € | 1.002 € | Nicht verfügbar | Nicht verfügbar |
| **Touristisch** | 938 € | 983 € | 460 € | 543 € |
| **Geschäftlich** | 720 € | 769 € | 365 € | 392 € |
| **Gemischt** | 586 € | 638 € | 337 € | 365 € |
| **Wohnorientiert** | 548 € | 589 € | 337 € | 365 € |

**Erkenntnisse:**
- Wirtschaftsviertel haben höchste Preise, aber kaum Privatzimmer  
- Touristische Stadtteile: Deutlicher Preisanstieg am Wochenende  
- Wohnorientierte Viertel: Moderateste Preise, besonders bei Privatzimmern

### 6️⃣ **Häufigkeiten der Buchungen**
- **Superhost-Status** führt nicht automatisch zu höheren Buchungszahlen  
- **Appartements dominieren** die Buchungen (besonders in Paris, London, Rom)  
- **99,1 % der Top-10-Wiederholungsbuchungen** stammen von Profianbietern  
- **Gästebewertung und Sauberkeit** sind beste Indikatoren für Superhost-Status  
- Kommerzialisierte Angebote setzen auf **Standort und Preis** statt persönliche Auszeichnungen

---

## 📈 Ergebnisse & Insights

### 🔴 **Haupterkenntnisse**

#### **1. Airbnb ist stark kommerzialisiert**
- Nur **~35 % sind echte Einzelanbieter** (ursprüngliche Sharing-Idee)  
- **65 % Multi- und Profianbieter** dominieren den Markt  
- **99,1 % der Top-Buchungen** stammen von professionellen Anbietern

#### **2. Preise hängen hauptsächlich von Größe und Lage ab**
- **Lage (+0,29)** und **Schlafzimmeranzahl (+0,22)** sind Hauptpreistreiber  
- Superhost-Status, Bewertungen und Metro-Nähe haben **kaum Einfluss**  
- Große Preisspannen zwischen Städten (Budapest vs. Amsterdam: Faktor 2-3)

#### **3. Gemeinschaftszimmer spielen kaum eine Rolle**
- Unter **5 % des Gesamtangebots**  
- Kaum Nachfrage, marginale wirtschaftliche Bedeutung

#### **4. Ausnahme Berlin: Regulierung wirkt**
- Trotz touristischer Attraktivität **vergleichsweise geringe Buchungszahlen**  
- Hoher Anteil an **Einzelanbietern und Privatzimmern**  
- **Zweckentfremdungsverbot** wirkt sichtbar gegen professionelle Anbieter  
- Berlin bleibt näher an der **ursprünglichen Sharing-Idee**

### 🟡 **Kritische Faktoren**
- **Gentrifizierung:** Wohnraum wird für touristische Nutzung zweckentfremdet  
- **Marktverzerrung:** Professionelle Anbieter verdrängen private Gastgeber  
- **Preisdruck:** Besonders in Amsterdam, Paris und London  
- **Fehlende Regulierung:** Außer Berlin kaum wirksame Beschränkungen

---

## 🟢 **Handlungsempfehlungen**

### **1. Vermietung begrenzen & registrieren**
- Maximal **60–90 Tage pro Jahr** für private Anbieter  
- **Verpflichtende Registrierung** zur Unterscheidung von gewerblichen Vermietern  
- Sanktionen bei Verstößen

### **2. Echte Privatvermieter fördern**
- **Steuerliche Vorteile** für Einzelanbieter  
- **Erhöhte Sichtbarkeit** auf der Plattform (z. B. "Echte Privatvermieter"-Badge)  
- Stärkung der ursprünglichen Sharing-Idee

### **3. Wohnraum schützen**
- **Zweckentfremdete Wohnungen** zurückführen  
- **Illegale Vermietung** konsequent sanktionieren  
- Besonders wichtig in **angespannten Wohnungsmärkten**

### **4. Mehr Transparenz von Airbnb**
- **Datenoffenlegung** zu Inseraten, Buchungen und Anbieterstruktur  
- Ermöglicht **gezielte kommunale Steuerung**  
- Grundlage für evidenzbasierte Regulierung

---

## 🧠 Learnings
- Umfassende **Datenbereinigung und Feature Engineering** mit Pandas  
- **Korrelationsanalysen** zur Identifikation von Preistreibern  
- **Visualisierung komplexer Zusammenhänge** mit Matplotlib und Seaborn  
- **Geospatiale Analysen** durch Reverse Geocoding  
- **Explorative Datenanalyse (EDA)** zur Mustererkennung  
- **Storytelling mit Daten** zur Kommunikation komplexer Sachverhalte

---

## 📁 Projektdateien
| Datei | Beschreibung |
|--------|---------------|
| `Thorsten_Teetzen_Projektwoche_Python_Airbnb_2.ipynb` | Jupyter Notebook mit vollständiger Analyse |
| `Thorsten_Teetzen_Projektwoche_Python_Airbnb_Power_Point.pptx` | Präsentation der Ergebnisse |

### 💾 **Notebook öffnen:**
1. Lade die `.ipynb`-Datei herunter
2. Öffne sie mit [Jupyter Notebook](https://jupyter.org/) oder [Google Colab](https://colab.research.google.com/)
3. Führe die Zellen aus, um die Analyse nachzuvollziehen

---

## 📄 Lizenz
Dieses Projekt steht unter der MIT-Lizenz – siehe [LICENSE](LICENSE) Datei für Details.  
Es wurde im Rahmen der Weiterbildung zum **Data Analyst (IHK)** zu Lern- und Demonstrationszwecken erstellt.  
Eine kommerzielle Nutzung oder Weitergabe der enthaltenen Daten ist ausgeschlossen.  
© 2025 Thorsten Teetzen

---

## 👤 Autor

**Thorsten Teetzen**  
*Data Analyst (IHK-Zertifizierung in Ausbildung)*  

📅 **Projektzeitraum:** Juli 2025  
🌍 **Standorte:** Germany / Asia (Remote)  
🔗 [LinkedIn-Profil](https://www.linkedin.com/in/thorsten-teetzen-744891350)
