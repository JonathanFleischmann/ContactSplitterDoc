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

# Release Notes - Kontaktsplitter v1.0

## **Version**: 1.0  
## **Release Date**: 28.05.2025  

---

## **Zusammenfassung**
Diese Version enthält die erste stabile Veröffentlichung des Kontaktsplitters, einer Anwendung zur automatisierten Erkennung und Verarbeitung von Kontaktinformationen (Anrede, Titel, Vorname, Nachname, Geschlecht und einer Altersschätzung). Die Anwendung wurde in Python entwickelt und als ausführbare Datei (.exe) für Windows 11 bereitgestellt.  

---

## **Neue Features**
### 1. **Automatische Anrede- und Geschlechtserkennung**
- Identifikation, Zuordnung und Zwischenspeicherung von der Anrede, den Titel, den Vorname, den Nachname, dem Geschlecht und einer Altersschätzung.
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
   


