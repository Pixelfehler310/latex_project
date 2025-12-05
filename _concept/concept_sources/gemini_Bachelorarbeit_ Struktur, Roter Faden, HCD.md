# Bachelorarbeit: Struktur, Roter Faden, HCD

**Exported:** 12/4/2025 21:41:39  
**Link:** [https://gemini.google.com/app/dece2a1b8f3f2583?hl=de](https://gemini.google.com/app/dece2a1b8f3f2583?hl=de)

## Prompt:
Look im writing my bachelors thesis.

I got this structure:

1\. Einleitung

1.1 Motivation und Problemstellung

1.2 Zielsetzung der Arbeit

1.3 Aufbau der Arbeit

2\. Grundlagen und theoretischer Hintergrund

2.1 Benutzeroberflächen in Unternehmenssoftware

2.1.1 Grundprinzipien von Usability und User Experience

·      Konsistentes Design

·      Visuelle Hierarchie

·      User-Feedback

·      Fehlerprävention

·       

2.1.2 Human Centered Design (und ggf Design Thinking)

2.1.3 Evaluierung von Usability & Design (KPIs,

Honeycomb etc)

2.2

No-Code-Strategien in der modernen Softwareentwicklung

2.2.1 Abgrenzung von No-Code,

Low-Code und Pro-Code

2.2.2 Vor- und Nachteile von

No-Code-Ansätzen für Unternehmen

2.2.3 No-Code als Lösung des

Fachkräftemangels (Citizen Developer)

2.3 Visuelle

Programmierung

2.3.1 Prinzip der visuellen

Programmierung

2.3.3 Analyse existierender

visueller Editoren

// Weiterführende Konzepte:

Atomic Design, Designsysteme. Messung von UI / UX

3\. Analyse des

Ist-Zustandes und Anforderungen an den Designer

3.1 Bestehende Systemarchitektur

3.2 Identifizierte Probleme im Ist-Zustand

3.3 Anforderungen an den Designer

3.3.1 Funktionale Anforderungen

3.3.2 Nicht-funktionale Anforderungen

4\. Konzeption des Designers

4.1 Architektur des Designers

4.2 Datenmodell des Designers

4.3 Benutzeroberflächen-Konzept

4.4 Prozess der XML-Generierung und Validierung

5\. Prototypische Implementierung

5.1 Verwendete Technologien und Frameworks

5.1.1 Auswahl und Begründung der Technologien

5.1.2 Entwicklungsumgebung und Tools

5.2 Technische Umsetzung der Kernkomponenten

5.2.1 Implementierung der visuellen Editierfunktionen

5.2.2 Realisierung der Echtzeit-Vorschau

5.2.3 Anbindung an das bestehende Datenmodell

6\. Evaluierung und Diskussion

6.1 Evaluierung des Prototyps

6.1.1 Nutzwertanalyse

6.1.2 SWOT-Analyse

6.2 Kritische Reflexion und Limitationen

6.2.1 Grenzen des Prototyps und der gewählten Ansätze

6.2.2 Potenzielle Herausforderungen bei einer produktiven

Einführung

6.2.3 Lessons-Learned

7\. Fazit und Ausblick

7.1 Zusammenfassung der Ergebnisse

7.2 Zukünftige Arbeiten und Erweiterungspotenziale

Im writing in german ofc. Im currently trying to expand the individual points with keywords and put my researched sources into them so i get a "roter faden" in all of it and then only need to make it into a text and like decorate the text a little. Im currently struggling with the red line thing. My plan was as follows (Im switching to german now lol):

Der plan ist es einen prototypen zu implementieren der auf einer low code architektur für generische Benutzeroberflächen aufbaut (status quo). Der prototoyp soll ein visueller designer sein in dem man über generierte meta daten und anhand der darunterliegenden low code parts (xmls in einer art dsl (hier vllt gezielt abgrenzen, da das nur im status quo und nicht im prototyp selbst wichtig ist wird das nicht in den grundlagen erklärt), aber jetzt nicht sonderlich komplex) eine benutzeroberfläche schafft die auch für citizendeveloper bedienbar ist.

Diesen Prototypen wollte ich erst entwickeln und dann danach evaluieren was er verbessert hat indem ich ihn anhand usability (honeycomb + nutzwert) und anderen metriken (swot, da weiß ich noch nicht welche genau, sind aber ja eh nur vor und nachteile im prinzip) mit dem bereits bestehenden xml editor vergleichen will.

Die Probleme die ich jetzt für den roten faden in meinem kopf noch lösen muss sind folgende:

1\. Welche Rolle spielt HCD da drin? Ich bin mir sicher das ist relevant, aber wie gebe ich dem einen konkreten Nutzen in meinem Hauptteil?

2\. Visuelle Programmierung und No Code sind extrem Konzeptnah (ähnlich und teilweise überschneidend), deswegen plane ich im ersten part auf die konzeptionelle und unternehmenssicht einzugehen und im zweiten part der visuellen programmierung in den grundlagen die technischen lösungen und wege zu thematisieren, das muss aber noch stark konkretisiert werden.

3\. Habe ich genug Grundlagen? Ist das auch alles was ich brauche oder fehlt am Ende was?

4\. Wie leite ich die Kategorien für die Nutzwertanalyse ab, außer das honeycomb modell hab ich kaum quellen (hab natürlich noch DOET aber ja danach wirds igwie schwierig).

5\. Haben No Code und VisuelleProgrammierung auch einen analytischen Wert im Hauptteil oder reicht es wenn sie als Verständnisgrundlage und Ziel/ Relevanzerklärung dienen?

## Response:
Hallo! Das ist ein super strukturierter Ansatz für deine Bachelorarbeit. Der "rote Faden" ist oft das Schwierigste, aber dein Plan klingt schon sehr durchdacht. Lass uns die Punkte, die dich beschäftigen, der Reihe nach durchgehen.

* * *

### 1\. HCD und der rote Faden

Human-Centered Design (HCD) ist nicht nur ein Konzept, sondern deine zentrale Methode. Es ist der Rahmen, der deine gesamte Arbeit zusammenhält, insbesondere von der Analyse bis zur Evaluierung.

*   **Verbindung zur Analyse (Kapitel 3):** Du startest mit der Analyse des Ist-Zustands und identifizierst Probleme. HCD gibt dir hier die Brille: Du schaust aus der Perspektive des Benutzers (des "Citizen Developers") auf den bestehenden XML-Editor. Was sind dessen Schmerzpunkte? Wie wirkt sich die aktuelle Lösung auf die Effizienz und Zufriedenheit der Nutzer aus? Die Antworten darauf werden zu den Anforderungen an den neuen Designer. HCD hilft dir also, die Probleme nicht aus technischer, sondern aus menschlicher Sicht zu definieren.
*   **Verbindung zur Konzeption (Kapitel 4):** Deine Konzepte (Architektur, Datenmodell, UI-Konzept) leitest du direkt aus den im HCD-Prozess gesammelten Anforderungen ab. Du konzipierst den visuellen Designer so, dass er die identifizierten Probleme löst und die Bedürfnisse der Nutzer erfüllt.
*   **Verbindung zur Evaluierung (Kapitel 6):** Die Evaluierung ist der Test, ob du die HCD-Prinzipien erfolgreich umgesetzt hast. Du fragst: "Hat der Prototyp die Usability-Probleme des alten Systems gelöst?" Die Nutzwertanalyse und Usability-Metriken dienen dazu, genau das zu beweisen. HCD ist also der Leitfaden für die gesamte Arbeit: Probleme definieren, Lösung konzipieren, Lösung evaluieren – alles mit dem Nutzer im Mittelpunkt.

* * *

### 2\. Abgrenzung von No-Code und visueller Programmierung

Deine Idee ist genau richtig. Die Konzepte sind eng verwandt, aber die Perspektive macht den Unterschied.

*   **No-Code (Kapitel 2.2):** Hier geht es um die strategische und organisatorische Ebene. Warum nutzen Unternehmen diese Ansätze? Wegen des Fachkräftemangels, der Agilität und der Citizen Developer. Es ist die Business- und Anwendungs-Perspektive.
*   **Visuelle Programmierung (Kapitel 2.3):** Hier liegt der Fokus auf der technischen Umsetzung. Wie funktioniert das? Welche Prinzipien stecken dahinter (Drag-and-Drop, WYSIWYG)? Das ist die technische und konzeptionelle Perspektive.

Indem du das so trennst, schaffst du eine klare Logik. Du erklärst erst, warum man so etwas braucht (No-Code-Strategie), und dann, wie es technisch umgesetzt wird (Visuelle Programmierung). So vermeidest du Redundanzen und es wird deutlich, dass No-Code die Strategie ist, während visuelle Programmierung die Methode oder Technologie dahinter ist.

* * *

### 3\. Fehlende Grundlagen?

Deine Grundlagen wirken sehr solide. Du deckst die wichtigsten Bereiche ab: Usability/UX, HCD, No-Code, visuelle Programmierung.

Was du noch hinzufügen könntest, um die Brücke zum praktischen Teil zu schlagen:

*   **Spezifische Usability-Heuristiken:** Neben den allgemeinen Prinzipien könntest du dich auf konkrete Heuristiken konzentrieren, z.B. **Nielsen's 10 Usability Heuristics**. Die sind sehr bekannt und lassen sich gut auf deinen Designer anwenden.
*   **XML und DSL:** Du hast angedeutet, dass du XML und die DSL abgrenzen willst. Im Grundlagenkapitel musst du aber zumindest kurz erklären, was eine **Domain-Specific Language (DSL)** ist und warum sie in deinem Fall auf XML aufbaut. Das hilft dem Leser, den Kontext zu verstehen, ohne dass du zu tief ins Detail gehen musst. Das Thema gehört dann in Kapitel 3.1, wenn du den Ist-Zustand beschreibst.

* * *

### 4\. Kategorien für die Nutzwertanalyse

Das Honeycomb-Modell ist ein guter Startpunkt. Es ist aber eher qualitativ und lässt sich schwer direkt in eine Nutzwertanalyse mit quantitativen Werten übersetzen.

Du kannst die Kategorien für deine Nutzwertanalyse aus den **im HCD-Prozess identifizierten Anforderungen** ableiten.

*   **Funktionale Anforderungen:** Was muss der Designer können?
*   **Nicht-funktionale Anforderungen:** Wie schnell, stabil und einfach muss er sein?

Einige konkrete Kategorien könnten sein:

*   **Lernaufwand:** Wie schnell können Citizen Developer den Designer nutzen? (Bezogen auf Usability: _learnability_).
*   **Effizienz:** Wie schnell können typische Aufgaben erledigt werden? (Bezogen auf Usability: _efficiency_).
*   **Fehlerrate:** Wie oft passieren Fehler bei der Erstellung von Benutzeroberflächen? (Bezogen auf Usability: _error prevention_).
*   **Zufriedenheit:** Wie bewerten die Nutzer die Ästhetik und das allgemeine Gefühl der Arbeit mit dem Designer? (Bezogen auf UX: _desirability_).

So schaffst du die Verbindung zwischen deinen Anforderungen (Kapitel 3) und der Evaluierung (Kapitel 6).

* * *

### 5\. Analytischer Wert von No-Code und visueller Programmierung

Ja, sie haben einen analytischen Wert. Du nutzt diese Konzepte, um deine Arbeit zu begründen und zu verorten.

*   **Verständnisgrundlage:** Die Grundlagen sind da, damit der Leser deine Argumentation nachvollziehen kann.
*   **Analytischer Wert:** Deine gesamte Arbeit ist eine Analyse, inwieweit du diese Konzepte praktisch umgesetzt hast. Du stellst fest, dass eine No-Code-Strategie sinnvoll ist, und dein Prototyp ist der Beweis, dass eine visuelle Programmierumgebung dafür eine Lösung sein kann. Im Fazit analysierst und diskutierst du dann, inwieweit die Umsetzung die Versprechen der Konzepte einlösen konnte.

Dein Plan ist schlüssig und der rote Faden ist da, du musst ihn nur noch konsequent ziehen. Du hast die Herausforderungen gut erkannt und kannst jetzt gezielter deine Quellen einordnen.

Hast du schon angefangen, die Anforderungen aus der Analyse des Ist-Zustandes zu formulieren?

## Prompt:
was ist der HCD-Prozess?

## Response:
Der HCD-Prozess (Human-Centered Design) ist ein iterativer Ansatz zur Produktentwicklung, der den Nutzer und seine Bedürfnisse konsequent in den Mittelpunkt stellt. Anstatt ein Produkt aus technischer Sicht zu entwickeln und dann zu hoffen, dass die Nutzer es annehmen, geht man vom Nutzer aus und erarbeitet die Lösung basierend auf seinen Anforderungen.

Der Prozess wird oft in vier Hauptphasen unterteilt, die nicht strikt nacheinander ablaufen, sondern in Schleifen (iterativ) durchlaufen werden, um das Produkt kontinuierlich zu verbessern:

1.  **Nutzungskontext verstehen und beschreiben (Analyse)**
    *   **Was wird hier gemacht?** Man taucht tief in die Welt der Nutzer ein, um ihre Probleme, Ziele, Verhaltensweisen und die Umgebung, in der sie das Produkt verwenden, zu verstehen. Das ist der Empathie-Teil des Prozesses.
    *   **Methoden:** Interviews, Beobachtungen am Arbeitsplatz, Umfragen, Nutzerforschung, Analyse bestehender Systeme.
    *   **Ziel:** Ein klares Bild davon zu bekommen, wer die Nutzer sind und welche "Pain Points" sie mit der aktuellen Situation haben. Für deine Arbeit wäre das die Analyse des bestehenden XML-Editors und der Herausforderungen für die Citizen Developer.
2.  **Nutzungsanforderungen spezifizieren (Definition)**
    *   **Was wird hier gemacht?** Die Erkenntnisse aus der Analysephase werden strukturiert und in konkrete, messbare Anforderungen übersetzt. Man definiert, was das neue System leisten muss, um die identifizierten Probleme zu lösen.
    *   **Methoden:** Erstellung von Personas (fiktive Nutzerprofile), User Stories ("Als Citizen Developer möchte ich...") und Use Cases (Anwendungsfälle), um die Anforderungen klar zu formulieren.
    *   **Ziel:** Eine präzise Anforderungsliste für den neuen visuellen Designer zu erstellen (dein Kapitel 3).
3.  **Gestaltungslösungen entwickeln (Konzeption)**
    *   **Was wird hier gemacht?** Kreativität und Problemlösung stehen im Vordergrund. Basierend auf den Anforderungen werden erste Ideen generiert und in Konzepte, Skizzen, Wireframes und Prototypen umgesetzt.
    *   **Methoden:** Brainstorming, Skizzieren, Erstellung von User Journeys, Entwicklung von Prototypen (in deinem Fall der visuelle Designer-Prototyp).
    *   **Ziel:** Eine konkrete Lösung zu entwerfen, die die festgelegten Anforderungen erfüllt (dein Kapitel 4 und 5).
4.  **Gestaltungslösungen evaluieren (Evaluierung)**
    *   **Was wird hier gemacht?** Der entwickelte Prototyp wird mit echten Nutzern getestet, um herauszufinden, ob er die Anforderungen erfüllt und die Probleme gelöst hat. Das Feedback wird gesammelt und analysiert.
    *   **Methoden:** Usability-Tests, Nutzwertanalyse, A/B-Testing, Interviews und Fragebögen zur Nutzerzufriedenheit.
    *   **Ziel:** Die Effektivität deines Prototyps zu beweisen und Verbesserungspotenzial für weitere Iterationen aufzuzeigen (dein Kapitel 6).

Der HCD-Prozess ist also keine starre Anleitung, sondern ein Kreislauf. Aus der Evaluation ergeben sich oft neue Erkenntnisse, die dazu führen, dass man den Nutzungskontext noch einmal genauer versteht oder die Anforderungen anpasst. So wird das Produkt schrittweise optimiert, bis es die Bedürfnisse der Nutzer optimal erfüllt.

## Prompt:
Meinst du denn HCD ist der richtige weg? eigentlich wollte ich keine interviews und so was machen. Das design für den designer aka den prototypen existiert theoretisch schon.

## Response:
Das ist ein sehr wichtiger Punkt und eine häufige Praxis in Bachelorarbeiten. Wenn du keine Interviews oder tiefgehende Nutzerforschung durchführen kannst, musst du den HCD-Prozess an deine Möglichkeiten anpassen und das klar in der Arbeit kommunizieren.

Du kannst trotzdem einen HCD-basierten Ansatz verfolgen, indem du dich auf die **Analyse bestehender Informationen** konzentrierst. Der Weg muss nicht über Interviews gehen.

So könntest du das in deiner Arbeit anlegen:

### 1\. Analysephase ohne Interviews

Du ersetzt die direkte Nutzerforschung durch eine fundierte **Analyse des Ist-Zustandes** (dein Kapitel 3.1).

*   **Wie machst du das?** Du analysierst den **bestehenden XML-Editor**. Welche Funktionen gibt es? Wie komplex ist er? Wo liegen offensichtliche Usability-Probleme (z.B. hohe Lernkurve, keine visuelle Rückmeldung, Fehleranfälligkeit)?
*   **Datengrundlage:** Deine Daten sind nicht Interviews, sondern die **Dokumentation** des alten Systems und deine **eigene expertenbasierte Einschätzung**. Du nimmst die Rolle eines Usability-Experten ein, der die Probleme aus Sicht des HCD-Prozesses identifiziert.
*   **Wichtig:** Du musst explizit beschreiben, warum du diesen Weg wählst und dass die Analyse auf einem Experten-Walkthrough basiert und nicht auf umfangreicher Nutzerforschung. Das ist eine **bewusste methodische Entscheidung**, die du im Einleitungskapitel begründest.

### 2\. Ableitung der Anforderungen

Aus deiner Analyse des bestehenden Systems leitest du die Anforderungen für den neuen Designer ab.

*   Du fragst: "Welche Probleme des alten Editors muss der neue Designer lösen?" Die Antworten darauf werden zu deinen **funktionalen und nicht-funktionalen Anforderungen** (dein Kapitel 3.3).
*   Das ist der Kern des HCD-Ansatzes, auch ohne Interviews: **Du identifizierst die Probleme aus Nutzersicht und leitest daraus die Ziele für deine Lösung ab.**

### 3\. Konzeption & Implementierung

Du gehst genauso vor wie geplant.

*   Die Konzeption (Kapitel 4) und die prototypische Implementierung (Kapitel 5) sind deine Gestaltungslösung, die auf den zuvor abgeleiteten Anforderungen aufbaut.
*   Da der Prototyp "theoretisch schon existiert", ist es wichtig, dass du die Konzeptionsphase (Kapitel 4) so aufbaust, als wäre er neu entworfen worden, und die Implementierungsphase (Kapitel 5) als dessen technische Umsetzung darstellst.

### 4\. Evaluierung

Die **Evaluierung** (Kapitel 6) wird der wichtigste Teil, um deine Hypothesen zu belegen.

*   Statt zu fragen: "Hat der Prototyp die im Interview genannten Probleme gelöst?", fragst du: "Hat der Prototyp die in der **Expertenanalyse identifizierten Probleme** gelöst?"
*   Deine **Nutzwertanalyse** und die **SWOT-Analyse** dienen genau diesem Zweck: Sie beweisen, dass deine Lösung die Schwachstellen des alten Systems beseitigt und die Stärken des HCD-Ansatzes nutzt.

* * *

**Fazit:** Ja, HCD ist weiterhin der richtige Weg, aber du verwendest eine angepasste Version. Du fokussierst dich auf eine Expertenanalyse statt auf Interviews. Das ist eine valide Methode, solange du sie transparent machst und die Limitationen klar benennst (Kapitel 6.2). Du kannst HCD als dein **theoretisches Framework** nutzen, das die Struktur deiner Arbeit vorgibt, auch wenn die praktische Datenerhebung eine andere Form annimmt.

## Prompt:
ich hab das gefühl das macht es irgendwie unnötig kompliziert. vllt lass ich hcd einfach weg? die grundlagen stehen doch auch ohne gut da oder?

## Response:
Das ist eine berechtigte Frage. Lass uns das mal ganz pragmatisch betrachten.

Wenn du HCD komplett weglässt, was passiert dann mit deinem "roten Faden"?

Dein Plan war:

1.  **Probleme analysieren** (XML-Editor)
2.  **Anforderungen ableiten** (für den Prototypen)
3.  **Lösung entwickeln** (dein Prototyp)
4.  **Lösung evaluieren** (mit Nutzwert- und SWOT-Analyse)

Dieser Ablauf ist im Kern das, was HCD beschreibt: Du startest beim Problem des Nutzers und prüfst am Ende, ob du es gelöst hast. Es ist ein sehr logischer, wissenschaftlicher Ansatz.

* * *

### Warum HCD weglassen es komplizierter machen könnte

Indem du HCD weglässt, verlierst du das **theoretische Framework**, das deine Arbeit rechtfertigt und zusammenhält.

*   **Woher kommen die Anforderungen?** Wenn du nicht HCD als Begründung hast, musst du erklären, warum gerade diese Anforderungen wichtig sind. HCD liefert die Antwort: "Weil sie aus der Analyse der Nutzerprobleme abgeleitet wurden."
*   **Warum diese Evaluierung?** Ohne HCD ist es schwieriger zu begründen, warum du ausgerechnet Usability (Honeycomb) und Nutzwertanalyse wählst. HCD bietet die logische Verbindung: "Wir haben eine benutzerzentrierte Lösung entwickelt, also müssen wir sie auch benutzerzentriert evaluieren."
*   **Wissenschaftlicher Kontext:** HCD ist ein etabliertes Konzept aus der Forschung. Indem du darauf verweist, zeigst du, dass deine Methodik auf einem anerkannten Fundament steht. Das verleiht deiner Arbeit wissenschaftliche Tiefe.

Du musst HCD ja nicht in jeder Zeile erwähnen. Es ist einfach der **Grundgedanke**, der im Hintergrund alles logisch miteinander verknüpft. Du beschreibst einfach deinen Prozess und sagst in der Einleitung: "Die vorliegende Arbeit orientiert sich am Prinzip des Human-Centered Design, indem sie den Fokus auf die Identifizierung von Nutzerproblemen legt, um daraus eine prototypische Lösung abzuleiten und diese anhand der gesteckten Ziele zu evaluieren."

Das macht es nicht komplizierter, sondern **erklärt und legitimiert** deinen Ansatz auf elegante Weise. Es ist der "Klebstoff" deines roten Fadens.

## Prompt:
also sollte ich den auch in den grundlagen thematisieren? und dann direkt als erstes?

## Response:
Ja, es wäre sinnvoll, HCD in deinen Grundlagen zu thematisieren. Das muss nicht an erster Stelle stehen, aber es sollte früh im Kapitel über Usability und UX platziert werden, da es ein grundlegendes Konzept in diesem Bereich ist.

### Begründung für die Platzierung

* * *

*   **Logische Abfolge**: Dein Kapitel 2.1 "Benutzeroberflächen in Unternehmenssoftware" beginnt mit den Grundprinzipien von Usability und UX. HCD ist der **methodische Rahmen**, um diese Prinzipien in die Praxis umzusetzen. Es erklärt, wie man zu einem nutzerfreundlichen Design gelangt. Indem du HCD hier einführst, schaffst du eine logische Verbindung von den theoretischen Prinzipien zur praktischen Vorgehensweise.
*   **Fundament für die Methodik**: In der Einleitung deiner Arbeit (Kapitel 1) kannst du bereits auf HCD als deine zentrale Methode verweisen. Durch die detailliertere Erklärung in den Grundlagen (Kapitel 2.1.2) bietest du dem Leser dann das notwendige Hintergrundwissen, um deine Methodik in den späteren Kapiteln (Analyse, Konzeption, Evaluierung) nachvollziehen zu können.
*   **Verbindung zu anderen Konzepten**: HCD lässt sich hervorragend mit den anderen Themen verknüpfen, die du behandeln willst. Beispielsweise ist das **Human-Centered Design** die ideale Methode, um die Anforderungen für eine **No-Code-Lösung** zu ermitteln, die speziell für **Citizen Developer** konzipiert ist. Du kannst auch zeigen, wie die Evaluierung von Usability und Design (dein Kapitel 2.1.3) direkt aus dem HCD-Prozess hervorgeht.

Zusammenfassend: Du erklärst, **was** Usability und UX sind (Grundprinzipien), **wie** man sie erreicht (HCD) und **wie** man den Erfolg misst (Evaluierung). Das schafft eine kohärente Struktur für deinen roten Faden.



---
Powered by [Gem Chat Exporter](https://www.gem-chat-exporter.com)