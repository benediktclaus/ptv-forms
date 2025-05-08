# PTV Formulare 
Für den Antrag auf Psychotherapie in Kostenerstattung

## Dependencies
- Schriftart [Roboto](https://fonts.google.com/specimen/Roboto)
- typst package `letter` vom meinem Account
- `config.typ` Datei, in der die Variablen `therapeut`, `anrede`, `arztregister-nr`, `berufsbezeichnung`, `praxisadresse` und `stempel` als typst content definiert sind, also in der Form von

```typ
#let therapeut = [Dr. Hieronymus Bosch]
```

## Argumente
Für die Hauptfunktion `ptv` können die folgenden Argumente vergeben werden:


Argument | Type | Erklärung
--- |--- | ---
therapeut | content | Name Therapeut
anrede | content | Anrede, bspw. `[Herr]` 
arztregister-nr | content | Nummer im Arztregister
berufsbezeichnung | content | Berufsbezeichnung, bspw. `[Psychologischer Psychotherapeut (VT)]`
praxisadresse | content | Adresse der Praxis
stempel | content | Stempel
krankenkasse | content | Krankenkasse Patient
krankenkasse-adresse | content | Adresse Krankenkasse
vorname | content | Vorname Patient
nachname | content | Nachname Patient
geburtsdatum | content | Geburtsdatum Patient
adresse | content | Adresse Patient
vnummer | content | Versichertennummer
diagnosen | array | Diagnose, array mit 3 contents, bspw. `([F32.0], [], [])`
einheiten-ebm | content | Anzahl Einheiten EBM
einheiten-gop | content | Anzahl Einheiten GOP
einheiten-ebm-bezugsperson | content | Anzahl Einheiten EBM mit Bezugspersonen
einheiten-gop-bezugsperson | content | Anzahl Einheiten GOP mit Bezugspersonen
ziffern-ebm | array | Ziffern EBM, array mit 3 contents, bspw. `([35425], [], [])`
ziffern-gop | array | Ziffern GOP, array mit 3 contents, bspw. `([A812K], [], [])`
ziffern-ebm-bezugsperson | array | Ziffern EBM, array mit 2 contents, bspw. `([], [])`
ziffern-gop-bezugsperson | array | Ziffern GOP, array mit 2 contents, bspw. `([], [])`
bisher-einzel | content | Bisherige Anzahl Sitzungen Einzeltherapie
bisher-gruppe | content | Bisherige Anzahl Sitzungen Gruppentherapie
bisher-einzel-ziffern | content | Bisherige Ziffern Einzeltherapie
bisher-gruppe-ziffern | content | Bisherige Ziffern Gruppentherapie
checks | array | array mit strings, die die Checkboxen identifizieren, siehe nächster Abschnitt
datum | content | Antragsdatum

## Checkboxen
Über das Argument `checks` (s.o.) kann gesteuert werden, in welche Checkboxen ein Kreuz gesetzt wird. Dabei werden einzelne Strings in ein array geschrieben, also z.B. `("erw", "lzt", "vt")`. Zur Auswahl stehen:
String | Checbox
--- | ---
"ap" | Analytische Psychotherapie
"tp" | Tiefenpsychologisch fundierte Therapie
"vt" | Verhaltenstherapie
"kombination" | Kombinationsbehandlung Einzel-/Gruppentherapie
"station-ja" | Stationäre oder rehabilitative Behandlung in den letzten 12 Monaten
"station-nein" | Keine stationäre oder rehabilitative Behandlung in den letzten 12 Monaten
"ambulant-ja" | Ambulante Psychotherapie in den letzten 2 Jahren
"ambulant-nein" | Keine ambulante Psychotherapie in den letzten 2 Jahren
"f70" | Es liegt eine Diagnose nach F70-F79 (ICD-10-GM) vor
"erw" | Für Erwachsene (Erw)
"kiju" | Für Kinder und Jugendliche (KiJu)
"ap" | Analytische Pschotherapie (AP)
"tp" | Tiefenpsychologisch fundierte Therapie (TP)
"vt" | Verhaltenstherapie (VT)
"kzt1" | Kurzzeittherapie 1 (KZT 1)
"kzt2" | Kurzzeittherapie 2 (KZT 2)
"lzt" | Langzeittherapie (LZT) als
"erstantrag" | Erstantrag
"umwandlung" | Umwandlung
"fortführung" | Fortführung
"einzel" | Ausschließlich Einzeltherapie
"gruppe" | Ausschließlich Gruppentherapie
"kombination" | Kombinationsbehandlung mit
"kombi-einzel" | Überwiegend Einzeltherapie
"kombi-gruppe" | Überwiegend Gruppentherapie
"kombi-zwei" | Kombinationsbehandlung durch zwei Therapeuten/Therapeutinnen