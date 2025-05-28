# Abgabe-Dokumente für den Kontaktsplitter Team Laura

# User-Stories
## User Story 1: Anrede identifizieren, aufteilen und zwischenspeichern
**Als** Sachbearbeiter:in  
**möchte ich**, dass die Ausgabe des Visitenkartenscanners (Zeichenkette) automatisch in den Feldern "Titel", "Vorname", "Nachname" und "Geschlecht" zerlegt und zwischengespeichert wird,  
**um** sicherzustellen, dass die Daten standardisiert und korrekt vorliegen.

### Akzeptanzkriterien
- Die Anrede ("Herr", "Frau", etc.) wird korrekt erkannt.
- Das Geschlecht wird auf Basis der Anrede richtig zugeordnet (z. B. "Herr" → Männlich).
- Der Titel soll anhand einer Titelliste erkannt und zugeordnet werden.
- Der/Die Vorname(n) und Nachname(n) soll(en) so gut es geht unterschieden und getrennt zu den korrespondierenden Feldern zugeordnet werden.
- Falls ein Inhalt der Zeichenkette einem Feld nicht automatisch zugeordnet werden kann, wird ein Annahme angezeigt, und die manuelle Auswahl/Änderung ist möglich.

### Priorität : Hoch

---

## User Story 2: Manuelle Anpassung von Feldern 
**Als** Sachbearbeiter:in
**möchte ich**, dass ich die Inhalte der Felder bei Bedarf manuell manipulieren kann,  
**um** individuelle Anpassungen für spezielle Fälle vornehmen zu können.

### Akzeptanzkriterien
- Die Nutzer:innen können vorhandene Felder durch die Eingabefelder bearbeiten.
- Die Nutzer:innen können leere Felder durch die Eingabefelder füllen.
- Die Änderungen der Nutzer:innen werden erfolgreich zwischengespeichert.

### Priorität : Hoch

---

## User Story 3: Bereitstellung und Erweiterbarkeit einer Titelliste
**Als** Sachbearbeiter:in
**möchte ich**, dass eine vorgefertigten Titelliste (Top 20 häufigste Titel in Deutschland) über die Nutzungsoberfläche aufgerufen und manuell erweitert werden kann,  
**um** individuelle Anpassungen für spezielle Fälle vornehmen zu können.
### Akzeptanzkriterien
- Die Nutzer:innen können Titel in die Titelliste hinzufügen.
- Die Änderungen werden solange das Programm läuft erfolgreich zwischengespeichert.

### Priorität : Hoch

---


## User Story 4: Standardisierte Briefanrede generieren
**Als** Sachbearbeiter:in  
**möchte ich**, dass eine Briefanrede auf Basis der Ausgabe des Visitenkartenscanners (Zeichenkette) generiert wird,  
**um** die Qualität und Konsistenz von Korrespondenz sicherzustellen.

### Akzeptanzkriterien
- Die generierte Briefanrede verwendet alle relevanten Informationen: Anrede, Titel, Vorname und Nachname.
- Die Briefanrede entspricht der definierten Tabelle für Anreden (z. B. "Sehr geehrte Damen und Herren").

### Priorität : Hoch

---

## User Story 5: Doppelnamen formatieren
**Als** Sachbearbeiter:in  
**möchte ich**, dass Doppelnamen mit einem Bindestrich verbunden werden,  
**um** die Anrede leichter lesbarer zu gestalten.

### Akzeptanzkriterien
- Bei Doppelnamen oder ungewöhnlichen Formaten (z. B. Bindestriche) wird der Nachname korrekt interpretiert.
- Bei Doppelnamen wird der Bindestrich automatisch ergänzt.

### Priorität : Mittel

---

## User Story 6: Deutschsprachige Unterstützung für Anreden
**Als** Sachbearbeiter:in  
**möchte ich**, dass die Unterstüzung der deutsche Sprache, aber auch die potentzielle Erkennung anderer Sprachen gewährleistet ist,  
**um** eine internationale Korrespondenz zu ermöglichen.

### Akzeptanzkriterien
- Deutsch ist die Standard-Sprache.
- Den Nutzenden wird mitgeteilt wenn eine andere Sprache erkannt wurde.

### Priorität : Niedrig

---

# Definition of Done (DoD) 

Der Auftrag gilt als **fertiggestellt**, wenn alle der folgenden Kriterien erfüllt sind:

## **Allgemein**
- [X] Alle User Stories sind vollständig umgesetzt und erfüllen die definierten Akzeptanzkriterien.
- [X] Der Code ist in einer Versionsverwaltung (Git) sauber dokumentiert, inklusive beschreibender Commits.
- [X] Die Anwendung ist vollständig lauffähig auf einem Windows 11 PC und kann ohne Fehler ausgeführt werden.
- [X] Es existiert ein lauffähiger Build/Release, der die MVP-Funktionalität vollständig abbildet.

---

## **Clean-Code-Qualität**
- [X] Der Quellcode ist klar strukturiert, formatiert, modular aufgebaut und leicht verständlich.
- [X] Die Ordnerstruktur ist klar strukturiert modular aufgebaut und leicht verständlich.
- [X] "Hard Coding" wird vermieden.
- [X] Es werden Iterationen anstatt Rekursionen werden verwendet.
- [X] Alle externen Bibliotheken/Dependencies sind im Design dokumentiert.
- [X] Variablennamen befolgen Bennenungskonventionen.
- [X] Clean-Code-Konventionen werden eingehalten (< 500 Zeilen / < 3 Parameter / DRY-Prinzip).
- [X] Kommentaren sind sinnvoll genutzt, um Zweck und Funktionsweise verständlicher zu beschreiben.
- [X] Kommentare befolgen Kommentarkonventionen (auskommentierten Code-Blöcke / TODOs:).

---

## **Tests**
- [X] Unit-Tests decken alle implementierten Funktionen ab.
- [X] Alle Testfälle sind erfolgreich durchlaufen.
- [X] Es existieren Testfälle für alle kritischen Use-Cases, insbesondere:
  - Erkennung der Anrede, des Titel, des Vorname, des Nachname und des Geschlechts.
  - Trennung von Vor- und Nachname.
  - Generierung der Briefanrede.
  - Generierung des Bindestrichs bei Doppelnamen.
  - Fehlerhafte Eingaben (z. B. doppelte Anrede, fehlender Name) werden korrekt gehandhabt.
- [X] Manuelle Tests wurden durchgeführt, um die Funktionalität auf der Zielplattform zu validieren.

---

## **Design und Architektur**
- [X] Ein grobes Designkonzept liegt vor und ist in der Dokumentation enthalten.
- [X] Die Datenstruktur ist logisch und leicht strukturiert.
- [X] Das Programm ist so aufgebaut, dass durch Schnittstellen, zukünftige Erweiterungen (z. B. Datenbank-Anbindung) möglich wären.

---

## **Benutzerfreundlichkeit**
- [X] Die Anwendung ist intuitiv zu bedienen, mit klaren Hinweisen und Fehlermeldungen.
- [X] Bei manuellen Eingaben gibt es Eingabefelder, die die Nutzungsführung unterstützen.
- [X] Alle Felder (z. B. Titel, Vorname, Nachname, Geschlecht, Sprache) können vom den Benutzer:innen einfach überprüft und bearbeitet werden.

---

## **Dokumentation**
- [X] Eine vollständige und verständliche Dokumentation liegt vor, die folgende Punkte enthält:
  - Übersicht über die Funktionalitäten (User Stories, Akzeptanzkriterien).
  - Kurzanleitung zur Installation und Nutzung der Anwendung.
  - Beschreibung der Datenstruktur.
- [X] Release Notes dokumentieren technische Informationen und die Installationsanweisungen.

---

## **Abnahme**
- [X] Ein Review wurde mit mindestens einem Mitglied durchgeführt und alle identifizierten Probleme wurden behoben.

---

## **Qualitätssicherung**
- [X] Alle Anforderungen der Aufgabenstellung wurden vollständig erfüllt.
- [X] Die Gesamtbewertungskriterien der Aufgabe (MVP, User Stories, Tests, Release Notes, Funktionalität) sind abgedeckt und überprüft.

---

# **Kontakt-Splitter Design**

Die Anwendung "Kontakt-Splitter" bietet eine intuitive Nutzungsoberfläche, um Namen und zugehörige Informationen wie Titel, Vorname und Nachname zu analysieren, zu bearbeiten und für verschiedene Zwecke zu nutzen. Hier eine Beschreibung der einzelnen Bereiche und ihrer Funktionen:

---

## **UI-Design**

### **1. Namen scannen**
- **Eingabefeld:** Ganz oben befindet sich ein Textfeld, in das der vollständige Name eingegeben werden kann (z. B. "Herr Max Mustermann").
- **Schaltfläche "Namen scannen":** Mit einem Klick auf diese orangefarbene Schaltfläche wird der eingegebene Name analysiert und wird automatisch in ein Objekt mit den Bestandteilen diesen Namens umgewandelt (Titel, Vorname und Nachname).
- **KI-Ein- und Ausschalten:** Mit Einer Checkbox kann die Unterstüzung von KI, zur Ermittlung des Geschlechts anhand des Namens ein und ausgeschalten werden.

---

### **2. Modusauswahl**
Unter dem Bereich "Namen scannen" gibt es eine horizontale Leiste mit vier Hauptmodi (lila Schaltflächen), die unterschiedliche Funktionen bieten:

#### **Briefanrede:** 
Generiert basierend auf den analysierten Daten eine standardisierte Briefanrede. Die Anrede wird im unteren Bereich angezeigt (z. B. "Sehr geehrter Herr Mustermann"). Es gibt außerdem ein Dropdown-Menü, um die Sprache der Anrede zu ändern.
  
#### **Namen und Daten anpassen:** 

- **Bearbeitungsfelder:** 
  - "Titel", "Vorname" und "Nachname" werden einzeln aufgelistet, und jede Komponente kann manuell angepasst oder entfernt werden.
  - Zusätzliche Informationen wie Sprache und Geschlecht können hinzugefügt beziehungsweise geändert werden, wobei die Änderungen direkt wirksam werden.
- **Schaltflächen:** "Entfernen" entfernt eine Komponente, und "Komponente hinzufügen" erlaubt das Hinzufügen neuer Informationen.

#### **Eingabeverlauf:** 
Dieser Modus ist in der Lage den eingegebenen Namen in einer Kontaktliste **transistent** zu speichern, indem man die grüne Schaltfläche "Kontakt speichern drückt". Mithilfe den zweien blauen Schaltflächen "persistentes Speichern" und "persistent Laden" können die Benutzer:innen die Kontaktliste **persistent** speichern. Damit wird die Nutzungsfreundlichkeit enorm verbessert, da Kontakte auch nach Programmende nach Wunsch der Benutzer:innen wieder geladen werden können.

Kontakte die gespeichert wurden, können durch die blaue Schaltfläche "Bearbeiten" bearbeitet werden, wobei dann in der Modusauswahl "Namen und Daten anpassen" die Daten des Kontaktes reingeladen werden. Ebenfalls können diese Kontakte wiederrum auch mit der roten Schaltfläche "Löschen" entfernt werden.


#### **Optionen ergänzen:**
 Hier können neue Titel-, Anreden-, Geschlechts- und Briefanredenoptionen  ergänzt und **transistent** gespeichert werden, um die Analyse und Zuordnung weiter zu individualisieren.

 - **Titel hinzufügen:** \
 Für die Erweiterung der **Titelliste** ist ein Eingabefeld und ein Drop-Down mit verschiedenen Sprachen vorgesehen, die mit der blauen Schaltfläche "Hinzufügen" den neuen Titel speichert. 
 - **Geschlecht hinzufügen:**\
  Für das Hinzufügen eines neuen Geschlechts in die **Geschlechtsliste** gibt es auch ein Eingabenfeld mit einer "Hinzufügen"-Schaltfläche. 
 - **Anrede hinzufügen:**\
  Um eine neue Anrede in die **Anredeliste** zu speichern, wird ebenfalls ein Eingabefeld, sowie eine Drop-Down der verschiedenen Sprachen und ein Drop-Down mit den aktuell vorhandenen Geschlechtn bereitgestellt. Die Speicherung erfolgt ebenfalls durch die Aktivierung der blauen Schaltfläche "Hinzufügen".
 - **Briefanrede hinzufügen:** \
 Schlussendlich gibt es noch die Option eine neue Briefanrede in die **Briefanredensliste** einzufügen. Dies wird mithilfe eines Eingabefeldes, einer Sprache (Drop-Down), eines Geschlechts (Drop-Down) und einer Entscheidung (Nachname anhängen/ Nachnamen nicht anhängen) realisiert. Wie auch bei den anderen Optionen wird die Eingabe durch die blaue Schaltfläche "Hinzufügen" gespeichert. 
- **Listen anzeigen:**\
 Per Design-Entscheidung von Team Laura wurde festgelegt, dass die Listen in JSON-Datein verwaltet und abgerufen werden können. In dem MVP werden deshalb die Listen in demselben Ordner, in der auch die .exe liegt verwaltet. Die Benutzer:innen haben damit die Möglichkeit zu überprüfen, welche Sprachen, Titel, Anreden, Geschlechter und Briefanreden dieses Programm momentan unterstützt, wobei die Nutzungsfreundlichkeit aber auch die Nachvollziehbarkeit verbessert wird.
---

### **Anwendungsbeispiel**
1. **Eingabe eines Namens:** 
   - Geben Sie z. B. "Herr Dr. Max Mustermann" in das Textfeld ein und klicken Sie auf "Namen scannen". Der Name wird in "Anrede: Herr", "Titel: Dr.", "Vorname: Max", und "Nachname: Mustermann" aufgeteilt.

2. **Erstellung einer Briefanrede:** 
   - Wechseln Sie in den Modus "Briefanrede", und die Anwendung generiert automatisch die korrekte Anrede ("Sehr geehrter Herr Dr. Mustermann").

3. **Bearbeiten von Daten:**
   - Im Modus "Namen und Daten anpassen" können Sie etwa den Vornamen von "Max" zu "Alexander" ändern, oder andere Komponenten wie Anrede, Titel, Vorname oder Nachname hinzufügen, oder die bestehenden Attribute ändern. 

4. **Verwenden des Eingabeverlaufs:**
   - Speichern Sie diesen Kontakt ab, damit dieser im Eingabeverlauf erscheint.
   - Persistieren Sie diesen, indem Sie die entsprechende Schaltfläche betätigen.
   - Diesen können nun jederzeit (auch nach Programmende) aufrufen, indem Sie die persistente Liste laden (Dieser Schritt ersetzt auch die transistenten Kontakte, falls vorhanden).

5. **Ergänzen von Optionen:**
   - Fügen Sie einen neuen Titel oder ein neues Geschlecht in Kombination mit einer passenenden Anrede im Modus "Optionen ergänzen" hinzu.
---
## **Architektur-Design**
![Alt-Text](ContactSplitterKlassendiagramm.svg)

---

# Release Notes - Kontaktsplitter v1.0

## **Version**: 1.0  
## **Release Date**: 28.05.2025  

---

## **Zusammenfassung**
Diese Version enthält die erste stabile Veröffentlichung des Kontaktsplitters, einer Anwendung zur automatisierten Erkennung und Verarbeitung von Kontaktinformationen (Titel, Vorname, Nachname und Geschlecht). Die Anwendung wurde in Python entwickelt und als ausführbare Datei (.exe) für Windows 11 bereitgestellt.  

---

## **Neue Features**

### Namen Scannen
- **Eingabe und Scannen:** Nutzer:innen können eine Zeichenkette eingeben und diese analysieren lassen, um relevante Informationen wie Titel, Vorname, Nachname und Geschlecht zu extrahieren.
- **KI-Unterstützung:** Die KI kann ein- oder ausgeschaltet werden. Ist das Geschlecht aufgrund mangelnder Daten nicht bestimmbar (z. B. nur der Name ist gegeben), hilft die KI, eine Schätzung anhand von Namensmustern vorzunehmen.

---

### Automatische Erkennung von Titel, Namen und Geschlecht
- **Identifikation und Zuordnung:** Das Programm erkennt und speichert automatisch Titel, Vorname, Nachname und Geschlecht durch eine komplexe Logik, die über grundlegende Anforderungen hinausgeht.
- **Anrede-Erkennung:** Anreden werden erkannt, aber nicht gespeichert. Stattdessen wird bei der Erstellung einer Briefanrede eine passende, standardisierte Anrede aus einer vordefinierten Liste verwendet.

---

### Manuelle Anpassungen
- **Flexibilität:** Nutzer:innen können alle erkannten Attribute manuell anpassen, falls die automatische Zuordnung nicht eindeutig war.
- **Bearbeitung:** Attribute können bearbeitet, entfernt oder neu hinzugefügt werden.
- **Trennung von Vor- und Nachnamen:** Das Programm unterstützt die automatische Trennung von Vor- und Nachnamen sowie die Anpassung von Sprache und Geschlecht eines Kontakts.

---

### Generierung von Briefanreden
- **Automatisierte Erstellung:** Auf Basis der eingegebenen Informationen erstellt das Programm standardisierte Briefanreden in verschiedenen Sprachen.
- **Unterstützung für Doppelnamen:** Sowohl Vor- als auch Nachnamen mit Bindestrich werden korrekt formatiert.
- **Mehrsprachigkeit:** Die generierte Anrede kann problemlos in andere Sprachen geändert werden.

---

### Mehrsprachige Unterstützung
- **Verfügbarkeit:** Das Programm unterstützt die Sprachen Deutsch, Englisch, Französisch, Spanisch, Italienisch, Portugiesisch, Polnisch, Tschechisch, Rumänisch und Serbisch.

---

### Eingabeverlauf
- **Kontaktverwaltung:** Kontakte können temporär (transient) oder dauerhaft (persistent) zwischengespeichert werden, um auch nach einem Programmende wieder zugänglich zu sein.
- **Verlaufsgenerierung:** Ein übersichtlicher Verlauf wird erstellt, entweder durch das Laden persistenter Kontakte oder durch das Speichern neuer transienter Kontakte.
- **Bearbeitungsmöglichkeiten:** Kontakte im Verlauf können bearbeitet und entfernt werden. Änderungen müssen explizit gespeichert werden, um dauerhaft zu sein.
- **Datenkonsistenz:** Beim Laden persistenter Kontakte werden alle transienten Daten verworfen, es sei denn, sie wurden vorher persistent gespeichert.

---

### Erweiterbare Optionen
- **Anpassungsfähigkeit:** Nutzer:innen können neue Titel und Geschlechter hinzufügen, um das Programm an individuelle Anforderungen anzupassen.
- **Kontextuelle Briefanreden:** Anreden und Briefanreden mit speziellem Kontext können definiert und für die automatisierte Generierung genutzt werden.
- **Persistente Listen:** Alle Anpassungen werden in JSON-Listen gespeichert, die im selben Ordner wie die ausführbare Datei liegen und jederzeit erweitert oder bearbeitet werden können.

---

### UI-Feedback
- **Nutzungsfreundlichkeit:** Klare Fehlermeldungen und Hinweise verbessern die Bedienung und Nachvollziehbarkeit des Programms, was die Nutzungserfahrung optimiert.


### Definierte Logik der Namensaufteilung

#### **Namenszuordnung**
- **1 Name:** Wird als Nachname interpretiert.
- **2 Namen:** Erster Name wird als Vorname, zweiter Name als Nachname zugeordnet.
- **3 Namen:** Die ersten beiden Namen werden als Vornamen, der dritte als Nachname definiert.
- **4+ Namen:** Die ersten beiden Namen gelten als Vornamen, alle weiteren Namen werden als Nachnamen betrachtet.

#### **Sonderfall: Namensumkehrung durch Komma**
- Wenn ein Komma in der Eingabe erkannt wird, wird der Name nach folgender Regel verarbeitet:
  - Der Name rechts des Kommas wird als Vorname interpretiert.
  - Der Name links des Kommas wird als Nachname interpretiert.
- Beispiel: `Müller, Petra` wird zu:
  - Vorname: Petra
  - Nachname: Müller

#### **Erkennung von Titeln und Anreden**
- **Mehrsprachige Erkennung:** Titel und Anreden werden anhand einer hinterlegten Liste erkannt, unabhängig von ihrer Position im Namen.
- **Adelstitel:** Adelstitel werden zusammen mit den nachfolgenden Namen als Nachname betrachtet.

#### **Geschlechtserkennung**
- **Anhand der Anrede:** Wenn eine Anrede vorhanden ist, wird das Geschlecht direkt daraus abgeleitet.
- **Anhand des Namens:** Wenn keine Anrede vorliegt, wird das Geschlecht mithilfe der KI geschätzt. 
  - **Hinweis:** Die KI kann bei Bedarf deaktiviert werden. In diesem Fall wird das Geschlecht als "nicht ermittelbar" gekennzeichnet.

#### **Briefanreden-Logik**
- **Hinterlegte Kombinationen:** Für jede Kombination aus Geschlecht und Sprache kann eine spezifische Anrede definiert werden.
- **Generierung:** Bei der Erstellung einer Briefanrede wird überprüft ob diese Kombination vorliegt, um diese passende Anrede und Briefanrede zu benutzen.

---

## **Systemanforderungen**
- **Betriebssystem**: Windows 11 (64-bit)
- **Laufzeitumgebung**: Python 3.10+ (falls Quellcode verwendet wird)
- **RAM**: 2 GB (Minimum)  
- **Speicherplatz**: 100 MB

---
## **Installation**

### **Option 1: Download des Programms**

1. Laden Sie das bereitgestellte Release-Paket herunter.
2. Speichern Sie die Datei an einem gewünschten Speicherort auf Ihrem Computer.
3. Doppelklicken Sie auf die Datei `Kontaktsplitter_v1.0.exe`, um die Anwendung zu starten.

### **Option 2: Ausführung aus dem Quellcode**
Falls Sie den Quellcode ausführen möchten, gehen Sie wie folgt vor:

1. Laden Sie das Repository herunter oder klonen Sie es über Git:  
   
   git clone https://github.com/JonathanFleischmann/ContactSplitter.git

   pip install tinydb, tkinter, openai

   python main.py

---
## **Support**

Falls Sie auf Probleme stoßen oder Feedback geben möchten, kontaktieren Sie uns bitte unter:
---
i22006@hb.dhbw-stuttgart.de

i22032@hb.dhbw-stuttgart.de

i22021@hb.dhbw-stuttgart.de

Vielen Dank, dass Sie den Kontaktsplitter verwenden!
Ihr Entwicklungsteam Laura
   
# Anhang: KI-Einsatz bei der Geschlechtserkennung

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
- **Nutzungsfeedback:** Direkte Rückmeldungen von Anwendern zur Qualität und Korrektheit der Ergebnisse.

---

## **Fazit**
Der Einsatz der KI spart Zeit und Aufwand bei der Geschlechteranalyse. Allerdings erfordert die Verwendung zusätzlicher technischer Maßnahmen für die Integration, klare Tests und eine gute Dokumentation. Es bleibt wichtig, die KI-Ergebnisse zu validieren, insbesondere in kritischen Kontexten.


