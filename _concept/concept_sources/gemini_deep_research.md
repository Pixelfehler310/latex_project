Theoretische Fundierung des Low-Code UI-Designers: Human-Centered Design, Usability und Kognitive Effizienz (Kapitel 2.3)
I. Einführung und Verortung des Designparadigmas
1.1 Die Herausforderung traditioneller UI-Erstellung und das Defizit textbasierter Konfiguration
Der traditionelle Prozess der Erstellung und Anpassung von Benutzeroberflächen (User Interfaces, UIs), insbesondere jener, die auf komplexen, rein technischen Konfigurationsdateien wie XML basieren, ist mit inhärenter Ineffizienz und einer erhöhten Fehleranfälligkeit verbunden. Dieses Problem zu adressieren, ist das primäre Ziel des vorliegenden Prototyps.
Die Kritik an textbasierten Darstellungen wie XML in der UI-Gestaltung ist fundiert. Solche Repräsentationen werden als langwierig beschrieben und führen zu Problemen in der Verarbeitung durch automatisierte Systeme.[1, 2] Entscheidend für die Usability ist jedoch, dass die textuelle Syntax das visuelle Verständnis der Benutzeroberfläche stark beeinträchtigt.[1] Der Nutzer ist gezwungen, das räumliche und interaktive Ergebnis mental aus der abstrakten Code-Struktur zu synthetisieren. Beim Lesen von Code muss das Arbeitsgedächtnis die Werte von Variablen, die Steuerungslogik und die Aufrufsequenzen zwischenspeichern.[3] Da das menschliche Arbeitsgedächtnis extrem begrenzt ist und nur etwa vier Informationseinheiten ("Chunks") speichern kann, überschreiten komplexe XML-Strukturen diesen Schwellenwert schnell.[3, 4] Die Folge ist eine erhöhte Verwirrung und eine Beeinträchtigung der Aufgabenerfüllung.[3, 4]
Diese kognitive Bürde wird in der Cognitive Load Theory (CLT) als extrinsische kognitive Belastung (Extraneous Cognitive Load) klassifiziert.[5, 6] Die extrinsische Last ist der unnötige Aufwand, der durch schlechtes Design oder die Art der Informationspräsentation verursacht wird.[6] Im Falle der XML-basierten UI-Erstellung wird die extrinsische Last dadurch generiert, dass das Gehirn sich jeden Arbeitsschritt vorstellen muss.[5] Philosophen wie Leibniz erkannten bereits die Notwendigkeit, die Form eines Symbols so zu gestalten, dass es die exakte Natur des Dings abbildet und dadurch die Denkarbeit wunderbar verringert.[7] Die abstrakte, technische XML-Syntax erfüllt diese Anforderung nicht, was direkt zu der unnötigen kognitiven Belastung führt, die minimiert werden soll.[5]
Die Ablösung dieses Prozesses ist auch ökonomisch notwendig. Organisationen sind zunehmend gefordert, Modifikationen an ihren IT-Systemen intern vorzunehmen, da ausgelagerte Projekte unverhältnismäßig höhere Kosten und längere Zeitspannen in Anspruch nehmen.[8] Angesichts der Intensivierung der digitalen Transformation und des Bedarfs an schneller Marktadaption [9, 10] führt der traditionelle Ansatz aufgrund begrenzter IT-Ressourcen und langer Entwicklungszyklen zu Engpässen.[10]
1.2 Der Low-Code/WYSIWYG-Designer als nutzerzentrierte Abstraktion
Als Antwort auf diese technischen und kognitiven Defizite wird ein visueller Low-Code-Designer (WYSIWYG) zur Direkten Manipulation der Benutzeroberfläche zur Laufzeit entwickelt. Low-Code Development Platforms (LCDPs) stellen einen Paradigmenwechsel dar, da sie die Erstellung von Software durch grafische Benutzeroberflächen und Konfiguration statt traditioneller Programmierung ermöglichen.[11, 12]
Der Erfolg von Low-Code und WYSIWYG basiert auf dem Konzept der Abstraktion.[11] Abstraktion blendet unnötige Details aus, wodurch die Nutzer sich auf die Teile konzentrieren können, die relevant sind, um ihre Ziele zu erreichen.[11] Low-Code ist die logische Weiterentwicklung dieser Idee, indem es Entwicklern und Nicht-Programmierern gleichermaßen zugänglich gemacht wird.[11]
Das Prinzip des WYSIWYG ("What You See Is What You Get") ist fundamental für diesen Ansatz. Es stellt sicher, dass der Inhalt in einer Form bearbeitet wird, die seinem fertigen Erscheinungsbild entspricht.[11] WYSIWYG-Editoren sind ein primäres Beispiel für das Direct Manipulation User Interface, da sie Entwicklern ermöglichen, UI-Elemente visuell zu manipulieren und sofortiges, visuelles Feedback zu sehen.[13]
Die technische Realisierung der Laufzeitbearbeitung (Runtime Adaptation, RTA) [14, 15] im Kontext des Low-Code-Designers ist die praktische Implementierung des iterativen Prinzips des Human-Centered Design (HCD). HCD ist ein strukturierter, iterativer Prozess, der kontinuierlich durch Feedback und Verfeinerung vorangetrieben wird.[16, 17, 18] Die Fähigkeit zur schnellen, kontinuierlichen Änderung der Benutzeroberfläche zur Laufzeit [19] durch den Fachexperten ermöglicht es der Organisation, agil auf sich ändernde Anforderungen zu reagieren. Dies beschleunigt die Bereitstellung von UI-Anpassungen erheblich und steigert somit direkt die Time-to-Market.[12, 19]
II. Das Fundament: Human-Centered Design (HCD)
2.1 Normative Definition und Zielsetzung nach ISO 9241-210
Das Human-Centered Design (HCD) liefert das theoretische und normative Fundament für die Konzeption des visuellen UI-Designers. Nach der internationalen Norm ISO 9241-210:2010(E) ist HCD ein Ansatz für interaktive Systeme, dessen Ziel es ist, Systeme nutzbar und nützlich zu machen, indem er sich auf die Nutzer, ihre Bedürfnisse und Anforderungen sowie die Anwendung von Human Factors/Ergonomie und Usability-Kenntnissen konzentriert.[16, 20]
Die Anwendung des HCD-Ansatzes resultiert in spezifischen, messbaren Verbesserungen.[16] Er ist darauf ausgerichtet, die Effektivität und Effizienz zu steigern. Darüber hinaus verbessert HCD das menschliche Wohlbefinden, die Nutzerzufriedenheit, die Barrierefreiheit und die Nachhaltigkeit und wirkt möglichen negativen Auswirkungen der Nutzung auf Gesundheit, Sicherheit und Leistung entgegen.[16]
Der geplante Low-Code-Designer wird durch diese ISO-Norm explizit validiert, da die im Projekt angestrebten Erfolgskriterien – Usability, Citizen Development und Effizienz – die expliziten Resultate sind, die HCD laut Standard erzielen soll. HCD ist somit nicht bloß eine Design-Philosophie, sondern ein strukturierter und akademisch fundierter Ansatz [17, 18], der gezielt darauf ausgelegt ist, die im Projekt definierten Kennzahlen zu optimieren.[16]
2.2 Die Kernprinzipien des HCD-Prozesses (ISO 9241-110)
Der HCD-Prozess ist durch eine Reihe von Kernprinzipien definiert, die sicherstellen, dass die Entwicklung konsequent nutzerzentriert abläuft. Die Gestaltung muss auf einem expliziten Verständnis der Nutzer, ihrer Aufgaben und des Nutzungsumfeldes basieren.[16] Eine kontinuierliche Nutzerbeteiligung während des gesamten Design- und Entwicklungsprozesses ist erforderlich.[16]
Ein zentrales Merkmal des HCD ist seine Iterativität.[16, 17] Der Prozess ist zyklisch, wird durch nutzerzentrierte Evaluation verfeinert [16] und ermöglicht es, nach dem Testen eine Neudefinition des Problems vorzunehmen, falls erforderlich.[17] Diese Flexibilität und Anpassungsfähigkeit, oft beschrieben als „Fail early; fail fast; fail small“, betrachtet die Iteration als kontinuierliches Lernen.[21]
Für die Gestaltung der Benutzeroberfläche selbst legt die ISO 9241-110 folgende Designprinzipien fest, die berücksichtigt werden müssen [16]:
• Eignung für die Aufgabe (suitability for the task).
• Selbstbeschreibungsfähigkeit (self-descriptiveness).
• Konformität mit den Nutzererwartungen (conformity with user expectations).
• Eignung zum Lernen (suitability for learning).
• Kontrollierbarkeit (controllability).
• Fehlertoleranz (error tolerance).
• Eignung zur Individualisierung (suitability for individualization).
Historisch gesehen war die Entwicklung von Computersystemen oft technologiegetrieben, basierend auf der Annahme, dass "Nutzer sich anpassen können" an das, was Entwickler bauen.[22] HCD stellt diese Perspektive in Frage und argumentiert, dass ein vielversprechenderer Ansatz darin besteht, das natürliche Verhalten der Nutzer zu modellieren, um Schnittstellen zu entwerfen, die intuitiver, leichter erlernbar und fehlerfreier sind.[22] Der visuelle Low-Code-Designer ist eine direkte Umsetzung dieser Forderung, da er die textbasierte, abstrakte Anpassung (XML) durch eine Direkte Manipulation ersetzt, die physische Aktionen und Gesten imitiert.[23]
III. Usability als zentrales Erfolgsmaß (Projektwert 1)
3.1 Die triadische Definition der Usability und ihre Operationalisierung
Usability ist das zentrale messbare Erfolgskriterium des HCD-Prozesses und des prototypischen Designers. Nach ISO 9241-11:2018 wird Usability definiert als das Ausmaß, in dem ein Produkt von bestimmten Nutzern verwendet werden kann, um spezifizierte Ziele mit Effektivität, Effizienz und Zufriedenheit in einem spezifizierten Nutzungskontext zu erreichen.[24]
Diese Definition umfasst drei voneinander abhängige Dimensionen [25]:

1. Effektivität: Bezieht sich auf die Genauigkeit und Vollständigkeit, mit der spezifizierte Nutzer ihre spezifizierten Ziele erreichen.[25]
2. Effizienz: Bezieht sich auf die aufgewendeten Ressourcen (typischerweise Zeit oder kognitiver Aufwand) im Verhältnis zur Genauigkeit und Vollständigkeit der erreichten Ziele.[25]
3. Zufriedenheit: Bezieht sich auf den Komfort und die Akzeptanz des Arbeitssystems für seine Nutzer und andere betroffene Personen.[25]
   Im Rahmen dieses Projekts bildet die Dimension der Effizienz die theoretische Grundlage für die Messung des übergeordneten Projektzielwerts "Time-to-Market".[25] Eine Steigerung der Prozesseffizienz im UI-Anpassungsprozess – beispielsweise durch die Reduzierung des Zeitaufwands und des kognitiven Aufwands durch den WYSIWYG-Designer [13] – führt direkt zu einer Beschleunigung der Lieferkette. Eine schnelle Reaktion auf Marktanforderungen ist kritisch; so kann eine Verzögerung von nur einem Quartal bei der Markteinführung eines Produkts zum Verlust von 50% des erwarteten Produktgewinns führen.[26]
   3.2 Quantifizierung der Usability und ökonomische Rechtfertigung
   Die Wirksamkeit des HCD-Ansatzes, und damit des prototypischen Designers, kann quantitativ gemessen werden. Im Rahmen der Testphase des HCD-Prozesses [17, 27] ist es möglich, Key Performance Metrics (KPMs) wie die Zeit zur Erledigung der Aufgabe (Time on Task) und die Fehlerraten (Error Rates) zu erfassen.[27] Diese quantitativen Daten ermöglichen eine fundierte Anpassung und iterative Verbesserung des Prototyps.[27]
   Die ökonomische Rechtfertigung für die Implementierung eines HCD-orientierten Designers ist signifikant. Es besteht ein etabliertes Kosten-Nutzen-Verhältnis für Usability, das in vielen Organisationen bei 1 zu 10 bis 1 zu 100 liegt.[26] Die Integration von Usability von Beginn an kann Effizienzsteigerungen von über 700% ermöglichen.[26] Entscheidend ist die Kostenvermeidung: Die Korrektur eines Problems in einem System kostet nach dessen Freigabe 100-mal so viel, wie die Behebung desselben Problems in der Designphase.[26]
   Die Implementierung der Runtime Adaptation (RTA) in Verbindung mit dem Low-Code-Designer stellt sicher, dass der Prozess der UI-Korrektur und -Anpassung kontinuierlich in der kostengünstigsten Phase ("Designphase") verbleibt.[26] Da der Citizen Developer die Benutzeroberfläche zur Laufzeit anpassen kann [14], wird der Zyklus des Prototyping und Testens [27] kontinuierlich fortgeführt. Dies dient als strategischer Schutzmechanismus gegen die exponentiell steigenden Kosten der Fehlerbehebung, die typischerweise nach der Produktfreigabe anfallen.[26] Darüber hinaus haben Usability-Techniken nachweislich die Entwicklungszeit um 33-50% gesenkt und können die Zeit für mühsame Entwicklungsaufgaben um 40% reduzieren.[26]
   IV. Kognitive Ergonomie und Designprinzipien
   4.1 Die limitierte Natur des Arbeitsgedächtnisses und die Cognitive Load Theory (CLT)
   Die theoretische Grundlage für die Notwendigkeit des visuellen Designers liegt in der Cognitive Load Theory (CLT), entwickelt von John Sweller.[4] Die kognitive Last ist der Aufwand, der im Arbeitsgedächtnis verwendet wird.[4] Das Arbeitsgedächtnis ist jedoch extrem begrenzt in Kapazität und Dauer, was unter bestimmten Bedingungen das Lernen und die Aufgabenerfüllung behindern kann.[4]
   Die zentrale Feststellung der CLT ist, dass die Qualität des instruktionalen Designs durch die Berücksichtigung der Rolle und der Limitationen des Arbeitsgedächtnisses gesteigert werden kann.[4] Hohe kognitive Last kann die Aufgabenerfüllung negativ beeinflussen.[4] Insbesondere beim Lesen und Verstehen von Code wird es deutlich schwerer, sobald die kognitive Last den Schwellenwert von etwa vier Informationseinheiten im Arbeitsgedächtnis überschreitet.[3]
   4.2 Differenzierung und Minimierung der Extrinsischen Kognitiven Last
   Die CLT unterscheidet drei Arten kognitiver Belastung, die sich den begrenzten Raum im Arbeitsgedächtnis teilen [5]:
4. Intrinsische Kognitive Last: Der Aufwand, der mit der inhärenten Schwierigkeit oder Komplexität eines spezifischen Themas oder einer Aufgabe verbunden ist.[3, 4]
5. Extrinsische Kognitive Last (Extraneous Cognitive Load): Die unnötige kognitive Bürde, die durch schlechtes instruktionales Design, Erklärungen oder irrelevante Elemente entsteht.[5, 6] Sie wird durch Faktoren verursacht, die nicht direkt für die Aufgabe relevant sind.[3]
6. Germane Kognitive Last: Die Arbeit, die in die Schaffung dauerhaften Wissens (Schemata) investiert wird.[4, 5]
   Das primäre Designziel in der Mensch-Computer-Interaktion ist die Minimierung der extrinsischen kognitiven Belastung.[5, 22] Während die Germane Last maximiert werden soll, um den Kompetenzzuwachs zu fördern [5], muss die extrinsische Belastung auf ein Minimum reduziert werden.[5] Im Kontext der UI-Erstellung mittels komplexer XML-Syntax [1] resultiert die notwendige Dekodierungsarbeit – das Vorstellen des visuellen Ergebnisses – in unnötiger extrinsischer Last.[5, 6]
   Human-Centered Design dient als strategischer Rahmen, um diese extrinsische Last zu eliminieren. HCD zielt darauf ab, die kognitive Last der Nutzer zu minimieren, wodurch mentale Ressourcen freigesetzt werden, um besser zu performen.[22] Durch die Implementierung von Designstrategien wie dem Kohärenzprinzip, der Vermeidung irrelevanter Elemente und der Reduzierung von Auswahlmöglichkeiten [6, 28] im visuellen Designer wird die unnötige kognitive Bürde beseitigt. Dies ermöglicht es den Fachexperten, sich auf die intrinsische Komplexität ihrer Geschäftsanforderungen und die eigentliche Lösungsfindung zu konzentrieren, anstatt sich mit den syntaktischen Herausforderungen textbasierter Konfigurationen abmühen zu müssen.[22]
   Tabelle 2 verdeutlicht die funktionale Ausrichtung des Prototyps basierend auf der CLT:
   Table 2: Die drei Formen der Kognitiven Last und die Funktion des Prototyps
   Last-Typ
   Definition
   Ziel im UI-Design
   Relevanz für den Prototyp (Reduktion der XML-Last)
   Quelle(n)
   Intrinsische Kognitive Last
   Aufwand, der mit der inhärenten Komplexität der Aufgabe verbunden ist.[3, 4]
   Muss durch Chunking und Strukturierung verwaltet werden, um die Belastung innerhalb der Kapazitätsgrenze zu halten.[3, 4]
   Relevant für die Komplexität der zugrundeliegenden MDSE-Modelle oder Geschäftsanforderungen.
   [3, 4]
   Extrinsische Kognitive Last
   Unnötige Belastung durch schlechtes Design oder Präsentation.[5, 6]
   Muss auf ein Minimum reduziert werden.[5] Erfolg wird durch die Minimierung unnötiger kognitiver Bürden gemessen.[6]
   Direktes Projektziel: Eliminierung der syntaktischen Dekodierungsarbeit, die durch komplexe XML-Dateien verursacht wird [1], zugunsten einer visuellen Repräsentation.
   [1, 3, 5, 6]
   Germane Kognitive Last
   Aufwand, der zur Konstruktion von Schemata und dauerhaftem Wissen (Lernen) dient.[4]
   Sollte maximiert werden, sobald die extrinsische Last minimiert ist.[5]
   Effizienter Transfer von Domänenwissen und Designprinzipien in die UI-Gestaltung.
   [4, 5]
   V. Das Interaktionsparadigma: Direct Manipulation und WYSIWYG
   5.1 Theoretische Fundierung der Direct Manipulation (Shneiderman)
   Die Direct Manipulation (DM) liefert das konkrete Interaktionsmodell, das die theoretischen Anforderungen des HCD an kognitive Entlastung erfüllt. Der Begriff wurde von Ben Shneiderman geprägt [29, 30] und beschreibt Systeme, die Nutzern das befriedigende Gefühl vermitteln, auf sichtbaren Objekten zu operieren, sodass sie sich auf ihre eigentlichen Aufgaben konzentrieren können.[7]
   Die Kernmerkmale von Direct Manipulation, die den WYSIWYG-Designer definieren, sind [23, 29]:
7. Kontinuierliche Repräsentation des Objekts von Interesse: Die zu manipulierenden UI-Elemente sind ständig und sichtbar als greifbare Objekte auf dem Bildschirm präsent.[23, 29]
8. Physikalische Aktionen statt komplexer Syntax: Der Nutzer führt Aktionen durch physische Handlungen oder beschriftete Tastenbetätigungen aus, anstatt abstrakte Befehlssequenzen oder komplexe Syntax (wie in XML) eingeben zu müssen.[29] Interaktionen ahmen reale Aktionen nach.[23]
9. Rapid Inkrementelle Reversibilität: Operationen sind schnell, inkrementell und umkehrbar, wobei ihre Auswirkungen auf das Objekt von Interesse sofort sichtbar sind.[23, 29]
   5.2 WYSIWYG als intuitive, kognitiv entlastende Interaktion
   WYSIWYG-Editoren sind die herausragenden Beispiele für Direct Manipulation in der Softwareentwicklung.[13] Sie ermöglichen die intuitive Interaktion [13], indem sie es Nutzern erlauben, UI-Elemente wie Buttons, Textfelder oder Menüs per Drag & Drop zu positionieren, deren Größe anzupassen und Eigenschaften zu konfigurieren.[13]
   Der WYSIWYG-Designer trägt signifikant zur Reduzierung der kognitiven Last und zur Steigerung der Effizienz bei.[13] Die kontinuierliche Sichtbarkeit von Objekten ist konform mit der ersten Usability-Heuristik, der Sichtbarkeit des Systemstatus.[23] Vor allem aber werden die mentale Modellierung und die syntaktische Dekodierungsarbeit, die bei textbasierten UI-Definitionen (XML) erforderlich sind [1], eliminiert.
   Die DM unterstützt mehrere der von Shneiderman formulierten "Acht Goldenen Regeln des Interface Designs".[31] Insbesondere die Eigenschaft der kontinuierlichen Repräsentation reduziert die Last des Kurzzeitgedächtnisses.[31] Die schnelle Reversibilität von Aktionen [29] unterstützt die Forderung nach Fehlertoleranz und der Erlaubnis zur Umkehrung von Aktionen.[31]
   Die Eigenschaften der Direct Manipulation, insbesondere das sofortige visuelle Feedback und die schnelle Umkehrbarkeit [23, 29], fördern das Design durch "Trial-and-Error"-Experimentieren. Dies ist ein entscheidender Vorteil, da die Zielgruppe, die Citizen Developers, keine formelle Programmierausbildung besitzt und ihre Artefakte oft fehlerhaft sind.[32] Die DM-Schnittstelle reduziert das Risiko beim Experimentieren und implementiert die in ISO 9241-110 geforderte Fehlertoleranz [16], wodurch die Fachexperten Designs schnell testen und verfeinern können, ohne dass die extrinsische Last fehlerhaften Codes ihre Leistung behindert.[3]
   Tabelle 3 fasst die kausalen Zusammenhänge zwischen DM, Usability und kognitiver Entlastung zusammen:
   Table 3: Direct Manipulation als Fundierung des WYSIWYG-Designers
   Eigenschaft der Direct Manipulation
   Definition (Shneiderman)
   Beitrag zur Kognitiven Entlastung/Usability
   Quelle(n)
   Kontinuierliche Repräsentation
   Das Objekt von Interesse ist ständig sichtbar.[29] Elemente sind als tangible Objekte präsentiert.[23]
   Reduziert extrinsische Last, indem es die mentale Modellierung des visuellen Ergebnisses aus Syntax [1] unnötig macht. Erfüllt "Sichtbarkeit des Systemstatus".[23]
   [1, 23, 29]
   Physikalische Aktionen
   Nutzung von Gesten oder Klicks anstelle komplexer Syntax.[29]
   Eliminiert die Notwendigkeit, die Abstraktionen einer Programmiersprache zu erlernen.[33] Unterstützt intuitive Bedienung und Citizen Development.[13]
   [13, 29, 33]
   Rapid Inkrementelle Reversibilität
   Schnelle, umkehrbare Operationen mit sofort sichtbarer Wirkung.[23, 29]
   Stellt informatives Feedback sicher.[31] Implementiert die ISO-Anforderung der Fehlertoleranz [16] und beschleunigt den iterativen Designzyklus.
   [16, 23, 29, 31]
   VI. Citizen Development und die Demokratisierung der UI-Erstellung (Projektwert 2)
   6.1 End-User Development (EUD) und die Rolle des Fachexperten
   Low-Code Development Platforms (LCDPs) stellen einen Schlüssel-Enabler für die Demokratisierung der Softwareentwicklung dar, indem sie das Phänomen des Citizen Development (CD) oder End-User Development (EUD) ermöglichen.[8, 10, 33] Citizen Developers sind Fachexperten ohne traditionelle IT-Ausbildung, die befähigt werden, Softwarelösungen unabhängig zu erstellen und zu modifizieren.[8, 10] Das Ziel von EUD-Tools ist es, Endnutzern die Erstellung oder Modifikation von Software-Artefakten zu ermöglichen, ohne dass signifikantes Wissen über eine Programmiersprache erforderlich ist.[33]
   Für das Gelingen des EUD-Paradigmas sind die Usability-Anforderungen an die Werkzeuge extrem hoch. EUD-Tools müssen hochgradig nutzbar sein, schnell erlernbar und leicht in die Domänenpraxis integrierbar sein, da Endnutzer Code oft nur zur Erreichung kurz- oder mittelfristiger Ziele schreiben, statt dauerhafte Software-Assets zu schaffen.[32]
   6.2 HCD als kritischer Erfolgsfaktor für die Akzeptanz von LCDPs
   Die Forschung identifiziert eine fundamentale Spannung innerhalb von Low-Code-Plattformen zwischen der geforderten Einfachheit für unerfahrene Nutzer und der notwendigen Leistungsfähigkeit für komplexe Geschäftsanforderungen.[10] Die systematische Anwendung von HCD-Methoden ist entscheidend, um diese Spannung aufzulösen und die Akzeptanz, das Engagement und die Usability der Plattform zu gewährleisten.[18] Der prototypische WYSIWYG-Designer löst diese Spannung, indem er die nötige Abstraktionsebene [11] schafft, die es dem Citizen Developer ermöglicht, komplexe UI-Modifikationen durch intuitive, direkte Manipulation vorzunehmen, während die extrinsische, unnötige Komplexität technischer Syntax (XML) eliminiert wird.[5, 13]
   Die Befähigung von Fachexperten zur selbstständigen UI-Anpassung mittels eines HCD-optimierten Designers ist eine strategische Antwort auf die Notwendigkeit schneller Marktadaption und steigert die Wettbewerbsfähigkeit der Organisation.[12] Indem die Organisation IT-Engpässe umgeht und interne Ressourcen nutzt, um Änderungen an IT-Systemen vorzunehmen, wird die Effizienz gesteigert.[8] Low-Code-Plattformen liefern hierdurch einen klaren Time to Market Advantage.[12]
   Die folgende Tabelle verdeutlicht, wie die HCD-Prinzipien direkt auf die Erreichung der Projektwerte Citizen Development und Effizienz einzahlen:
   Table 1: HCD-Prinzipien und ihre Wirkung auf die Projektwerte
   HCD-Prinzip (ISO 9241-110)
   Bezug zur Usability (ISO 9241-11)
   Bezug zum Projektwert (Citizen Dev./Effizienz)
   Quelle(n)
   Explizites Verständnis von Nutzern, Aufgaben, Umgebungen [16]
   Gewährleistung der Eignung für die Aufgabe (suitability for the task) [16] und Effektivität.[25]
   Sicherstellung, dass das Tool die tatsächlichen Bedürfnisse von Fachexperten ohne Programmierkenntnisse erfüllt.[8]
   [8, 16, 25]
   Prozess ist iterativ und durch Evaluation getrieben [16, 17]
   Kontinuierliche Verbesserung von Effizienz und Fehlertoleranz.[27]
   Ermöglicht schnelle und kontinuierliche Änderungen [19] und erhöht die Time-to-Market-Geschwindigkeit.
   [16, 17, 19, 27]
   Design adressiert die gesamte User Experience [16]
   Steigerung der Zufriedenheit (satisfaction) [25] und des Wohlbefindens.[16]
   Höhere Akzeptanz und Adoptionsrate der Low-Code-Plattform bei Fachexperten, was zur Erfüllung der CD-Ziele führt.[10]
   [10, 16, 25]
   VII. Synthese: HCD und das Modellgetriebene Paradigma (MDSE)
   7.1 Der Designer als humanzentrierte Transformationsschicht im MDSE
   Das gesamte System basiert auf den Prinzipien der Modellgetriebenen Softwareentwicklung (MDSE). Die Einbettung des HCD-Prozesses in MDSE-Modelle ist essenziell, um die Usability systematisch über den gesamten Entwicklungszyklus zu gewährleisten.[34]
   Der Low-Code WYSIWYG-Designer agiert in diesem Paradigma als eine humanzentrierte Abstraktionsschicht. Er muss in der Lage sein, die zugrundeliegenden Modelle, welche die Struktur und Logik der Benutzeroberfläche definieren, zu manipulieren. Die Direct Manipulation Schnittstelle transformiert die physischen Aktionen und visuellen Gesten des Citizen Developers in Modellmodifikationen, ohne den Nutzer mit der zugrundeliegenden syntaktischen oder modellbasierten Komplexität zu konfrontieren.

---

7.2 Die Implementierung adaptiver und individualisierbarer UIs
Die Notwendigkeit des prototypischen Designers zur Laufzeitbearbeitung ist eng mit der dynamischen Natur der Usability verbunden. Die Definition der Usability nach ISO 9241-11 ist immer an einen spezifizierten Kontext der Nutzung gebunden.[24] Da dieser Kontext – bestehend aus Nutzer, Plattform und Umgebung – ständig variieren kann [35], wird eine einmalig entworfene UI schnell suboptimal. Moderne Nutzer fordern zunehmend adaptive Schnittstellen, die dynamisch auf ihre spezifischen Bedürfnisse reagieren.[36]
Die Modellgetriebene UI-Entwicklung (MDUID) bietet Lösungen für diesen Bedarf. Sie ermöglicht die Runtime UI Adaptation (RTA) [36] durch die Kopplung der klassischen UI-Modellierung mit separaten Modellen für Anpassungsregeln und den Nutzungskontext.[35] Diese Kopplung ermöglicht eine automatische Reaktion auf Änderungen im Kontext der Nutzung zur Laufzeit.[35]
Die RTA-Fähigkeit des Low-Code-Designers unterstützt direkt das HCD-Designprinzip der Eignung zur Individualisierung (suitability for individualization).[16] Durch die Bereitstellung des Direct Manipulation Editors zur Laufzeit [14] wird der Citizen Developer ermächtigt, die Usability im sich ändernden Kontext selbstständig und effizient zu gewährleisten. Der HCD-Ansatz, der kontinuierliche Iteration fordert [16, 17], findet somit seine technische Entsprechung in der Laufzeitanpassung [14, 36], um die dynamische Usability zu sichern.
VIII. Schlussfolgerung der theoretischen Fundierung
Die Notwendigkeit des prototypischen webbasierten Designers zur Laufzeitbearbeitung von Benutzeroberflächen wird durch eine klare kausale Kette von theoretischen Grundlagen aus der Mensch-Computer-Interaktion und der kognitiven Psychologie fundiert.
Der Ausgangspunkt ist das Defizit der traditionellen, XML-basierten UI-Erstellung, welche eine hohe extrinsische kognitive Last verursacht, indem sie den Nutzer zur Dekodierung abstrakter Syntax zwingt und das limitierte Arbeitsgedächtnis überlastet.[1, 3] Das übergeordnete Ziel des Projekts – die Steigerung der Usability und die Ermöglichung von Citizen Development – wird durch die normative Zielsetzung des Human-Centered Design (HCD) nach ISO 9241-210 validiert.[16]
Der Prototyp implementiert das HCD-Paradigma durch das Interaktionsmodell der Direct Manipulation (DM) und das WYSIWYG-Prinzip.[13, 29] Die Schlüsselmerkmale der DM – kontinuierliche Repräsentation, physikalische Aktionen und schnelle Reversibilität [23, 29] – eliminieren die extrinsische Last, machen das System intuitiv und effizient [13] und setzen mentale Ressourcen frei, um die Leistung zu steigern.[22]
Die Verbindung dieser theoretischen Pfeiler führt zu den angestrebten Projektwerten:

1. Reduzierte Kognitive Last: Die Eliminierung des technischen Syntax-Overheads ermöglicht Fachexperten die fokussierte Arbeit an Geschäftsanforderungen.[22]
2. Citizen Development: Die intuitive DM-Schnittstelle und die Reduktion der Lernkurve [13, 33] demokratisieren die Softwareanpassung, indem sie Nicht-IT-Spezialisten befähigen.[8]
3. Effizienz/Time-to-Market: Die Iterativität des HCD-Prozesses, technisch umgesetzt durch die Laufzeitanpassung (RTA) [14], sorgt dafür, dass die UI-Anpassung kontinuierlich in der kostengünstigsten Phase verbleibt und die Reaktionszeit auf Marktanforderungen massiv beschleunigt wird.[12, 26]
   Die Evaluation der prototypischen Implementierung kann somit anhand quantifizierbarer KPMs wie Time on Task und Error Rates erfolgen [27], welche als direkter Indikator für die erfolgreiche Reduktion der extrinsischen kognitiven Belastung und die Steigerung der Usability dienen.

---

1. UICrit: Enhancing Automated Design Evaluation with a UI Critique Dataset - People @EECS, https://people.eecs.berkeley.edu/~bjoern/papers/duan-uicrit-uist2024.pdf
2. UICrit: Enhancing Automated Design Evaluation with a UI Critique Dataset - arXiv, https://arxiv.org/html/2407.08850v2
3. zakirullin/cognitive-load: Cognitive load is what matters - GitHub, https://github.com/zakirullin/cognitive-load
4. Cognitive load - Wikipedia, https://en.wikipedia.org/wiki/Cognitive_load
5. Reduziere externe Last - Speicherung neuen Wissens - SKILLQUBE, https://de.skillqube.com/2022/03/24/cognitive-load-theory-clt/
6. Guide to Cognitive Load in UX Design| AND Academy, https://www.andacademy.com/resources/blog/ui-ux-design/cognitive-load/
7. Direct Manipulation: - Department of Computer Science and Technology |, https://www.cl.cam.ac.uk/~pr10/iui/shneiderman83.pdf
8. Evaluating low-code development platforms with the CD score - PMC - NIH, https://pmc.ncbi.nlm.nih.gov/articles/PMC12586684/
9. How to Calculate the ROI of Custom Software Development - SumatoSoft, https://sumatosoft.com/blog/how-to-calculate-the-roi-of-custom-software-development
10. Empowering Citizen Developers: Evaluating the Usability of Low-Code BPM Tools in Process Design - EA Journals, https://eajournals.org/bjms/wp-content/uploads/sites/21/2025/07/Empowering-Citizen-Developers.pdf
11. No-Code and WYSIWYG: A Perfect Match - Conor Dewey, https://www.conordewey.com/blog/wysiwyg-and-no-code/
12. Leveraging Low-Code Development Platforms (LCDPs) for Emerging Technologies - World Journal of Advanced Research and Reviews, https://wjarr.com/sites/default/files/WJARR-2022-0127.pdf
13. Direct Manipulation: Exploring the Definition and Use Cases, https://bluezorro.com/blog/what-is-direct-manipulation/
14. UI Adaptation at Runtime - SAP Help Portal, https://help.sap.com/docs/UI_ADD-ON_FOR_SAP_NETWEAVER_20/b4b7cba328bc480d9b373c7da9335537/f1430c0337534d469da3a56307ff76af.html
15. Enabling UI Adaptation at Runtime - SAP Help Portal, https://help.sap.com/docs/ABAP_PLATFORM_BW4HANA/a7b390faab1140c087b8926571e942b7/402b392585834dd38dd381d8f04b2616.html
16. Human Centered Design (HCD) | NIST - National Institute of Standards and Technology, https://www.nist.gov/itl/iad/visualization-and-usability-group/human-factors-human-centered-design
17. Human-Centered Design: A Process for Usability and Success - OpenArc, https://www.openarc.net/human-centered-design-a-process-for-usability-and-success/
18. Leveraging Human-Centered Design to Implement Modern Psychological Science: Return on an Early Investment - ResearchGate, https://www.researchgate.net/publication/347552251_Leveraging_human-centered_design_to_implement_modern_psychological_science_Return_on_an_early_investment
19. What is Human-Centered Design (HCD)? — updated 2025 | IxDF, https://www.interaction-design.org/literature/topics/human-centered-design
20. What Exactly Is Human-Centred Design (HCD) - Nikolay Nikolov, https://www.nikolaynikolov.ch/blog/human-centred-design
21. HCD principles - Introduction to human-centered design - Digital.gov, https://digital.gov/guides/hcd/introduction/principles
22. Human-centered design meets cognitive load theory: designing interfaces that help people think - Semantic Scholar, https://www.semanticscholar.org/paper/Human-centered-design-meets-cognitive-load-theory%3A-Oviatt/86761f81daaf54c5db29d670e431fbbdd58e721e
23. Direct Manipulation: A Fundamental Element of Graphical User Interfaces - UX Tigers, https://www.uxtigers.com/post/direct-manipulation
24. Usability - Glossary | CSRC - NIST Computer Security Resource Center, https://csrc.nist.gov/glossary/term/usability
25. Exploring Usability Enhancements in W3C Process - slide "Usability - ISO 9241 definition", https://www.w3.org/2002/Talks/0104-usabilityprocess/slide3-0.html
26. The ROI of Usability - UXPA International, https://uxpa.org/the-roi-of-usability/
27. Incorporating Metrics into Human-Centered Design (HCD) - Homeland Security, https://www.dhs.gov/cx/metrics/creating-cx-metrics/incorporating-metrics-into-hcd
28. Cognitive Load Theory: Typen und Prinzipien zur Reduzierung - Goldfuchs Software, https://goldfuchs-software.de/blog/cognitive-load-theory
29. Direct manipulation Interfaces. - MIT Visualization Group, https://vis.csail.mit.edu/classes/6.859/readings/pdfs/Hutchins-DirectManipulationInterfaces.pdf
30. Ben Shneiderman - Wikipedia, https://en.wikipedia.org/wiki/Ben_Shneiderman
31. Shneiderman's Eight Golden Rules Will Help You Design Better Interfaces | IxDF, https://www.interaction-design.org/literature/article/shneiderman-s-eight-golden-rules-will-help-you-design-better-interfaces
32. End-User Development | The Encyclopedia of Human-Computer Interaction, 2nd Ed., https://www.interaction-design.org/literature/book/the-encyclopedia-of-human-computer-interaction-2nd-ed/end-user-development
33. End-user development - Wikipedia, https://en.wikipedia.org/wiki/End-user_development
34. Integrating Human-Centered Design into Software Development: An Action Research Study in the Automation Industry - IEEE Xplore, http://ieeexplore.ieee.org/document/6068362/
35. Self-Adaptive UIs: Integrated Model-Driven Development of UIs and their Adaptations, https://cs.uni-paderborn.de/fileadmin/informatik/fg/dbis/Publikationen/2017/ECMFA.pdf
36. A Model-Driven Approach to Graphical User Interface Runtime Adaptation - CEUR-WS, https://ceur-ws.org/Vol-641/paper_15.pdf
