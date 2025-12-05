# Gliederung der Bachelorarbeit

> **Titel (Arbeitstitel):** Prototypische Implementierung und Evaluierung eines webbasierten Designers zur Laufzeitbearbeitung von Benutzeroberflächen
>
> **Ziel der Gliederung:** Diese Struktur dient als Skelett für die Bachelorarbeit. Sie ist wissenschaftlich aufgebaut und führt logisch vom Problem über die theoretischen Grundlagen hin zur praktischen Lösung und deren Bewertung.
>
> **Roter Faden:**
>
> 1.  **Problem:** Die aktuelle UI-Erstellung mittels XML ist ineffizient, fehleranfällig und nur für Entwickler machbar.
> 2.  **Lösungsidee:** Ein visueller "Low-Code"-Designer soll dies vereinfachen und Fachexperten ("Citizen Developers") befähigen.
> 3.  **Theorie:** Wir stützen uns auf MDSE (technische Basis), Low-Code (Konzept) und HCD/Usability (Qualitätsmaßstab).
> 4.  **Praxis:** Wir analysieren den Ist-Zustand, konzipieren den Designer nach HCD-Prinzipien und setzen ihn prototypisch um.
> 5.  **Beweis:** Wir evaluieren den Prototypen gegen den alten XML-Editor, um die Verbesserung zu belegen.

---

## 1. Einleitung

### 1.1 Motivation und Problemstellung

> **Inhalt:**
>
> - Einführung in das Umfeld: Enterprise Software, Notwendigkeit von Anpassbarkeit und Standardisierung.
> - Beschreibung des Status Quo: UI-Definition über komplexe XML-Dateien (`meta.xml`, `view.xml`).
> - Das Problem: Dieser Prozess ist technisch anspruchsvoll, fehleranfällig (kein visuelles Feedback), langsam ("Time-to-Market") und schließt Fachexperten aus.
> - Der Trend: Wandel hin zu Low-Code und Empowerment der Fachbereiche.

### 1.2 Zielsetzung der Arbeit

> **Inhalt:**
>
> - Hauptziel: Entwicklung eines webbasierten, visuellen Designers (WYSIWYG) für die Laufzeitbearbeitung von UIs.
> - Teilziele:
>   - Reduzierung der technischen Hürden (Demokratisierung/Citizen Development).
>   - Steigerung der Effizienz bei UI-Anpassungen.
>   - Vermeidung von Medienbrüchen (Direkte Manipulation statt Code).
> - Forschungsfrage (implizit): Inwiefern kann ein visueller Editor die Effizienz und Usability im Vergleich zur XML-basierten Konfiguration steigern?

### 1.3 Aufbau der Arbeit

> **Inhalt:**
>
> - Kurzer Überblick über die folgenden Kapitel und deren logischen Zusammenhang.

---

## 2. Grundlagen

> **Struktur-Kommentar:** Dieses Kapitel folgt nun dem Prinzip "Mensch -> Technik -> Lösung". Wir definieren erst den qualitativen Maßstab (HCD), dann das technische Fundament (MDSE) und schließlich die Synthese (Visuelle Programmierung).

### 2.1 Human-Centered Design (HCD) und Usability

> **Inhalt:** Der qualitative Maßstab. Wir stellen den Menschen in den Mittelpunkt, bevor wir über Technik reden.

#### 2.1.1 Kognitive Aspekte der Interaktion (Psychologie, DOET und CLT)

> **Inhalt:**
>
> - **Problem**: Nutzersysteme mit schlechter Usability führen zu hoher kognitiver Last und Fehleranfälligkeit. -> Beispiel!
> - **Norman's Konzepte**: Affordanzen, Signifiers, Mapping, Feedback, Constraints, Conceptual Model.
> - **Cognitive Load Theory**: Extrinsische Last (durch schlechtes Tool) vs. Intrinsische Last (Aufgabe). Ziel: Reduktion der extrinsischen Last durch den visuellen Editor.
> - **Gulf of Execution/Evaluation** (Norman): Die Kluft zwischen Nutzerziel und Systembedienung verringern.
> - **Definitionen Usability & User Experience** (ISO 9241-11, ISO 9241-210 und weitere finden)
> - Reihenfolge Variabel!

#### 2.1.2 Human Centered Design (HCD) Prinzipien

> **Inhalt:**
>
> - **Aus 2.1.1 ableitbare Designprinzipien**
> - **kognitive zusammenfassung der wichtigsten Heuristiken, mit Fokus auf ISO NORM 9241:210:2010**: (Additiv und als BOnus quellen: Norman, Shneiderman, Nielsen, Honeycomb)
> - **Feedback & Feedforward**: Nutzerführung.
> - **Konsistenz**: Erwartungskonformität.
>   Dialoggestaltungs prinzipien (9241-110)
> - explizit NICHT hier drin: Direkte und indirekte Manipulation und WYSIWYG (kommt in 2.3.1)

#### 2.1.3 Gestaltungsprinzipien für interaktive Systeme

> **Inhalt:**
>
> - **Aus 2.1.1 ableitbare Designprinzipien**
> - **kognitive zusammenfassung der wichtigsten Heuristiken, mit Fokus auf ISO NORM 9241:210:2010**: (Additiv und als BOnus quellen: Norman, Shneiderman, Nielsen, Honeycomb)
> - **Feedback & Feedforward**: Nutzerführung.
> - **Konsistenz**: Erwartungskonformität.
>   Dialoggestaltungs prinzipien (9241-110)
> - explizit NICHT hier drin: Direkte und indirekte Manipulation und WYSIWYG (kommt in 2.3.1)

#### 2.1.4 Methoden der Usability-Evaluation

> **Inhalt:**
>
> - **UX Honeycomb** (Peter Morville): Useful, Usable, Desirable. (WICHTIG für die spätere Nutzwertanalyse, liefert die Kategorien)
> - **Heuristische Evaluation** (Nielsen).
> - **Usability Testing** (Nutzerbasierte Evaluation).
> - **Qualitative vs. Quantitative Methoden**.
> - **Ggf weitere Methoden wenn sinnvoll**

### 2.2 Modellgetriebene Softwareentwicklung (MDSE)

> **Inhalt:** Das technische Fundament. Software wird durch Modelle statt Code beschrieben.

#### 2.2.1 Kernelemente und Konzepte der MDSE

> **Inhalt:**
>
> - Definition von **Modell** (Abstraktion) und **Metamodell** (Grammatik/Regelwerk).
> - Unterscheidung: **Modell-Transformation** (Code-Generierung) vs. **Modell-Interpretation** (Laufzeit).
> - Bezug zum Projekt: Die XMLs sind Modelle, die Web-App ist der Interpreter.
> - _Literatur:_ Stahl/Völter, OMG Standards (MOF).

#### 2.2.2 Textuelle Domänenspezifische Sprachen (DSLs)

> **Inhalt:**
>
> - Was sind DSLs? (Spezialisierte Sprachen für ein Problemfeld).
> - Klassifikation: Externe DSLs (wie hier XML/XSD) vs. Interne DSLs.
> - Konkrete Syntax (XML) vs. Abstrakte Syntax (Baumstruktur).
> - _Literatur:_ Martin Fowler (Domain-Specific Languages).

### 2.3 Visuelle Programmierung und Low-Code-Plattformen

> **Inhalt:** Die Synthese. Wir nutzen MDSE-Technik, um HCD-Ziele zu erreichen.

#### 2.3.1 Paradigmen Visueller Programmiersprachen (VPLs)

> **Inhalt:**
>
> - Definition VPL: Programmierung durch Manipulation grafischer Elemente.
> - **WYSIWYG (What You See Is What You Get):** Das zentrale Interaktionsparadigma für direkte Manipulation.
> - Historie und Ansätze (Datenfluss, Blockbasiert).
> - Vorteile: Geringere Einstiegshürde, Übersichtlichkeit.

#### 2.3.2 Low-Code/No-Code als moderne Anwendungsform

> **Inhalt:**
>
> - Definition Low-Code: MDSE + Visuelle Tools + Minimales Coding.
> - Architektur von Low-Code-Plattformen (Visueller UI-Builder).
> - Der **Citizen Developer**: Befähigung von Fachexperten ohne tiefes IT-Wissen.
> - _Literatur:_ Gartner/Forrester Reports, Fachbücher zu Low-Code.

---

## 3. Analyse des Ist-Zustandes und Anforderungen

> **Struktur-Kommentar:** Wir analysieren zuerst das Problem aus Nutzersicht (HCD), dann die technischen Ursachen (MDSE).

### 3.1 Analyse des Nutzungskontexts und der Probleme

> **Inhalt:**
>
> - **Zielgruppen-Analyse:** Wer sind die Nutzer? (Entwickler, Consultants).
> - **Der aktuelle Workflow:** Wie entsteht eine View heute? (Manuelles Editieren, Deployment, Testen).
> - **Identifizierte Schwachstellen:** Hohe Fehleranfälligkeit (Syntaxfehler), "Blindflug" (kein visuelles Feedback), hohe kognitive Last.

### 3.2 Analyse der bestehenden Systemarchitektur

> **Inhalt:**
>
> - Technische Beschreibung: Wie hängen `meta.xml`, `view.xml` und der Interpreter zusammen?
> - Warum ist XML technisch notwendig, aber für den Menschen schlecht? (Trennung von konkreter Syntax und abstrakter Syntax).

### 3.3 Ableitung der Anforderungen an den visuellen Designer

> **Inhalt:**
>
> - **HCD-Ziele:** Reduktion der kognitiven Last, Ermöglichung von Citizen Development.
> - **Funktionale Anforderungen:** Baumstruktur anzeigen, Drag & Drop, Eigenschafts-Editor, WYSIWYG-Preview.
> - **Nicht-funktionale Anforderungen:** Usability (Erlernbarkeit), Performance, Integrierbarkeit.

---

## 4. Konzeption des visuellen Designers

> **Struktur-Kommentar:** Erst die Lösung für den Nutzer (UI/Interaktion), dann die technische Umsetzung (Architektur).

### 4.1 Interaktionskonzept und UI-Design

> **Inhalt:**
>
> - **Layout des Designers:** Zweiteilung (oder Dreiteilung) des Screens.
>   - Links: Strukturbaum (Metamodell-Quelle).
>   - Mitte/Rechts: Live-Preview (WYSIWYG).
>   - Rechts/Unten: Property-Panel (Detail-Konfiguration).
> - **Interaktionsmuster:** Drag & Drop von Feldern in die Preview. Direkte Selektion in der Preview.

### 4.2 Architekturkonzept und Datenmodell

> **Inhalt:**
>
> - **Integration:** Einbettung in die bestehende Angular-Architektur.
> - **Datenmodell:** Wie wird das visuelle Modell intern repräsentiert? (Abstrakter Syntaxbaum im Browser).
> - **Round-Trip:** Mapping-Logik zwischen visueller Repräsentation und XML/JSON.
> - **Validierung:** Sicherstellung gültiger Konfigurationen gemäß Metamodell.

---

## 5. Prototypische Implementierung

> **Struktur-Kommentar:** HCD Phase 3: Umsetzen. Beschreibung der technischen Realisierung.

### 5.1 Technologische Basis und Entwicklungsumgebung

> **Inhalt:**
>
> - Verwendetes Framework (Angular).
> - Genutzte Bibliotheken (z.B. für Drag & Drop, State Management).

### 5.2 Umsetzung der Kernkomponenten

> **Inhalt:**
>
> - **Der Strukturbaum:** Implementierung der Anzeige der verfügbaren Meta-Daten.
> - **Die Live-Preview:** Realisierung des WYSIWYG-Renderings (Nutzung der bestehenden Interpreter-Logik?).
> - **Der Property-Editor:** Dynamische Generierung von Eingabemasken für Feld-Eigenschaften.
> - **Drag & Drop Logik:** Technische Umsetzung der Verschiebe-Operationen.

### 5.3 Herausforderungen und Lösungsansätze

> **Inhalt:**
>
> - Technische Hürden während der Entwicklung (z.B. Synchronisation zwischen Modell und View, Performance, Komplexität der Verschachtelung).
> - Wie wurden diese gelöst?

---

## 6. Evaluierung und Diskussion

> **Struktur-Kommentar:** HCD Phase 4: Evaluieren. Der Beweis, dass die Lösung das Problem behebt.

### 6.1 Methodik der Evaluierung

> **Inhalt:**
>
> - Beschreibung des Vorgehens: Vergleich "Alter Prozess (XML)" vs. "Neuer Prozess (Designer)".
> - Gewählte Methoden (aus Kapitel 2.3.3): z.B. Heuristische Evaluation, Nutzwertanalyse, SWOT.

### 6.2 Durchführung der Evaluierung

> **Inhalt:**
>
> - **Nutzwertanalyse:** Bewertung anhand definierter Kriterien (Erlernbarkeit, Effizienz, Fehleranfälligkeit).
> - **SWOT-Analyse:** Strengths, Weaknesses, Opportunities, Threats des neuen Ansatzes.
> - **Qualitativer Vergleich:** Gegenüberstellung der Workflows (Schritte im XML-Editor vs. Schritte im Designer).

### 6.3 Diskussion der Ergebnisse

> **Inhalt:**
>
> - Interpretation der Daten: Wurden die Ziele (Kapitel 1.2) erreicht?
> - Bestätigung: Der Designer senkt die Hürden und erhöht die Effizienz (Reduktion kognitive Last).
> - Kritische Reflexion: Wo hat der Prototyp noch Schwächen? (z.B. komplexe Spezialfälle, Performance bei riesigen Views).

---

## 7. Fazit und Ausblick

### 7.1 Zusammenfassung der Ergebnisse

> **Inhalt:**
>
> - Kurze Rekapitulation: Problem -> Lösung -> Ergebnis.
> - Kernaussage: Visuelle Programmierung ermöglicht Citizen Development im Enterprise-Kontext.

### 7.2 Kritische Reflexion und Limitationen

> **Inhalt:**
>
> - Ehrliche Betrachtung der Grenzen der Arbeit (z.B. Prototyp-Status, noch nicht produktiv im Einsatz, begrenzte Feature-Menge).

### 7.3 Ausblick

> **Inhalt:**
>
> - Zukünftige Erweiterungen: Full-Roundtrip (XML -> Designer -> XML), Erweiterung auf andere Modell-Typen (Workflows), Integration von KI-Assistenz.
