# Abgabe-Dokumente für den Kontaktsplitter Team Laura

# User-Stories
## User Story 1: Anrede identifizieren und speichern
**Als** Sachbearbeiter  
**möchte ich**, dass die Ausgabe des Visitenkartenscanners (Zeichenkette) automatisch in den Feldern "Anrede", "Titel", "Geschlecht", "Vorname" und "Nachname" zerlegt und zwischengespeichert wird,  
**um** sicherzustellen, dass die Daten standardisiert und korrekt vorliegen.

### Akzeptanzkriterien
- Die Anrede ("Herr", "Frau", etc.) wird korrekt erkannt und gespeichert.
- Das Geschlecht wird auf Basis der Anrede richtig zugeordnet (z. B. "Herr" → männlich).
- Der Titel soll anhand einer Titelliste erkannt und zugeordnet werden.
- Der/Die Vorname(n) und Nachname(n) soll(en) so gut es geht unterschieden und getrennt zu den korrespondierenden Feldern zugeordnet werden.
- Falls ein Inhalt der Zeichenkette einem Feld nicht automatisch zugeordnet werden kann, wird ein Annahme angezeigt, und die manuelle Auswahl/Änderung ist möglich.

### Priorität : Hoch

---

## User Story 2: Manuelle Anpassung von Feldern 
**Als** Sachbearbeiter  
**möchte ich**, dass ich die Inhalte der Felder bei Bedarf manuell manipulieren kann,  
**um** individuelle Anpassungen für spezielle Fälle vornehmen zu können.

### Akzeptanzkriterien
- Der Nutzer kann vorhandene Felder durch die Eingabefelder bearbeiten.
- Der Nutzer kann leere Felder durch die Eingabefelder füllen.
- Die Änderungen des Nutzers werden erfolgreich zwischengespeichert.

### Priorität : Hoch

---

## User Story 3: Bereitstellung und Erweiterbarkeit einer Titelliste
**Als** Sachbearbeiter  
**möchte ich**, dass eine vorgefertigten Titelliste (Top 20 häufigste Titel in Deutschland) über die Benutzeroberfläche aufgerufen und manuell erweitert werden kann,  
**um** individuelle Anpassungen für spezielle Fälle vornehmen zu können.
### Akzeptanzkriterien
- Der Nutzer kann Titel in die Titelliste hinzufügen.
- Die Änderungen werden solange das Programm läuft erfolgreich zwischengespeichert.

### Priorität : Hoch

---


## User Story 4: Standardisierte Briefanrede generieren
**Als** Sachbearbeiter  
**möchte ich**, dass eine Briefanrede auf Basis der Ausgabe des Visitenkartenscanners (Zeichenkette) generiert wird,  
**um** die Qualität und Konsistenz von Korrespondenz sicherzustellen.

### Akzeptanzkriterien
- Die generierte Briefanrede verwendet alle relevanten Felder: Anrede, Titel, Vorname und Nachname.
- Die Briefanrede entspricht der definierten Tabelle für Anreden (z. B. "Sehr geehrte Damen und Herren").

### Priorität : Hoch

---

## User Story 5: Doppelnamen formatieren
**Als** Sachbearbeiter  
**möchte ich**, dass Doppelnamen mit einem Bindestrich verbunden werden,  
**um** die Anrede leichter lesbarer zu gestalten.

### Akzeptanzkriterien
- Bei Doppelnamen oder ungewöhnlichen Formaten (z. B. Bindestriche) wird der Nachname korrekt interpretiert.
- Bei Doppelnamen wird der Bindestrich automatisch ergänzt.

### Priorität : Mittel

---

## User Story 6: Deutschsprachige Unterstützung für Anreden
**Als** Sachbearbeiter  
**möchte ich**, dass die Unterstüzung der deutsche Sprache, aber auch die potentzielle Erkennung anderer Sprachen gewährleistet ist,  
**um** eine internationale Korrespondenz zu ermöglichen.

### Akzeptanzkriterien
- Deutsch ist die Standard-Sprache.
- Den Nutzer wird mitgeteilt wenn eine andere Sprache erkannt wurde.

### Priorität : Niedrig

---

# Definition of Done (DoD)

Der Auftrag gilt als **fertiggestellt**, wenn alle der folgenden Kriterien erfüllt sind:

## **Allgemein**
- [ ] Alle User Stories sind vollständig umgesetzt und erfüllen die definierten Akzeptanzkriterien.
- [ ] Der Code ist in einer Versionsverwaltung (Git) sauber dokumentiert, inklusive beschreibender Commits.
- [ ] Die Anwendung ist vollständig lauffähig auf einem Windows 11 PC und kann ohne Fehler ausgeführt werden.
- [ ] Es existiert ein lauffähiger Build/Release, der die MVP-Funktionalität vollständig abbildet.

---

## **Clean-Code-Qualität**
- [ ] Der Quellcode ist klar strukturiert, formatiert, modular aufgebaut und leicht verständlich.
- [ ] Die Ordnerstruktur ist klar strukturiert modular aufgebaut und leicht verständlich.
- [ ] "Hard Coding" wird vermieden.
- [ ] Es werden Iterationen anstatt Rekursionen werden verwendet.
- [ ] Alle externen Bibliotheken/Dependencies sind im Design dokumentiert.
- [ ] Variablennamen befolgen Bennenungskonventionen.
- [ ] Clean-Code-Konventionen werden eingehalten (< 500 Zeilen / < 3 Parameter / DRY-Prinzip).
- [ ] Kommentaren sind sinnvoll genutzt, um Zweck und Funktionsweise verständlicher zu beschreiben.
- [ ] Kommentare befolgen Kommentarkonventionen (auskommentierten Code-Blöcke / TODOs:).

---

## **Tests**
- [ ] Unit-Tests decken größtenteils die implementierten Funktionen ab.
- [ ] Alle Testfälle sind erfolgreich durchlaufen und dokumentiert.
- [ ] Es existieren Testfälle für alle kritischen Use-Cases, insbesondere:
  - Erkennung der Anrede, des Titel, des Vorname, des Nachname und des Geschlechts.
  - Trennung von Vor- und Nachname.
  - Generierung der Briefanrede.
  - Generierung des Bindestrichs bei Doppelnamen.
  - Fehlerhafte Eingaben (z. B. doppelte Anrede, fehlender Name) werden korrekt gehandhabt.
- [ ] Integrationstests überprüfen die Zusammenarbeit verschiedener Module.
- [ ] Manuelle Tests wurden durchgeführt, um die Funktionalität auf der Zielplattform zu validieren.

---

## **Design und Architektur**
- [ ] Ein grobes Designkonzept liegt vor und ist in der Dokumentation enthalten.
- [ ] Die Datenstruktur ist logisch und leicht strukturiert.
- [ ] Das Programm ist so aufgebaut, dass durch Schnittstellen, zukünftige Erweiterungen (z. B. Datenbank-Anbindung) möglich wären.

---

## **Benutzerfreundlichkeit**
- [ ] Die Anwendung ist intuitiv zu bedienen, mit klaren Hinweisen und Fehlermeldungen.
- [ ] Bei manuellen Eingaben gibt es Eingabefelder, die die Benutzerführung unterstützen.
- [ ] Alle Felder (z. B. Anrede, Titel, Vorname, Nachname, Geschlecht) können vom Benutzer einfach überprüft und bearbeitet werden.

---

## **Dokumentation**
- [ ] Eine vollständige und verständliche Dokumentation liegt vor, die folgende Punkte enthält:
  - Übersicht über die Funktionalitäten (User Stories, Akzeptanzkriterien).
  - Kurzanleitung zur Installation und Nutzung der Anwendung.
  - Beschreibung der Datenstruktur.
- [ ] Release Notes dokumentieren Änderungen, technische Informationen und die Installationsanweisungen.

---

## **Abnahme**
- [ ] Ein Review mit mindestens einem Kollegen wurde durchgeführt, und alle identifizierten Probleme wurden behoben.
- [ ] Ein Code-Scanner hat den Quellcode auf Schwachstellen überprüft.

---

## **Qualitätssicherung**
- [ ] Alle Anforderungen der Aufgabenstellung wurden vollständig erfüllt.
- [ ] Die Gesamtbewertungskriterien der Aufgabe (MVP, User Stories, Tests, Release Notes, Funktionalität) sind abgedeckt und überprüft.

---

# **Kontakt-Splitter UI**

Die Anwendung "Kontakt-Splitter" bietet eine intuitive Benutzeroberfläche, um Namen und zugehörige Informationen wie Anrede, Vorname und Nachname zu analysieren, zu bearbeiten und für verschiedene Zwecke zu nutzen. Hier eine Beschreibung der einzelnen Bereiche und ihrer Funktionen:

---

## **Oberfläche und Funktionen**

### **1. Namen scannen**
- **Eingabefeld:** Ganz oben befindet sich ein Textfeld, in das der vollständige Name eingegeben werden kann (z. B. "Herr Max Mustermann").
- **Schaltfläche "Namen scannen":** Mit einem Klick auf diese orangefarbene Schaltfläche wird der eingegebene Name analysiert und automatisch in seine Bestandteile zerlegt (Anrede, Vorname, Nachname).

---

### **2. Modusauswahl**
Unter dem Bereich "Namen scannen" gibt es eine horizontale Leiste mit vier Hauptmodi, die unterschiedliche Funktionen bieten:

- **Briefanrede:** Generiert basierend auf den analysierten Daten eine standardisierte Briefanrede. Die Anrede wird im unteren Bereich angezeigt (z. B. "Sehr geehrter Herr Mustermann"). Es gibt außerdem ein Dropdown-Menü, um die Sprache der Anrede zu ändern.
  
- **Namen und Daten anpassen:** Ermöglicht die detaillierte Bearbeitung der aufgeteilten Daten. 
  - **Bearbeitungsfelder:** 
    - "Anrede", "Vorname" und "Nachname" werden einzeln aufgelistet, und jede Komponente kann manuell angepasst oder entfernt werden.
    - Zusätzliche Informationen wie Sprache und Geschlecht können hinzugefügt werden.
  - **Schaltflächen:** "Entfernen" entfernt eine Komponente, und "Komponente hinzufügen" erlaubt das Hinzufügen neuer Informationen.
  - **Speichern:** Mit der Schaltfläche "Aktualisieren" können alle Änderungen gespeichert werden.

- **Eingabeverlauf:** Dieser Modus ist in der Lage den eingegebenen Namen in einer Kontaktliste zu speichern, indem man die grüne Schaltfläche "Kontakt speichern drückt". Der Benutzer kann alte Eingaben einsehen und bei Bedarf wiederverwenden. Diese sind als blaue Schaltflächen dargestellt und werden per Mausklick ausgewählt.

- **Optionen ergänzen:** Hier können neue Titel, Anreden und Geschlechtsoptionen ergänzt werden, um die Analyse und Zuordnung weiter zu individualisieren. Für die Erweiterung der Titelliste ist ein Eingabefeld und ein Drop-Down mit verschiedenen Sprachen vorgesehen, die mit der blauen Schaltfläche "Hinzufügen" den neuen Titel speichert. Für das Hinzufügen eines neuen Genders gibt es auch ein Eingabenfeld mit einer "Hinzufügen"-Schaltfläche. Um eine neue Anrede zu speichern, wird ebenfalls ein Eingabefeld, sowie eine Drop-Down der verschiedenen Sprachen und ein Drop-Down mit den aktuell vorhandenen Gendern bereitgestellt. Die Speicherung erfolgt ebenfalls durch die Aktivierung der blauen Schaltfläche "Hinzufügen".

---

## **Anwendungsbeispiele**
1. **Eingabe eines Namens:** 
   - Geben Sie z. B. "Herr Dr. Max Mustermann" in das Textfeld ein und klicken Sie auf "Namen scannen". Der Name wird in "Anrede: Herr", "Titel: Dr.", "Vorname: Max", und "Nachname: Mustermann" aufgeteilt.

2. **Erstellung einer Briefanrede:** 
   - Wechseln Sie in den Modus "Briefanrede", und die Anwendung generiert automatisch die korrekte Anrede ("Sehr geehrter Herr Dr. Mustermann").

3. **Bearbeiten von Daten:**
   - Im Modus "Namen und Daten anpassen" können Sie etwa den Vornamen von "Max" zu "Alexander" ändern, oder andere Komponenten wie Anrede, Titel, Vorname oder Nachname hinzufügen, oder die bestehenden Attribute ändern. 

4. **Verwenden des Eingabeverlaufs:**
   - Speichern Sie diesen Kontakt und rufen Sie ihn nach weiteren Eingaben aus dem Eingabeverlauf ab, um Zeit zu sparen.

5. **Ergänzen von Optionen:**
   - Fügen Sie einen neuen Titel oder ein neues Gender in Kombination mit einer passenenden Anrede im Modus "Optionen ergänzen" hinzu.
---

# Release Notes - Kontaktsplitter v1.0

## **Version**: 1.0  
## **Release Date**: 28.05.2025  

---

## **Zusammenfassung**
Diese Version enthält die erste stabile Veröffentlichung des Kontaktsplitters, einer Anwendung zur automatisierten Erkennung und Verarbeitung von Kontaktinformationen (Anrede, Titel, Vorname, Nachname und Geschlecht). Die Anwendung wurde in Python entwickelt und als ausführbare Datei (.exe) für Windows 11 bereitgestellt.  

---

## **Neue Features**
### 1. **Automatische Anrede- und Geschlechtserkennung**
- Identifikation, Zuordnung und Zwischenspeicherung von der Anrede, den Titel, den Vorname, den Nachname und dem Geschlecht.
- Unterstützung für manuelle Anpassungen, falls die Zuordnung nicht eindeutig ist.
- Fehlermeldungen und Hinweise erhöhen die Benutzerfreundlichkeit und die Nachvollziehbarkeit.

### 2. **Trennung von Vor- und Nachnamen**
- Automatische Trennung von Vor- und Nachnamen, inklusive Unterstützung für Doppelnamen.

### 3. **Generierung von Briefanreden**
- Erstellung standardisierter Briefanreden auf Basis der eingegebenen Informationen auf verschiedenen Sprachen.

### 4. **Mehrsprachige Unterstützung**
- Unterstützung für die englische, deutsche, französische, spanische, italienische, portugiesische, polnische, tschechische, rumänische und serbische Sprache.

### 5. **Manuelle Anpassungen**
- Möglichkeit, neue Titel hinzuzufügen.

---

## **Systemanforderungen**
- **Betriebssystem**: Windows 11 (64-bit)
- **Laufzeitumgebung**: Python 3.10+ (falls Quellcode verwendet wird)
- **RAM**: 2 GB (Minimum)  
- **Speicherplatz**: 100 MB

---

## **Installation**
1. Laden Sie die ausführbare Datei (`Kontaktsplitter_v1.0.exe`) aus dem bereitgestellten Release-Paket herunter.
2. Speichern Sie die Datei an einem gewünschten Speicherort auf Ihrem Computer.
3. Doppelklicken Sie auf die Datei `Kontaktsplitter_v1.0.exe`, um die Anwendung zu starten.

## **Ausführung aus dem Quellcode**
Falls Sie den Quellcode ausführen möchten, gehen Sie wie folgt vor:
1. Laden Sie das Repository herunter oder klonen Sie es über Git:  
   
   git clone https://github.com/beispiel/kontaktsplitter.git

   pip install -r requirements.txt

   python main.py

---

## **Zukünftige Verbesserungen**
- persistente Datenbankanbindung

---
## **Support**

Falls Sie auf Probleme stoßen oder Feedback geben möchten, kontaktieren Sie uns bitte unter:
i22021@hb.dhbw-stuttgart.de

i22006@hb.dhbw-stuttgart.de

i22032@hb.dhbw-stuttgart.de

Vielen Dank, dass Sie den Kontaktsplitter verwenden!
Ihr Entwicklungsteam Laura
   
# KI-Einsatz bei der Geschlechtserkennung

## **Inhaltliche Fragen**

### **1. In wie weit berücksichtigt die KI gültige Standards und Normen dazu?**
Die KI verwendet keine explizit standardisierten oder normierten Datenbanken zur Geschlechtsbestimmung. Stattdessen basiert die Einschätzung auf einem KI-Modell (z. B. GPT-4.1-mini), das auf allgemeine Daten und Sprachmuster trainiert ist. Standards wie ISO-Identifikationen von Geschlechtern oder amtliche Namenslisten werden nicht berücksichtigt. 

Die Zuordnung erfolgt nach Wahrscheinlichkeit auf Basis des Namens und gängiger Konventionen, was in bestimmten Fällen zu kulturellen oder regionalen Ungenauigkeiten führen kann.

---

### **2. Ist die KI in der Lage, eine Briefanrede im richtigen Kontext zu erstellen (z. B. Amt/Funktion einer Person)?**
Die derzeitige Implementierung schätzt die KI das Geschlechts nur anhand dem Namen (z. B. "Alisia Musterfrau"), wenn keine Anrede wie beispielsweise (Mr. <> Mrs.) in der Eingabe vorhanden war, um das Geschlecht identifizieren zu können. Der Kontext von Amt oder Funktion (z. B. "Professor Dr." oder "Direktorin") wird nicht automatisch berücksichtigt, da solche Daten nicht explizit im Modell oder der Anfrage spezifiziert sind. 

Erweiterungen wären möglich, indem zusätzliche Informationen wie Berufsbezeichnungen oder Funktionstitel in die Analyse einfließen.

---

## **Allgemeine Fragen**

### **1. An welchen Stellen hat die Gruppe bei der Bearbeitung der Aufgabe KI eingesetzt?**
- **Geschlechtsschätzung:** Die Hauptaufgabe der KI ist die Einschätzung des Geschlechts anhand eines Namens. Dies wird durch eine Anfrage an das KI-Modell realisiert.
- **Erstellung standardisierter Briefanreden:** Die geschätzten Daten werden für die automatisierte Generierung von Anreden verwendet.

---

### **2. Wie verändert sich der Aufwand zur Bearbeitung hinsichtlich Dokumentation, Architektur/Design, Umsetzung, Test im Vergleich zu Gruppen, die keine KI einsetzen?**

#### **Anmerkung**
Wie bereits erwähnt, verwendet Team Laura nur KI wenn das Geschlecht aus dem Kontext nicht ersichtlich wird. Dann und erst dann wird KI in Kombination mit dem Namen verwendet um eine Schätzung durchzuführen. Das geschätzte Geschlecht kann aber durch die grafische Oberfläche wieder modifiziert werden und erweitert werden, um niemanden zu diskriminieren.

#### **Dokumentation**
- Die Dokumentation wurde durch allein anhand dieses Kapitel komplexer, welches nicht nötig wäre wenn keine KI genutzt werden würde.

#### **Architektur/Design**
- Mit KI wird die Architektur dynamischer, da eine API-Integration erforderlich ist. Dies erhöht die Komplexität, da:
  - Verbindungen zu OpenAI gepflegt werden müssen.
  - Sicherheit (API-Key-Management) berücksichtigt werden muss.
- Ohne KI erfolgt die Geschlechtszuordnung durch eine statische Komponente, die einfacher, aber weniger flexibel ist.

#### **Umsetzung**
- Mit KI wird auf eine Alternative zugegriffen, die anhand bekannter Muster eine Zuordnung ermöglicht.
- Ohne KI müsste eine eigenständige Logik zur Geschlechtserkennung (z. B. Datenbank von Namen mit Geschlechtszuordnung) implementiert werden.

#### **Test**
- Mit KI ist die Testbarkeit eingeschränkt, da die internen Entscheidungswege der KI nicht vollständig transparent sind. Es müssen Testfälle definiert werden, um typische und problematische Eingaben zu prüfen.
- Dennoch lässt sich sagen, dass die Zuordnung eines Geschlechts zu einem Namen unter dem selben Seed deterministisch ist und daher theoretisch testbar wär, aber alle Namne zu testen jedoch wiederum nicht vollständig testbar ist.
- Ohne KI wäre eine größere Abdeckung, anhand der Transparenz, durch statische Tests möglich.

---

### **3. Wohin verschiebt sich die Arbeitsweise?**
-
 **Mit KI:** 
  - Mehr Aufwand fließt in Integration und Optimierung des Modells sowie der Definition klarer Schnittstelle.
  - Der Testaufwand verschiebt sich von funktionalen Tests hin zu explorativen Tests, um die Qualität der KI-Antworten sicherzustellen.
- **Ohne KI:** 
  - Mehr Aufwand fließt in die Erstellung einer vollständigen, regelbasierten Lösung und in die manuelle Pflege einer Namensliste.

---

### **4. Wo sind hier die Grenzen der eingesetzten KI?**
- **Eingeschränkte kulturelle und regionale Unterschiede:** Namen können je nach Region unterschiedliche Geschlechter haben (z. B. "Andrea" in Italien vs. Deutschland). Solche Nuancen werden nicht immer korrekt berücksichtigt.
- **Unklarheit bei seltenen oder geschlechtsneutralen Namen:** Die KI kann bei Namen wie "Toni" oder "Sam" nur eine unsichere Schätzung ("X") liefern.
- **Kontextignoranz:** Die KI kennt weder den kulturellen noch funktionalen Kontext der Person (z. B. berufliche Titel oder Ämter).

---

### **5. Wie vergleichbar ist die Qualität der Ergebnisse ohne KI?**
- **Mit KI:** 
  - Die Ergebnisse sind schneller und decken viele Fälle korrekt ab.
  - Es bleibt jedoch eine gewisse Unzuverlässigkeit bei Grenzfällen.
- **Ohne KI:** 
  - Die Ergebnisse wären konsistenter und vollständig nachvollziehbar, erfordern jedoch eine aufwendige manuelle Pflege und größere Datenbanken.

---

### **6. Unterscheiden sich verschiedene Modelle in ihren Antworten und deren Güte?**
Ja, die Antworten und deren Qualität hängen stark vom gewählten Modell und seinem Training ab:
- Modelle wie GPT-4 oder spezialisierte Namensanalyse-Tools können unterschiedliche Ergebnisse liefern.
- GPT-4 ist vielseitig und bietet bei ausreichendem Training eine hohe Genauigkeit, während kleinere Modelle (z. B. GPT-4.1-mini) möglicherweise eingeschränkt sind.

---

### **7. Wie misst man die Güte einer Antwort einer KI bezogen auf die Aufgabenstellung?**
- **Testfälle:** Eine Liste von Namen mit bekannten Geschlechtern kann verwendet werden, um die Genauigkeit der KI zu messen.
- **Erfolgsquote:** Prozentualer Anteil korrekt geschätzter Geschlechter.
- **Fehlerrate:** Anteil der Fälle, bei denen die KI "X" oder ein falsches Geschlecht liefert.
- **Benutzerfeedback:** Direkte Rückmeldungen von Anwendern zur Qualität und Korrektheit der Ergebnisse.

---

## **Fazit**
Der Einsatz der KI spart Zeit und Aufwand bei der Geschlechter- und Namensanalyse. Allerdings erfordert die Verwendung zusätzlicher technischer Maßnahmen für die Integration, klare Tests und eine gute Dokumentation der Limitationen. Es bleibt wichtig, die KI-Ergebnisse zu validieren, insbesondere in kritischen Kontexten.


