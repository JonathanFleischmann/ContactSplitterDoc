# Abgabe-Dokumente für den Kontaktsplitter

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

