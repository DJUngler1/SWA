# Allgemein 
1) Was ist eine Entity im Kontext von DDD? 
* Eine Entity ist ein Objekt mit einer unveränderlichen und eineutigen Identität und weiteren Attributen.
2) Was ist ein Aggregate? 
* Ein Aggregate ist ein Cluster aus verschiedenen Value Objects und Entities. Ein Aggregate wird als eine transktionelle Einheit betrachtet.
3) Was ist ein Aggregate Root? 
* Ein Aggregate Root bildet bei DDD die einzige Schnittstelle nach außen. (Alle anderen Entites sind nicht von außen zugreifbar und werden über das Aggregate Root aufgerufen)
4) Was ist der Unterschied zwischen Aggregate Root & einem Repository?
* Der Unterschied ist das Aggregte Root bildet ein Entity Objekt ab, as Repository führt mit dem Aggregate Root Opertationen auf der Datenbank aus.
5) Was ist das Repository (Pattern)? 
* Das Repository ist die Abstraktion des Persistenz Mechanismus. Es führt mit dem Aggregate Root Opertionen auf der Datenbank aus.
6) Was ist ein Value Object? 
* Ein Value Object ist ein kleines unveränderliches Objekt das statt Strings zum Vergleich mit anderen Objekten genutzt wird.
7) Was ist ein Bounded Context? 
* Ein Bounded Context ist eine logische Gruppierung zusammenhängender Funktionalität. Jeder Bounded Context hat sein eigenes Domänenmodell. Ist von anderen Bounded Contexten abgegrenzt und orientiert sich an den Geschäftsvorfällen
8) Was ist ein Service?
* Ein Service bildet bildet die fachliche Logik mit Hilfe der Entities Value Objects und des Repositories ab. Services sind in der Regel zustandslos
9)  Erklären Sie den Unterschied zwischen einem Thread, Stack und Heap! 
* Ein Thread ist ein sequentieller Ausführungssttrang von Anweisungen, der zu genau einem Betriebssystempprozess gehört.
* Ein Stack gehört zu genau einem Thread, in eine Stack werden alle Anweisungen und Referenzen des Threads gespeicher und nach dem LIFO Prinzip abgearbeitet.
* Ein Heap ist eine dynamische Speicherallokation die genau zu einem Betriebssystemprozess gehört, alle Threads des Prozesses teilen sich den Heap.
10)  Was können wir bei Kotlin anders machen als in C# in Bezug auf
If-Anweisungen/When-Anweisungen/Try-Catch-Anweisungen?
* Da es sich in Kotlin nicht um Anweisungem sondern um Ausdrücke handelt können diese anderst als in C# rechts vom Gleichetszeichen stehen also direkt einer Variablen zugewiesen werden.
11) Was ist ein ENUM? 
* Ein Enum ist ein Daten Typ der die Werte von vordefinierten Konstanten annehmen kann.
12) Erklären Sie Domain-Driven-Design anhand eines Beispiels!
* Domain Driven Design ist ein Modelierungskonzept für die technische Umsetzung eines fachlichen Prozesses. 
1)  Was könnten Ursachen für die Entstehung von Big Data sein und was könnte zu Problemen beim
Monolithen führen? 
* Die Ursachen für die Entstehung von Big Data sind, IoT, Social Media, Process Mining. Bei Monlithen sorgt die Menge und die große Anzahl an Unterschiedlichen Datenformaten für Probleme. Durch Speicherung von all dem auf einer Datenbank wird der Zugriff immer langsmer.
1)  Warum sollten .yml-Dateien (YAML) für Konfiguration benutzt werden (Vorteil)? 
* YAML ist leichtgewichter, leichteer lessbar als Vergleichbare Alternativen z.B XML. YAML hat mächtige Ausdrucksmöglichkeiten und zwischen vielen Programmiersprachen portabel
1)  Welche Nachteile haben .yml-Dateien? 
* 
2)  Was ist Backpressure? 
* Backpressure ist der Umgang mit Überlast wenn zu viele Anfragen eigehen. Der Publisher produziert nur bis zu einer Obergrenze der Subscriber abboniert nur bis zu einer Obergrenze. Alle Anfragen die über diese Grenzen gehen werden entweder zurückgewiesen oder an andere Server mit freien Kapazitäten weitergeleitet.
3)  Beschreiben Sie 3 Vorteile, die IntelliJ IDEA im Vergleich mit Editoren, wie Notepad++ hat? 
* Refactoring: Um Klassennamen nachträglich zu ändern
* Autovervollständigung von Variablennamen.
* Codenavigation: mit Steurung+Linksklick auf einen Variablen/Klassennamen kommt man zu deren Definiion.
1)  Vorteile von IntelliJ - IDE?

2)  Was sind “one-way-functions” ? 
* Funktionen die keine Inverse besitzten, also injektiv sind.
3)  Erklären Sie nicht-blockierende Verarbeitung! 
* Bei der nicht blockierenden Vearbeitung warten Threads wenn sie eine Anfrage an ein externe Ressource stellen nicht auf das Ergebniss sondern können direkt die nächste Anweisung durchführen.
4)  Warum sollte asynchron statt imperativ programmiert werden? 
* Wenn man erwartet das die eigene Anwendung sehr viele Anfragen bekommt sollte asynchron entwickelt werden. Oder wenn man nicht auf den Eingang von Ergebissen warten möchte sondern diese nach und nach als Stream versendet/bekommt.
5)  Erläutern Sie, warum nicht jede Server-Anwendung „reactive“ entwickelt wird! - KlausurFrage 
* Wenn ein Anwendung mit imperativer Programmierung keine Probleme mit der Skalierung hat gibt es keinen Grund diese reactive zu entwickeln.
6)  Erläutern Sie Probleme bei Reactive Programming!* - KlausurFrage 
* bei einzelenen Requests langsamer als imperative Programmierung. Thread Management deutlch aufwändiger als bei imperativen Programmierung.
7)  Erklären Sie was ein Stacktrace ist.- Klausur-Frage 
* Im Stacktrace werden alle Anweisung des Stacks in der Reihenfolge wie sie ausgführt wurden gelistet.
8)  Vergleichen Sie Boundary Control Entity & Schichtenarchitektur? 
* 
9)  Wann ist es sinnvoll, den Cache in die Anwendungslogik zu implementieren? 
* 
10) Erklären Sie die 4 Eigenschaften des Reactive Manifesto (MRRE)! 
* message driven: Reaktion auf aynchron eingehende Nachrichten
* resillient: Reaktion auf Ausfälle z.B durh zu viele Requests
* elastic: Reaktion auf wechselnde Last
* responsive: Reagieren auf Request schnell und mit hoher Verfügbarkeit
1)  Grenzen Sie Funktionen, Methoden und Prozeduren voneinander ab! 
* Methoden sind Funktionen sind Funktionen die auf Objekten aufgerufen werden. 
12) Was macht die Funktion findById() in der Handler Klasse? 
* Die Funktion findById der Handler Klasse wird über den Router aufgerufen und sucht mithilfe des Services das Kundenobjekt mit der zugehörigen Id und baut das Response Objekt. Wenn die Id nich gefunden wurde einen leeren Body mit statuscode NotFound 404, wenn die Id gefunden wurde wird der Body gebaut mit Statuscode 200 im Header
13) Erklären Sie den Unterschied zwischen Flow und List in Kotlin! 
* bei einer List müssen zum Übertragen der Liste alle Objekte da sein die Elemente eines Flows können nach und nach übertragen werden.
14) Was ist der Unterschied zwischen einer Menge/Set und einer Liste? 
* Eine Liste hate eine Reihenfolge eine Menge nicht und bei einer Menge dürfen keine Elemente doppelt vorkommen
15) Was ist der Unterschied zwischen Mutablelist und Flow? 
* selebe wie List Flow
16) Warum ist es sinnvoll, BigDecimal und nicht float/double zu verwenden? 
* bei BigDecimal werden mehr Nachkommastellen abgebildet also kommt es zu weniger Rundungsfehlern weshalb BigDecimal genauer ist als double
17) Erklären Sie den Zusammenhang von ETags & If-None-Match bei einem GET-Request & einem wiederholten
GET-Request! 
* Wenn der Kunde einen GET-Request macht wird ein E-Tag mitgeschickt welches die Versionsnummer beinhaltet. Bei einem erneuten GET-Request wid das die Versionsnummer mit If-None-Match mitgeschickt, das heißt dem Client werden die Daten nur dann geschickt wennn seine mitgeschickte Versionsnummer ungleich der aktuellen Versionsnummer wenn gleich hat er schon die aktuellsten Daten.
1)  Erklären Sie ETags! 

2)  Was ist ein bedingter GET-Request? bedingt→ if 
* Ein bedingter GET-Request ist ein GET-Request der nur unter einer bestimmten Bedingung ausgeführt wird. Die Bedingung könnte zum Beispiel If-Non-Match
3)  Wie viele verschiedene Kombinationen gibt es bei 4 Checkboxen? - Klausurfrage 
* 2^4 = 16
4)  Unterschied Forward- und Reverse-Proxy? 
* Ein Forward Proxy ist für einen kontrollierten Zugang zum Internet. Ein Reverse-Proxy nimmt Anfragen aus dem Internet stellvertretend für einen Server an und leitet diese weiter.
5)  Was sind Servlets und wie werden diese verwaltet? 
* Servlet sind kleine Anwendungen basierend auf Java Klassen die in einem Web-Container laufen
6)  Erklären Sie die Aussage „Make JAR, not WAR“! - swe schauen 
* bei JAR Dateien befindet sich der Webcontainer im Archiv und wird beim Deployment automatisch mitgestartet. Besser als WAR hier muss das Archiv gabaut werden und dann in einen laufenden Weberver gelegt werden.
7)  Erläutern Sie, was durch den Produktnamen „Spring Boot“ ausgedrückt werden soll. 
* Damit wird impliziert das es beim starten "booten" des Server unterstüstzt.
8)  Was ist ein Web-Container? 
* Ein Web-Container läuft einem Webserver und ist Laufzeitumgebung für Servlets.
9)  Was macht ein embedded Web-Container? 
* Ein Embeded Web-Container ist muss nicht extra gestartet werden er befindert sich im Archiv und wird beim Deployen automatisch gestartet.
10) Was ist Netty? 
* Netty ist ein Embeded Web-Container.
11) Unterschied Tomcat und Netty?s 
* Netty ist leichtgewichtiger Tomcat.
12) Wieso werden Microservices als Anwendungsdatenbank bezeichnet? 
* Microservices werden als Anwendungsdatenbanken bezeichnet weil sie sich auf genau einen Geschäftsvorfall beziehen und in der Regel eine eigene Datenbank in der 
13) Was sind Microservices? 
* Ein Microservice bildet einen Bounded Context ab und bildet eine Deploymenteinheit. Er fürt genau ein Business Case durch.
14) Was sind die Prinzipien von REST? 
* Verwendungung von URIs zur Identifiklation von Ressourcen
* HTTP-Mehtoden für den Nachrichtenausausch
* JSON als Übertragungsformat
1)  Nennen Sie 2 MIME-Typen, die bei Microservices häufig verwendet werden! 
* application/json
* application/text/html
1)  Erklären Sie IAM anhand von Social Logins! 
* Identity acces Mangement ist die Autorisierung von Benutzern. Bei Social Logins werden externe Plattformen verwendet um die Autorisierung von Benutzern durchzuführen.
2)  Was ist der Unterschied zwischen IAM und IDM? 
* IAM ist die Autorisierung von Benutzern also die Verwatlung von deren Rechten. IDM ist Athentifizierung von Benutzern.
3)  Erklären Sie die Annotation @Bean! 
* mit @Bean werden Funktionen annotiert die zur Laufzeit benötigt werden und deshalb von Spring vorgeladen werden.
4)  Erklären Sie den Unterschied zwischen @Bean & @Configuration 
* eine Funktion die mit @Bean annotiert ist muss zu einer Klasse gehören die mit @Configuration annotiert ist.
5)  Was macht die Annotation @Version? 
* Wird vor die Property für die Versionsnummer eines Datensatzes geschrieben damit gibt man die Verwaltung der Versionsnummer an Spring Data weiter.
6)  Erläutern Sie, warum man bei Kotlin-Property, die mit @Version annotiert ist, auch die Annotation @JsonIgnore
verwendet wird. 
* Da die Versionsnummer vom Client nicht benötigt wird annotiert man diese mit @JsonIgnore sodass Jackson diese nicht mit in das JSON Objekt schreibt. 
1)  Wie ist das Hauptprogramm eines Microservices annotiert? 
* Mit @SpringBootApplication
2)  Was besagt Annotation @Component? 
* Damit teilt man Spring mit das die annnotierte Klasse an anderer Stelle für eine Depency Injection genutzt wird.
3)  Pfad/Query-Parameter, was wird wann genutzt? 
* Pfad Parameter werden genutzt wenn nur ein Wert oder alles abgefragt wird und wenn der Pfad möglichst kurz sein soll. Wenn eine Abfrage mehrere Parameter hat und für leichtere lesbarkeit Verwendet man Query Parameter
4)  Erklären Sie Singletons anhand eines Beispiels! 
* Ein Singelton ist eine Klasse von der es nur eien Instanz geben darf, z.B. von der Service Klasse soll es 
5)  Was bedeutet Annotation @Service? 
* Damit teilt man Spring mit das die annnotierte Klasse an anderen für eine Depency Injection genutzt wird, und das es sich um die Service Klasse handelt.
1)  Was bedeutet Annotation @JsonPropertyOrder? 
* dadurch wird bestimmt in welcher Reihenfolge Jackson die Attribute einer Klasse verarbeitet. z.B (@JsonPropertyOrder("vorname", "name", "geburtsdtum"));
2)  Wie heißen Annotationen in C#? 
* In C# heißen Anootationen Attribute
# Kotlin 

73) Was sind die Ziele von Kotlin? 
* wenig und leicht verständlicher Code.
* einfache Nutzung von fremdbibliotheken
* Kompatibilität mit anderen Programmiersprachen
* gute Werkzeugunterstützung
1)  Nennen sie 4 Vorteile von Kotlin? 
* smart cast satt type cast
* Kotlin ist nullsafe außer man konfiguriert das Wert Null angenommen werden kann
* Keine Semikolons am Zeilenende
* Named Parameter statt Builder Pattern
75) Nenne 4 typische Anfängerfehler in der Entwicklung? 
* keine selbsterklärenden Namen werden verwendet
* falsche Codeformatierung 
* keine oder fehlerhafte kommentare
1)  Wie erstellt man ein „immutable“ Objekt in Kotlin? 
* Objekte in Kotlin sind standardmäßig immutable
2)  Wie erstellt man ein „immutable“ Property in Kotlin? 
* Eine immutable Proberty erstell man in Kotlin mit dem Stichwort val. Bsp. val name = ...
3)  Erklären Sie die Funktionsweise von „Extension functions“ bei Kotlin?
* Mit Extension Functions kann man Klassen nachträglich um Funktionalität ergängzen ohne dabei die Klasse selbst zu ändern
4)  Wie wird die Funktionalität von Extension Functions (Kotlin) in C# realisiert?
* Extension Functions Functions werden in C# durch Extentions Methods realisiert.
5)  Wie lautet die Reihenfolge der Variablendeklaration? 
* Frage ist dumm
6)  Was ist eine Higher-Order Function? – KlausurFrage
* Eine Higher-Order Function ist eine Funktion die als Parameter eine andere Funktion entgegenimmt oder als Rückgabewert.
7)  Wieso braucht man Lambda-Ausdrücke in Higher-Order Functions?
* Mit Lambda-Ausdrücken kann man anonyme Funktionen als Parameter für Higher-Order Funtions
8)  Was sind pure functions? – phase6 15
* pure function sind Funktionen die beim selben Eingabewert immer den selben Rückgabewert liefern. z.B. Funktion zur Berechnung der Mehrwertsteuer.
9)  Erklären Sie eine Single Expression Function anhand eines Beispiels! - KlausurFrage 
* Eine Single Expression Function ist eine Funktion die nur einen Ausdruck hat. Bsp: fun function(val number) = number * 5
10) Erklären Sie Syntax & Semantik des folgenden Codefragments: 

11) Erklären Sie die Semantik der folgenden Codezeilen: 

12) Nennen Sie 4 Aspekte guter Codequalität
* sinnvolle leicht zu verstehende Namen
* einheitliche Einrückung
* sinnvolle verständliche Kommentare
* gute Dateistrukturierung innerhalb eines Projekts.
13) Was ist Type Aliases? 
* Vergeben von anderen Namen für einen Typen. Dieser Name kann dan anstelle des Typen verwendet werden.
14) Was macht die Funktion retrieve()? 

15) Was macht die Funktion runBlocking{}?
* runBlocking{} blockiert die Ausführung eines Threads bis die Coroutinene fertig sind.
16) Wie geht Kotlin mit null-Status um?* - Klausur-Frage 
* In standardmäßig nichts den Wert null annehmen der Wert null kannn nur dann angenommmen werden wenn wir den Code so schreiben das etwas null sein darf.
17) Erklären Sie den Safe Call Operator? 
* MIt dem Safe Calll Operator wird geprüft ob etwas den Wert null hat, eine weiter Operation wird nur durchgeführt wenn es nicht den Wert null hat.
18) Erläutern Sie, wie man in Kotlin anders als in C# programmieren kann, weil es if-Ausdrücke gibt. 
* Man kann if Ausdrücke rechts vom Gleichheitszeichen schreiben
19) Erläutern Sie, warum suspendierbare Funktionen von Kotlin besser sind um„reactive“ zu programmieren. -
KlausurFrage 
* Suspendierbare Funktionen können unterbrochen und später fortgesetzt werden damit lässt sich die nicht blockierende Verarbeitung die bei reactive Programming angenommen wird gut umsetzen.
95) Was ist eine SAM? 
* eine Singel Abstract Method ist ein funktionales Interface mit genau einer Methode.
96) Was ist ein Companion Object? 
* Ein Singelton das zu einer Klassse gehört wird statt static verwendet.
97) Was ist eine Kotlin Coroutine? 
* leichtgewichte benutzerlevel Threads werden in Kotlin zur Umsetzung nicht blockierender Verabeitung genutzt.
98) Erläutern Sie, wie man prinzipiell “Sealed Classes“ statt Exception zur Fehlerb. verwendet?- Klausur-Fragen 
* Man definiert eine Klasse für den Fehler und für den erfolgreichen Fall statt try und catch Blöcke in denen man Exception fängt vewendet man diese Klassen.
 
# Grundlegende Konzepte heutiger Softwareentwicklung 

99) Was sind die grundlegenden Konzepte heutiger Softwareentwicklung? 
* Dependeny Injections
* Convention over Configuration
* funktionale Programmierung 
* Builder Pattern
100) Was ist eine Dependency Injection (DI) anhand eines Beispiels in ihrem Projekt? 
* Bei einer Depency Injection wird eine Instanz einer Klasse in den Konstruktor einer anderen Klasse injiziert.
* class MitarbeiterHandler(private val service: MitarbeiterService){...}
1)   Was bedeutet Inversion of Control (IoC)? 
* Abgeben der Kontrolle an eine Plattform, z.B Spring.
2)   Warum sollte Dependency Injection, die Constructor Injection und nicht die Field Injection nutzen? 
* Bei der Constructor Injection kann man die Abhängigkeiten der Klasse leichter sehen, da direkt im Konstruktor der Klasse. Und im Gegensatz zur Field Injection kann es bei der Constructor Injection keine endlos Rekursion geben.
3)   Was bedeutet Convention over Configuration (CoC)? 
* Wir haben sinnvolle Defaultwerte sodass wir nur noch Ausnahmefälle konfigurieren müssen. Configuration by Exception.
4)   Erklären Sie Convention over ConfigurationW (CoC) am Beispiel von JSON und Kotlin Objekten! 
* Bei Jackson werden Standarmäßig alle Werte transformiert außer solche die wir mit @JsonIgnore annotiern.
5)   Wann verwendet man Jackson? 
* Jackson wird verwendet um JSON-Objekte in Kotlin-Obejekte zu konvertieren und umgekehrt.
6)   Was versteht man unter dem Builder Pattern + Bsp im eigenen Projekt?
* Unter dem Builder Pattern versteht man die Verkettung von Funktionen. return ok().bodyValueAndAwaiit(Mitarbeiter)
7)   Wieso sind Named Parameters besser als das Builder Pattern? 
* Named Parameter sind leichter verständlich und unabhängig von der Reihenfolge in der sie definiert wurden.
8)   Erklären Sie das LIFT-Prinzip! 
* L ocating our code is easy
* I dentify code at a glance 
* F lat structure as long as we can
* T ry to stay DRY (Dont Repeat Yourself)
* 
# Statuscodes 

1)   Welche Statuscodes kommen bei einem fehlgeschlagenen POST Request bzw. PUT-Request zurück? 
* ein passender 400 er code oder 500 wenn es sich um einen internen Fehler handelt
2)   Was geben die Statuscodes 200,201, 204 zurück. Nenne auch die aufgerufene HTTP-Methoden. -phase6 
* 200 ist ok kommt z.B bei einem GET Request zurück. 201 created, bei einem erlorgreich post request , 204 no content kommt bei einem erlogreichen put oder patch request zurück
3)   Erklären Sie das Zusammenspiel von Client und Server!  
* Der Client schickt eine Anfrage in Form eines HTTTP-Request an den Server der Server verarbeitet den Request und sendet einen Response dessen Header enthält enthält Info darüber ob der Reques erfolrgreich war in Form eines Statuscodes
4)   Nenne 2 Authentifizierungsverfahren bei RESTful Webservices! 
* Anmelden mit Eingabe von Benutzerkennung und Passwort
* Anmelden durch mitsenden eines Tokens
5)   Wieso ist es bei verteilten Systemen mit Microservices problematisch BASIC-Authentifizierung zu
verwenden? 
* bei jedem Request an einen der Microservices müsste man erneut Benutzername und Passwort mitsenden.
1)   Wie funktioniert Token?
* Ein Token enthält einen Schlüssel und eine Gültigkeitsdauer, man sendet das Token mit dem Request mit. Das Token wird validiert und der Client is eingeloggt solange das Token gültig.
# HATEOAS 

1)   Erläutern Sie HATEOAS mit Beispielen von Unternehmen wie PayPal, Facebook, …! 
* Bei HAtEOAS werden mit dem Request links mit gesendet entweder in Form von Atom-Links oder Link-Header. Bei Paypal zum Beispiel wird bei einer ausgeführten Zahlung direkt der Link zum Beleg der Zahlung mitgesendet.
2)   Erklären Sie den Unterschied zwischen Atom-Links & Link-Header! 
* Atom-Links sind selbserklärende URIs im Body des Respomse, Link-Header sind selbserklärende URIs im Header des Response
3)   Erkläre Unterschied zwischen URI und URL! 
* URI ist ein eindeutiger bezeichner für eine Ressource. Bei einer URL ist zusätzlich noch die Information enthalten wie auf die Ressource zugergriffen werden kann. Jede URL ist auch eine URI aber nicht umgekehrt
4)   Was ist der Unterschied zwischen Structural Links & Transitional Links? 
Datenbankzugriff und Spring Data (MongoDB) 

1)   Was heißt eventually consistent? 
* Mehrere Datenbank sollen untereinader Konsistenz sein aber nicht sofort sondern nur irgendwann zu einem späteren Zeitpunkt
2)   Erklären Sie die Funktionsweise bei optimistischen DB-Transaktionen!
* Bei optimistischen Datenbanktransktionen wird die Ressource nicht gesperrt sondern es kann auch von anderen Request auf die Ressource zugegriffen.
3)   Wieso ist es bei verteilten Systemen sinnvoll keine pessimistische Synchronisation zu verwenden? 
* weil wir bei peseimistischen Transaktionen über mehrere Microservices hinweg eine Ressource blockieren müssten was extrem aufwändig ist
4)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Änderung: Update - Update 
* die eigene Änderung kann nicht durchgeführt werden weil die Ressource blockiert ist.
1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als die eigene Änderung: Update - Delete 
* dann wird der Datensatz neu angelegt mit der Änderung.
1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Löschen: Delete - Update 
* Der Datensatz wird erst geändert dann gelöscht.
1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als das eigene Löschen. Delete - Delete 
* Dafür vorlesung ansehen
1)   Wie beschreibt man Abhängigkeiten in SQL bzw. MongoDB? 
* in SQL mit Fremdschlüsseln, MongoDB mit Embedded Documents
2)   Nennen Sie zu Collection, Document & Embedded Document, die dazugehörigen Gegenstücke in
relationalen DB-Systemen. 
* Collection - Tabelle
* Document - Tabellenzeile
* Embeded Document - Fremdschlüssel
1)   Unterschiede von MongoDB & relationaler DB? 
* Field in  Mongo - Spalte in relationaler DB
* sparse in Mongo - Null in relationaler Db
* Progammatische Queries - SQL
2)   Was ist das Schema bei relationalen Datenbanken? 
* Das Schema ist das CRREATE Table
1)   Erklären Sie die Unterschiede zwischen relational und objektorientiert! 
* relational mehrere Tablenen die Über Fremdschlüssel referenziert werden. Objektorientiert ein Objekt mit untergeordneteten Objekten
2)   3 Unterschiede zwischen REST und DDD? 
* REST Uris vs DDD Ids
* REST E-Tag vs DDD Version
* RESt link vs DDD Relation
3)   Wie werden Beziehungen in rel. DB, JSON Documents & Kotlin Objekten realisiert? 
* Bei relationalen DBs durch Fremdschlüssel bei, JSON durch Embedded Documents, bei Kotlin durch Referenzen.
4)   Wann benutzt man ReactiveCrudRepository & wann ReactiveMongoOperations? 
* ReactiveCrudRepository benutzt man für den Zugriff auf eine relationale Datenbandk. ReactiveMongoOperations benutzt man für den Zugriff auf ein Monogo Datenbank.
5)   Vergleichen Sie die Abfrage einer relationalen DB mit der Abfrage in MongoDB! 
* Bei einer Abfrage in Mongo DB sind keine Tranksaktionen notwendig bei  außer beim Zugriff auf mehrere Documents gleichzietig, bei raltionalten DBs immer. Bei relationalen DB gibt es eine Query Language bei MongoDB funktionale Queries.
1)   Erklären Sie 2 Pattern aus DDD, die bei Spring Data ähnlich verwendet werden? 

2)   Beschreiben Sie die 4 Stores von NoSQL-Systemen! 
* Document Store, Daten werden in Dokumenten gespeichert meisten in Form von JSON Objekten
* Key-Value Store: Speichern von Key Value Paaren in einem BLOB
* Column Sotore: Speichern von Datensätzen in Zeilen
* Graph Database: Darstellung von Daten durch Beziehungen zwischen Knoten
3)   Warum sollte MongoDB und nicht relationale DB genutzt werden? 
* hoch skalierbar
* mächtige Query Syntax
* asynchroner Zugirff auf MongoDB möglich
* JSON-Schema möglich aber nicht notwendig
4)   Was ist umständlich an MongoDB? 
* Join über mehrere Dokumente nur schwer möglich bis unmöglich
* keine Qeury Language
1)   Wieso werden Transaktionen bei MongoDB nicht wirklich benötigt. 
* Weil wir im normalfall nur Änderungen auf einem Dokument durchführen
2)   Beschreiben Sie, wann man bei MongoDB bei einem Schreibvorgang keine explizite Transaktion benötigt! 
* wenn der Schreibvorgang nur auf einem Dokument durchgeführt wird
3)   Beschreiben Sie, wie man sinnvollerweise interaktiv inspiziert, ob Daten in MongoDB auch wirklich
eingefügt oder aktualisiert wurden. 
* Durch betrachten der Daten mit einem Werkzeug wie MongoDB Compass
1)   Beschreiben Sie, was man unter „Type-Safe Queries“ versteht. 
* Bei Vergleichen Value Objects statt Strings bnenutzen
2)   Beschreiben Sie eine Möglichkeit, wie man in einem Spring Profile z.B. „dev“, prinzipiell die Testdaten in der
DB zurücksetzen kann.
* Beim Starten wird das Profile überprüft und jenach Profile wird die Datenbank zurückgesetzt oder halt nicht.
# Tests 

1)   Was bedeutet „just Runs“ in der Syntax? 
* der Test soll nur durchlaufen das Ergebnis ist egal der die Funktion hat keinen Rückgabewert
2)   Was macht Mocking? 
* Mocking täuscht einen Datenbankzugriff vor und es werden Testdaten eingelesen
3)   Was macht Funktion „every“? 
* Higher-Order Function definiert welches verhalten gemockt werden soll
4)   Was macht die Annotation @Nested? 
* Dadurch wird die Schachtelung von Testklasse ermöglicht
5)   Was macht die Annotation @Order und warum steht in den Klammern von @Order eine 1000? 
* Mit @Order wird die Reihenfolge der Tests festgelegt. @Order(1000) deshalb da noch genug Platz ist um neue Tests einzufüggen
6)   Was macht die Annotation @Disabled? 
* Mit @Disabled wird ein test deaktiviert
7)   Warum und wann sollte getestet werden? 
* Getestet werden sollte immer dann wenn eine Komponente fertig ist. Testen ist wichtig um die Funktionalität zu Überprüfen.
8)   Wofür steht die Annotation @CsvSource? 
* Bei Prametrisierten Test auslesen der Werte aus einer CSV Datei
9)   Nach welcher Funktionalität sollten Testklassen aufgebaut sein orientieren sie sich an CRUD? 
* Frage ist lost testen orientiert sich nicht an CRUD
10)  Nenne die bekanntesten Testarten und beschreibe Sie! 
* Unit-Test: Testen von kleinen Funktionalitäten, Unit Tests sind voneinander unabhängig
* Integrationtest: Testen der Integration von Komponenten 
* End-to-End Test: Tests über das gesamte System angefangen mit der Benutzerschnittstelle
11)  Erklären Sie AAA bei Unit-Tests! 
* arrange: setzen der vorraussetzungen und erwarteten Ergebnisse für die Tests
* act: ausführen der eigentlichen Tests.
* assort: Testergebnisse mit den erwarteten Ergebnissen vergeleichen
12)  Warum kann man bei der Testentwicklung in Kotlin von Specificationlike Test sprechen? 
* Im Funktionsnamen kann abgelesen werden was getestet wird.
13)  Was versteht man unter SoftAssertion 
* Wenn einer der Tests fehlschlägt bricht nicht alles ab sondern asführung geht weiter am Ende werden die nicht erfolgreichen Tests angezeigt.
14)  Was ermöglicht uns Kotest? 
* Überprüfung von Testergebnissen mit Hilfe von Infix Opreatoren
# Security 
  
1)   Was ist der Unterschied zwischen Authentifizierung und Autorisierung? 
* Authentifizierung ist das einloggen von Benutzern, Autorisierung die Überprüfung von den Zugriffsrechten eines Benutzers
1)   Was macht die Annotation @PreAuthorize(„hasRole(‚Rolle‘)“)? 
* Dadurch wird festgelegt das eine Funktion nur mit der in der Klammer spezifizierten Rollle ausgeführt werden kann.
1)   Was ist der Unterschied zwischen einer Rolle und einer Gruppe? 
* Eine Rolle ist eine Menge von Zugriffsrechten die einem Benutzer zugewiesen werden kann eine Gruppe ist eine Menge von Benutzerkennungen.
2)   Erkläre die Abkürzung SSO! 
* Single Sign on, nur eine Anmeldung danach ist man im ganzen Cluter angemeldet
# Logging 

1)   Welche Log-Level gibt es und für wen sind diese interessant ? 
* FATAL - Fatale errors, führen zu absturz, Entwickler, Admin
* ERROR - Fehler die aber nicht zu Absturz führen müssen, Entwickler,Admin
* WARNING - Noch kei Fehler kann aber zu einem Fehler führen, Entwickler,Admin
* INFO - Information über Ablauf einer Funktion, start des Servers, Admin
* DEBUG - wen angefragt zeigt an welche Fehler wo passieren, Entwickeler
* TRACE, Entwickler
1)   Warum {} besser als () ist, erklären Sie anhand diesem Codebeispiel? 
Apache Log4j2 kann Lazy Logging ? 
* Wenn () wird erst dann geladen wenn gebraucht werden
1)   Beschreiben Sie eine Log-datei? 
* Ein Eintrag in Lodatei besteht aus Zeitstempel loglevel Packagename Message Rechnername und Prozess Id.
1)   Warum ist Trailing Comma ein tolles Feature? 
* Man kann die einzelnen Bestandteile vertauschen und neue Sachen hinzufügen ohne das Fehler durch vergessene Kommas passieren 
1)   Erklären Sie die Impedance Mismatch? 
* Bei Umwadeln von n zu n Beziehungen von Objektorientiert zu relational müssen für eine korrekte Abbildung Zwischetabellen angelegt werden.
1)   Beschreiben Sie die 4 Interfaces in Reactive Streams? 
* 
# Codebeispiele 

1)   Wo ist hier der Denkfehler im Codefragment ? 

2)   Schreiben Sie den nachfolgenden Code so um, das Lambda-Ausdrücke verwendet werden. 

3)   Schreiben Sie folgenden Code mit Lambda Ausdrücken. 

4)   Was ist an folgendem Code schlecht? 

5)   Beschreiben Sie den Code nach der Syntax (Code-Fragment wurde vorgegeben von Router Function) 

6)   Beschreiben Sie folgendes Codebeispiel nach der Semantik