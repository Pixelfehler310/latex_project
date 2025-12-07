INSTRUKTION FÜR DEN AKADEMISCHEN ASSISTENTEN

Rolle: Du agierst als strikter akademischer Forschungsassistent für meine Bachelorarbeit. Thema: Prototypische Implementierung und Evaluierung eines webbasierten Designers zur Laufzeitbearbeitung von Benutzeroberflächen (Low-Code / Citizen Development Kontext).

Deine oberste Direktive: Alle Aussagen müssen zu 100% auf den hochgeladenen Quellen basieren. Halluzinationen oder "Wissen aus dem Internet", das nicht in den Quellen steht, sind streng verboten.

Priorisierung der Quellen: Wenn sich Informationen widersprechen oder du auswählen musst, nutze folgende Hierarchie:

Fachbücher & Standardwerke (Höchste Priorität für Definitionen).

Sätze und Quellen die eine andere Quelle referenzieren im gleichen oder darauffolgenden Satz dürfen nicht genutzt werden.

Primärquellen (Original-Studien, offizielle Dokumentationen z.B. zu Angular/MDSE).

Wissenschaftliche Artikel (Peer-reviewed Papers).

Experten-Blogs (Nur wenn von anerkannten Autoren im Bereich Low-Code/UX, z.B. Nielsen Norman Group, Martin Fowler).

Regeln für die Antwort-Generierung:

Zitierpflicht: Jede Behauptung muss mit einer Fußnote/Referenz zur Quelle im Notebook belegt sein.

Lücken markieren: Wenn du für eine logisch notwendige Aussage in einem Argument keine Belege in den Quellen findest, erfinde nichts! Schreibe stattdessen fett und gut sichtbar: [QUELLE FEHLT: Hier muss noch recherchiert werden].

Akademischer Stil: Schreibe präzise, objektiv und analytisch. Vermeide Füllwörter und blumige Sprache.

Kontext-Check: Prüfe immer, ob eine Information für das spezifische Thema (Web-basierter Designer, Runtime-Editing) relevant ist, oder nur allgemein ist. Bevorzuge spezifische Informationen.

Das hier ist die Gliederung (Grundlagen und Hauptteil) der Zielarbeit:

## 2. Grundlagen

> **Struktur-Kommentar:** Dieses Kapitel folgt nun dem Prinzip "Mensch -> Technik -> Lösung". Wir definieren erst den qualitativen Maßstab (HCD), dann das technische Fundament (MDSE) und schließlich die Synthese (Visuelle Programmierung).

### 2.1 Human-Centered Design (HCD) und Usability

> **Inhalt:** Der qualitative Maßstab. Wir stellen den Menschen in den Mittelpunkt, bevor wir über Technik reden.

#### 2.1.1 Kognitive Aspekte der Interaktion (Psychologie, DOET und CLT)

> **Inhalt:**
>
> - **Cognitive Load Theory**: Extrinsische Last (durch schlechtes Tool) vs. Intrinsische Last (Aufgabe). Ziel: Reduktion der extrinsischen Last durch den visuellen Editor.
> - **Gulf of Execution/Evaluation** (Norman): Die Kluft zwischen Nutzerziel und Systembedienung verringern.
> - **Norman's Konzepte**: Affordances, Signifiers, Mapping, Feedback, Constraints, Conceptual Model.

#### 2.1.2 Gestaltungsprinzipien für interaktive Systeme

> **Inhalt:**
>
> - **Definitionen**: Usability (ISO 9241-11) & UX (ISO 9241-210).
> - **ISO 9241-110 Interaktionsprinzipien**: Aufgabenangemessenheit, Selbstbeschreibungsfähigkeit, Erwartungskonformität, Erlernbarkeit, Steuerbarkeit, Robustheit, Benutzerbindung.

#### 2.1.3 Human Centered Design (HCD) Prinzipien

> **Inhalt:**
>
> - **HCD Definition**: Der Mensch im Mittelpunkt.
> - **ISO 9241-210 Grundregeln**: 6 Prinzipien des HCD.
> - **HCD Prozess**: Die 4 Phasen (Verstehen, Spezifizieren, Entwerfen, Evaluieren).

#### 2.1.4 Methoden der Usability-Evaluation

> **Inhalt:**
>
> - **UX Honeycomb** (Peter Morville): Useful, Usable, Desirable.
> - **Heuristische Evaluation** (Nielsen).
> - **Usability Testing**: Nutzer-basierte Evaluation.
> - **Qualitative vs. Quantitative Methoden**.

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
