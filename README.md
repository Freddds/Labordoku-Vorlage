# README – LaTeX Labor Vorlage

----------------------------------------
AUFBAU DER VORLAGE
----------------------------------------

Das Hauptdokument ist main.tex.
Alle Inhalte werden von dort eingebunden.

----------------------------------------
KAPITELSTRUKTUR
----------------------------------------

Alle Kapitel liegen im Ordner:

chapters/

Dateien:
- introduction.tex  → Einleitung
- chapterX.tex      → Kapitel
- resume.tex        → Zusammenfassung

Jede Kapiteldatei beginnt direkt mit:

\chapter{Kapitelname}

Es wird kein \begin{document} in Kapiteldateien benötigt.

Kapitel werden in der main.tex eingebunden mit:

\input{chapters/chapter1.tex}

Nicht benötigte Kapitel können deaktiviert werden durch Kommentieren:

%\input{chapters/chapter1.tex}

Das ist auch hilfreich zur Fehlersuche.

----------------------------------------
BILDER
----------------------------------------

Bilder liegen im Ordner:

figures/

Empfohlen ist die Nutzung von Unterordnern pro Aufgabe oder Versuch.

Einbindung:

\includegraphics[width=0.8\textwidth]{figures/Unterordner/Bild.png}

Empfohlene Bildbreite:
0.75 – 0.95 \textwidth

----------------------------------------
LITERATURVERZEICHNIS (BibTeX)
----------------------------------------

Die Literatur liegt in:

literature.bib

Es wird BibTeX verwendet, daher werden Quellen nicht direkt in LaTeX geschrieben.

----------------------------------------
NEUE QUELLE HINZUFÜGEN
!WICHTIG! Das muss in die literature.bib
----------------------------------------

Beispiel:

@misc{label,
  author       = {Autor oder Organisation},
  title        = {Titel der Quelle},
  year         = {2026},
  institution  = {Hochschule Darmstadt},
  howpublished = {Moodle-Kursunterlage},
  note         = {Accessed: 2026-04-21}
}

Der Schlüssel (z.B. label) wird zum Zitieren verwendet.

----------------------------------------
QUELLE IM TEXT ZITIEREN
!WICHTIG! Das muss in die chapter Dateien.
----------------------------------------

\cite{label}

Nur zitierte Quellen erscheinen im Literaturverzeichnis, aber dies dann voll-automatisch.

----------------------------------------
Sollten die Quellen auch nach mehrfachem Kompilieren nicht kommen, empfehle ich 
----------------------------------------
