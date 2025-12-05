# Masterplan für die Bachelorarbeit

> **Status:** In Bearbeitung
> **Aktuelle Phase:** 2 von 7

Dieser Masterplan dient als detaillierte Roadmap für das Schreiben der Bachelorarbeit. Er enthält inhaltliche Stichpunkte, Argumentationslinien und konkrete Literaturvorschläge für jedes Kapitel.

---

## Phase 1: Grundlagen MDSE (Kapitel 2.1)

Dieses Kapitel legt das **technische Fundament**. Es ist essenziell, um zu verstehen, _warum_ das aktuelle System so aufgebaut ist (XMLs als Modelle) und _worauf_ der neue Designer aufsetzt. Wir bewegen uns hier auf einer abstrakten, software-technischen Ebene.

### 2.1 Modellgetriebene Softwareentwicklung (MDSE)

**Ziel des Kapitels:** Dem Leser erklären, dass wir Software nicht als Code, sondern als abstrakte Modelle betrachten. Dies legitimiert den Ansatz, UIs über XMLs zu definieren.

#### 2.1.1 Kernelemente und Konzepte der MDSE

- **Definition "Modell":**
  - Ein Modell ist eine Abstraktion der Realität, die für einen bestimmten Zweck erstellt wurde.
  - Es reduziert Komplexität, indem es unwichtige Details weglässt (Abstraktionsmerkmal).
  - _Argumentation:_ In unserem Fall ist die `view.xml` ein Modell der Benutzeroberfläche. Sie abstrahiert von HTML/CSS-Details.
- **Das Metamodell (Die "Grammatik"):**
  - Erklärung, dass jedes Modell Regeln braucht. Das Metamodell definiert, welche Elemente es gibt (z.B. "Es gibt Buttons und Textfelder") und wie sie verknüpft werden dürfen.
  - Bezug zur **4-Schichten-Architektur der OMG (MOF)**:
    - **M3 (Meta-Meta-Modell):** Die Sprache, um Metamodelle zu schreiben (hier: XSD-Schema-Sprache).
    - **M2 (Metamodell):** Die konkrete Definition unserer Sprache (hier: `view.xsd` und `meta.xsd`).
    - **M1 (Modell):** Die Instanz, die wir schreiben (hier: `view.xml`).
    - **M0 (Realität/Laufzeit):** Das laufende System (die gerenderte Angular-Komponente).
- **Transformation vs. Interpretation:**
  - **Modell-Transformation (Generierung):** Aus dem Modell wird Code (Java/TS) generiert (Compile-Time).
  - **Modell-Interpretation (Laufzeit):** Eine Engine liest das Modell zur Laufzeit und führt es aus.
  - _Argumentation:_ Unser System nutzt **Interpretation**. Das ermöglicht die "Laufzeitbearbeitung" (Thema der Arbeit!), da kein Kompilierschritt nötig ist. Änderungen am Modell (XML/JSON) wirken sofort.

**📚 Literatur & Quellen:**

- **Stahl, T., & Völter, M. (2006).** _Model-Driven Software Development: Technology, Engineering, Management_. Wiley.
  - _Das Standardwerk. Nutze es für Definitionen von Modell, Metamodell und Transformation._
- **Brambilla, M., Cabot, J., & Wimmer, M. (2017).** _Model-Driven Software Engineering in Practice_. Morgan & Claypool.
  - _Sehr gut für die Erklärung der OMG-Standards und modernere Einordnungen._
- **Object Management Group (OMG).** _Meta Object Facility (MOF) Core Specification_.
  - _Primärquelle für die 4-Schichten-Architektur (M0-M3)._

#### 2.1.2 Textuelle Domänenspezifische Sprachen (DSLs)

**Ziel des Kapitels:** Die XML-Dateien als das klassifizieren, was sie wissenschaftlich sind: Eine DSL.

- **Definition DSL:**
  - Eine Sprache, die auf ein spezifisches Problemfeld (Domain) fokussiert ist, im Gegensatz zu General Purpose Languages (GPL) wie Java.
  - Unsere Domain: "Definition von Enterprise-UIs".
- **Klassifikation:**
  - **Interne DSL:** Nutzt die Syntax einer Wirtssprache (z.B. Fluent API in Java).
  - **Externe DSL:** Hat eine eigene Syntax und braucht einen eigenen Parser (z.B. XML, SQL).
  - _Argumentation:_ Wir nutzen eine **externe, textuelle DSL** auf XML-Basis.
- **Konkrete vs. Abstrakte Syntax:**
  - **Konkrete Syntax:** Das, was der Nutzer sieht/schreibt (die spitzen Klammern im XML).
  - **Abstrakte Syntax (AST):** Die Baumstruktur der Informationen im Hintergrund (das, was der Parser daraus macht).
  - _Überleitung:_ Der neue visuelle Designer ändert nur die **konkrete Syntax** (von Text zu Grafik), die **abstrakte Syntax** (das Modell dahinter) bleibt gleich. Das ist ein zentraler Punkt für das Verständnis der Arbeit!

**📚 Literatur & Quellen:**

- **Fowler, M. (2010).** _Domain-Specific Languages_. Addison-Wesley.
  - _Die "Bibel" für DSLs. Hier findest du alle Definitionen zu Internal/External DSLs und Syntax._
- **Voelter, M. (2013).** _DSL Engineering: Designing, Implementing and Using Domain-Specific Languages_. dslbook.org.
  - _Detaillierte Konzepte zu Syntax und der Trennung von konkreter/abstrakter Syntax._

---

## Phase 2: Grundlagen Low-Code & Visuelle Programmierung (Kapitel 2.2)

Dieses Kapitel schlägt die Brücke von der Theorie (MDSE) zur modernen Praxis. Es erklärt, wie wir die abstrakten Modelle für Menschen zugänglich machen, die keine Informatiker sind.

### 2.2 Visuelle Programmierung und Low-Code-Plattformen

**Ziel des Kapitels:** Den neuen Designer als "Visuelle Programmiersprache" (VPL) und Teil der "Low-Code"-Bewegung einordnen.

#### 2.2.1 Paradigmen Visueller Programmiersprachen (VPLs)

- **Definition VPL:**
  - Programmierung, bei der grafische Elemente (Icons, Blöcke, Diagramme) statt Text manipuliert werden.
  - _Argumentation:_ Unser Designer ist eine VPL, da er die Logik der UI (welches Feld kommt wohin?) visuell abbildet.
- **Paradigmen:**
  - **Kontrollfluss-orientiert:** (z.B. Flussdiagramme).
  - **Datenfluss-orientiert:** (z.B. LabVIEW).
  - **Block-basiert:** (z.B. Scratch).
  - _Einordnung:_ Unser Ansatz ist eher **struktur-orientiert** (Baumstruktur der UI), was eine spezielle Form ist.
- **Vorteile:**
  - Reduktion von Syntaxfehlern (man kann Blöcke oft nicht falsch zusammenstecken).
  - Bessere Übersichtlichkeit ("Cognitive Dimensions of Notations").

**📚 Literatur & Quellen:**

- **Burnett, M. M. (1999).** _Visual Programming_. In Encyclopedia of Electrical and Electronics Engineering. Wiley.
  - _Klassische Definition und Historie._
- **Shu, N. C. (1988).** _Visual Programming_. Van Nostrand Reinhold.
  - _Ein Klassiker, der die Grundlagen legt (auch wenn alt, gut für die Historie)._

#### 2.2.2 Low-Code/No-Code als moderne Anwendungsform

- **Definition Low-Code (LCNC):**
  - Low-Code nutzt MDSE-Prinzipien + Visuelle Tools, um die Entwicklung zu beschleunigen.
  - Unterschied Low-Code (für Entwickler, erlaubt Code) vs. No-Code (für Fachanwender, kein Code).
  - _Argumentation:_ Unser Designer macht das bestehende MDSE-System zu einer Low-Code-Plattform.
- **Architektur von LCAPs (Low-Code Application Platforms):**
  - Typischerweise: Visueller UI-Builder + Daten-Modellierer + Logik-Designer.
  - Wir bauen den "Visuellen UI-Builder"-Teil.
- **Der "Citizen Developer":**
  - Definition: Fachexperte (Business User), der Anwendungen erstellt.
  - **Demokratisierung der Softwareentwicklung:** Die Macht verschiebt sich von der IT in die Fachabteilung.
  - _Argumentation:_ Das ist das strategische Ziel der Arbeit (Business Empowerment).

**📚 Literatur & Quellen:**

- **Sahay, A., Indamutsa, A., Di Ruscio, D., & Pierantonio, A. (2020).** _Supporting the understanding of low-code development platforms: a systematic mapping study_. Journal of Systems and Software.
  - _Exzellente wissenschaftliche Quelle, die Low-Code akademisch definiert und abgrenzt._
- **Gartner / Forrester Reports.** (z.B. _Magic Quadrant for Enterprise Low-Code Application Platforms_).
  - _Hieraus zitierst du die Definitionen von "Citizen Developer" und Markttrends. Das sind die Standardquellen für diese Begriffe._
- **Waszkowski, R. (2019).** _Low-Code Platform: A New Approach in Software Development_.
  - _Paper über die Vorteile und Architektur._

---

## Phase 3: Grundlagen Usability & HCD (Kapitel 2.3)

Hier definieren wir die Qualitätsmaßstäbe für den neuen Designer. "Er soll besser sein" ist keine wissenschaftliche Aussage. "Er soll eine höhere Usability nach ISO 9241-210 aufweisen" schon.

### 2.3 Human-Centered Design (HCD)

**Ziel des Kapitels:** Den Prozess beschreiben, den du in der Arbeit durchlaufen hast (Analyse -> Konzept -> Prototyp -> Evaluation).

#### 2.3.1 Der Prozess nach ISO 9241-210

- **Definition:**
  - HCD ist ein Ansatz zur Systementwicklung, der darauf abzielt, Systeme gebrauchstauglich zu machen, indem er sich auf die Nutzer, ihre Bedürfnisse und Anforderungen konzentriert.
- **Die 4 Phasen (Iterativ):**
  1.  **Nutzungskontext verstehen:** Wer sind die Nutzer (Entwickler/Consultants)? Was wollen sie erreichen (UI bauen)?
  2.  **Nutzungsanforderungen spezifizieren:** Was muss das Tool können? (z.B. Drag & Drop, Property-Editor).
  3.  **Gestaltungslösungen entwerfen:** Prototyping (Mockups, dann Code).
  4.  **Lösungen evaluieren:** Testen gegen die Anforderungen.
  - _Argumentation:_ Deine Arbeit folgt exakt diesem Zyklus. Das Kapitel "Hauptteil" ist die praktische Umsetzung dieser Theorie.

**📚 Literatur & Quellen:**

- **ISO 9241-210:2019.** _Ergonomics of human-system interaction — Part 210: Human-centred design for interactive systems_.
  - _Die absolute Primärquelle. Muss zitiert werden._
- **Benyon, D. (2014).** _Designing Interactive Systems: A Comprehensive Guide to HCI, UX and Interaction Design_. Pearson.
  - _Gutes Lehrbuch für die Details der Phasen._

### 2.3.2 Usability-Engineering für Entwicklungswerkzeuge

**Ziel des Kapitels:** Spezifische Kriterien für "Developer Tools" einführen. Ein Tool für Experten muss anders funktionieren als eine App für Endkunden.

- **Usability vs. User Experience (UX):**
  - **Usability:** Effektivität, Effizienz, Zufriedenheit (objektiv messbar).
  - **UX:** Umfasst auch emotionale Aspekte (Vorfreude, Vertrauen).
  - _Fokus:_ Wir konzentrieren uns primär auf **Effizienz** (Zeitersparnis) und **Effektivität** (Fehlervermeidung).
- **Cognitive Dimensions of Notations (CDN):**
  - Ein Framework speziell für die Bewertung von (visuellen) Programmiersprachen.
  - **Wichtige Dimensionen für dich:**
    - **Viscosity (Zähigkeit):** Wie schwer ist es, eine kleine Änderung zu machen? (Text ist oft weniger "zäh" als Grafik -> Herausforderung für VPLs!).
    - **Visibility:** Wie leicht sieht man Abhängigkeiten?
    - **Premature Commitment:** Muss man Entscheidungen treffen, bevor man alle Infos hat?
  - _Argumentation:_ Du nutzt CDN, um zu erklären, warum XML (Text) manchmal nervig ist (hohe kognitive Last durch Syntax) und wo der grafische Editor helfen soll (bessere Visibility).

**📚 Literatur & Quellen:**

- **Green, T. R. G., & Petre, M. (1996).** _Usability Analysis of Visual Programming Environments: A ‘Cognitive Dimensions’ Framework_. Journal of Visual Languages & Computing.
  - _Das wichtigste Paper für die Bewertung von visuellen Sprachen. Goldstandard._
- **Nielsen, J. (1993).** _Usability Engineering_. Morgan Kaufmann.
  - _Klassiker für die Definition von Usability-Attributen._

---

## Phase 4: Analyse & Anforderungen (Kapitel 3)

Jetzt verlassen wir die Theorie und wenden den HCD-Prozess (aus Phase 3) auf dein konkretes Projekt an.

### 3.1 Ist-Analyse (Context of Use)

**Ziel des Kapitels:** Das Problem so schmerzhaft wie möglich beschreiben. Warum brauchen wir überhaupt einen Designer?

- **Der aktuelle Workflow:**
  - Entwickler schreibt XML -> Speichert -> Wartet auf Reload -> Sieht Ergebnis -> Korrigiert XML.
  - _Problem:_ Hoher "Gulf of Evaluation" (Kluft zwischen Systemzustand und Wahrnehmung). Man sieht nicht sofort, was man tut.
- **Zielgruppen-Analyse:**
  - **Primär:** Softwareentwickler (kennen XML, wollen Speed).
  - **Sekundär:** Technical Consultants / Citizen Developers (kennen Business-Logik, hassen Syntax-Fehler).
  - _Ableitung:_ Das Tool darf nicht "dumm" sein (zu einfach), es muss Power-User-Features haben, aber Syntax-Fehler verhindern.

### 3.2 Anforderungsanalyse (User Requirements)

**Ziel des Kapitels:** Eine harte Liste von Kriterien erstellen, gegen die später evaluiert wird.

- **Funktionale Anforderungen (Was muss es können?):**
  - **F1 Visualisierung:** Baumstruktur muss grafisch dargestellt werden.
  - **F2 Manipulation:** Drag & Drop von Elementen.
  - **F3 Parametrisierung:** Eigenschaften (Attribute) müssen über Formulare editierbar sein.
  - **F4 Round-Trip:** Änderungen im Designer müssen im XML landen und umgekehrt (Synchronisation).
- **Nicht-funktionale Anforderungen (Wie gut muss es sein?):**
  - **NFA1 Effizienz:** Aufgaben müssen schneller erledigt sein als im Text-Editor.
  - **NFA2 Erlernbarkeit:** Neueinsteiger müssen die Struktur schneller verstehen.
  - **NFA3 Erweiterbarkeit:** Neue Komponenten müssen leicht integrierbar sein (MDSE-Vorteil!).

**📚 Literatur & Quellen:**

- **Robertson, S., & Robertson, J. (2012).** _Mastering the Requirements Process: Getting Requirements Right_. Addison-Wesley.
  - _Standardwerk für Requirements Engineering. Nutze es für die Strukturierung der Anforderungen (Volere-Template oder ähnlich)._
- **Norman, D. A. (2013).** _The Design of Everyday Things_. Basic Books.
  - _Hieraus nimmst du die Begriffe "Gulf of Execution" und "Gulf of Evaluation", um das Problem des Text-Editors zu beschreiben._

---

## Phase 5: Konzept & Design (Kapitel 4)

Hier beschreibst du die Lösung, _bevor_ du sie programmierst. Das ist der "Bauplan".

### 4.1 Architektur-Konzept

**Ziel des Kapitels:** Zeigen, dass die Lösung technisch fundiert ist und in die bestehende Landschaft passt.

- **Komponenten-Architektur:**
  - Zerlegung in Module: `TreeEditor`, `PropertyInspector`, `Toolbox`.
  - Datenfluss: Unidirektionaler Datenfluss (State Management). XML -> Parser -> State -> UI -> User Action -> State Update -> Serializer -> XML.
- **Herausforderung Round-Trip:**
  - Wie verhindern wir, dass beim Speichern Kommentare im XML verloren gehen?
  - _Lösungsansatz:_ Nutzung eines speziellen Parsers oder "Non-Destructive Editing".

### 4.2 UI/UX-Design

**Ziel des Kapitels:** Begründung der Design-Entscheidungen anhand von Usability-Prinzipien.

- **Layout-Entscheidung:**
  - Klassisches "IDE-Layout" (Links: Palette, Mitte: Canvas/Baum, Rechts: Eigenschaften).
  - _Begründung:_ Konsistenz mit bekannten Tools (VS Code, Eclipse) -> Nutzt das Vorwissen der Entwickler (Jakob Nielsen: "Match between system and real world").
- **Interaktions-Konzept:**
  - Drag & Drop für Strukturänderungen (intuitiv, aber komplex zu implementieren).
  - Formulare für Attribute (verhindert Syntaxfehler, da Dropdowns statt Freitext).

**📚 Literatur & Quellen:**

- **Tidwell, J. (2010).** _Designing Interfaces: Patterns for Effective Interaction Design_. O'Reilly.
  - _Quelle für UI-Patterns wie "Property Inspector" oder "Toolbox"._
- **Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994).** _Design Patterns: Elements of Reusable Object-Oriented Software_. Addison-Wesley.
  - _Wenn du im Code das "Composite Pattern" für die Baumstruktur oder "Observer" für Events nutzt, zitiere das hier._

---

## Phase 6: Implementierung (Kapitel 5)

Hier zeigst du, dass du programmieren kannst. Aber: Kein Code-Dumping! Beschreibe Konzepte, zeige nur relevante Snippets.

### 5.1 Technische Umsetzung

**Ziel des Kapitels:** Die Brücke vom Konzept zum Code schlagen.

- **Der Tech-Stack:**
  - Angular (Frontend-Framework).
  - TypeScript (Typsicherheit ist wichtig für das Datenmodell).
  - _Begründung:_ Passt in die bestehende Systemlandschaft des Unternehmens.
- **Kern-Algorithmen:**
  - **Rekursives Rendering:** Wie wird der XML-Baum in Angular-Komponenten übersetzt? (Erklärung der `ng-template` Rekursion).
  - **Metadaten-Mapping:** Wie weiß der Property-Editor, welche Felder er anzeigen muss? (Erklärung, wie die XSD/Metadaten genutzt werden).

### 5.2 Herausforderungen

**Ziel des Kapitels:** Zeigen, dass es nicht trivial war.

- **Beispiel:** Performance bei großen XML-Dateien.
- **Beispiel:** Handling von "Mixed Content" im XML (Text und Tags gemischt).
- **Lösung:** Virtual Scrolling oder Optimierung der Change Detection (`OnPush`).

**📚 Literatur & Quellen:**

- **Martin, R. C. (2008).** _Clean Code: A Handbook of Agile Software Craftsmanship_. Prentice Hall.
  - _Zitiere das, wenn du über deine Code-Struktur, Benennung oder Modularisierung sprichst._
- **Offizielle Dokumentationen (Angular, TypeScript).**
  - _Hier sind Web-Quellen erlaubt und notwendig._

---

## Phase 7: Evaluation & Fazit (Kapitel 6 & 7)

Der Abschluss. Hier schließt sich der Kreis zur Einleitung.

### 6.1 Evaluation

**Ziel des Kapitels:** Beweisen, dass deine Lösung funktioniert (oder ehrlich sagen, wo nicht).

- **Methodik:**
  - Qualitative Evaluation: "Cognitive Walkthrough" mit einem Experten oder "Thinking Aloud" Test mit einem Kollegen.
  - _Szenario:_ "Erstelle eine View mit 2 Buttons und einem Textfeld." -> Zeit messen, Fehler zählen.
- **Ergebnis-Diskussion:**
  - Vergleich Ist-Zustand (Text-Editor) vs. Soll-Zustand (Dein Designer).
  - Abgleich mit den Anforderungen aus Phase 4 (F1-F4, NFA1-NFA3).
  - _Wichtig:_ Sei ehrlich! Wenn Drag & Drop hakelig ist, schreib das. Wissenschaft lebt von Ehrlichkeit, nicht von Marketing.

### 7.1 Fazit & Ausblick

**Ziel des Kapitels:** Die "Take Home Message".

- **Zusammenfassung:**
  - Kurzer Recap: Problem -> MDSE-Ansatz -> HCD-Prozess -> Low-Code-Lösung.
- **Fazit:**
  - Der Designer senkt die Einstiegshürde (Citizen Developer) und reduziert Syntaxfehler (Effektivität).
- **Ausblick:**
  - Was fehlt noch? (z.B. Undo/Redo, Copy/Paste).
  - Zukunftsvision: KI-Integration ("Erstelle mir ein Formular für Kunden").

**📚 Literatur & Quellen:**

- **Krug, S. (2014).** _Don't Make Me Think, Revisited: A Common Sense Approach to Web Usability_. New Riders.
  - _Gut für die Diskussion von Usability-Problemen, die bei der Evaluation aufgetreten sind._
- **Sauro, J., & Lewis, J. R. (2016).** _Quantifying the User Experience: Practical Statistics for User Research_. Morgan Kaufmann.
  - _Falls du Zahlen/Metriken in der Evaluation hast._
