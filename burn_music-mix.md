# Musik-Mix auf CD brennen

### Was wird benötigt?

* Audacity (freie Software)
* CueListTool (freie Software)
* CDBurnerXP (freie Software)
* Der Musik-Mix als WAV-Datei
  * 44100 Hz Abtastrate
  * 16 Bit Auflösung
  * Dither: POW-r 3 (stark limitierte Musik)

### 1. CD-Tracks framegenau ermitteln

* Audacity starten
* `Datei // Importieren // Audio ...`
* die Musik-Mix-WAV-Datei wählen und laden
* alle Zeitanzeigen im unteren Breich auf CDDA-Frames einstellen
* auf den Anfang des gesamten Tracks zoomen
* einen kleinen Breich ab dem Beginn der Wellenform auswählen
* den Bereich abspielen und akkustisch prüfen
* mit Hilfe des Fingers kann der Start framegenau korrigiert werden

**Achtung**: Der erste Track sollte mit Digital-NULL beginnen, deshalb hier eine Pause bis zur Wellenform lassen!

* mit `Strg + B` eine Textmarke des Bereiches erzeugen
* den nächsten Track anspringen und einen kleinen Bereich am Übergang auswählen
* den Bereich abspielen und akkustisch prüfen
* mit Hilfe des Fingers kann der Start framegenau korrigiert werden
* mit `Strg + B` eine Textmarke des Bereiches erzeugen
* Die vorherigen vier Vorgänge sooft wiederholen, bis auch der letzte Track mit einer Textmarke versehen wurde

**Tipp**: Die Textmarke muss nur am Beginn des jeweiligen Tracks passen. Das Ende ist unerheblich.

* `Bearbeiten // Textmarken // Textmarken bearbeiten ... // Export ...`
* Die Textmarken als txt-Datei speichern

### 2. Cue-List-Datei anfertigen

* CueListTool starten
* `File // Open WAV file...`
* Originale MIX-WAV-Datei laden
* `File // Import // Audacity Labels (.txt)`
* Textmarkendatei auswählen und laden
* `File // Export // Cue Sheet (.cue)`
* sämtliche CD-Text und Zeit-Einstellungen deaktivieren
* Namen für Cue Sheet vergeben und speichern

### 3. CD mit Hilfe der Cue-List-Datei brennen

* CDBurnerXP starten
* im Brenn-Assistenten `Audio-CD` wählen
* `Datei // Importieren von // Cue Sheet...`
* Cue Sheet Datei wählen und laden
* Durch Doppelklick auf die Tracks die Titelanfänge prüfen
* Zusammenstellung brennen,
  * dabei `CD-Text` deaktivieren
  * und `Keine Pausen zwischen den Titeln` auswählen

