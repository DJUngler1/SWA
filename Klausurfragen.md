# Allgemein 
1) Was ist eine Entity im Kontext von DDD? 

Eine Entity ist ein Objekt mit einer unveränderlichen, eindeutigen Identität und weiteren Attributen.

2) Was ist ein Aggregate? 

Ein Aggregate ist eine Gruppe von Entities, die einer Domain angehören. 

3) Was ist ein Aggregate Root? 

Ein Aggregate Root ist Teil eines Aggregates und bildet die einzige Schnittstelle nach außen.

4) Was ist der Unterschied zwischen Aggregate Root & einem Repository?

Das Repository stellt die Operationen mit den Aggregate Roots dar. Dabei finden keine Transaktionen über die Grenze des Bounded Context statt.

5) Was ist das Repository (Pattern)? 

Das Repository ist die Abstraktion des Persistenzmechanismus.

6) Was ist ein Value Object? 

Ein kleines, unveränderliches Objekt, dass statt Strings für die Validierung verwendet wird.

7) Was ist ein Bounded Context? 

Eine logische, in sich abgeschlossene Gruppierung von zusammengehöriger funktionalität.
Er hat ein eigenes Domainmodell und orientiert sich an Geschäftsvorfällen.

8) Was ist ein Service?

Er bildet die fachliche Logik unter verwendung von Repositories, Entities und Value Objekts ab

9) Erklären Sie den Unterschied zwischen einem Thread, Stack und Heap! 

ein Heap ist für die Dynamische Speicherallokation eines Betriebssystem Prozesses.
Ein Thread gehört zu einem Betriebssystem Prozess und ist ein Ausführugnsstrang.
Ein Betriebssystem Prozess kann mehrere Threads kontrollieren (multithreading)
Ein Stack ist ein Speicherbereich von genau einem Thread, der bei Funktionsaufrufen reserviert wird.
Der Stack speichert Referenzen auf Argumente und lokale Variablen und wird nach dem LIFO-Prinzip abgearbeitet.
Die Stacks befinden sich im Heap des Prozesses.

10) Was können wir bei Kotlin anders machen als in C# in Bezug auf
If-Anweisungen/When-Anweisungen/Try-Catch-Anweisungen? 

Bei Kotlin sind es keine Anweisungen sondern Ausdrücke.
Sie können rechts vom Gleichheitszeichen stehen und damit direkt einer variable zugewiesen werden.

11) Was ist ein ENUM? 

Ein Enum ist ein Datentyp, der die Werte von vordefinierten Konstanten annehmen kann.

12) Erklären Sie Domain-Driven-Design anhand eines Beispiels!

DDD ist ein Modellierungskonzept bei dem sich die technische Umsetzung an den Geschäftsvorfällen orientiert.
So wird z.B. ein Kunde mit seinen zugehörigen Funktionen wie z.B. Änderungen der Stammdaten oder aktualisieren des Umsatzes abgebildet.
Dafür werden alle benötigten Properties und Funktionen eines Kunden erstellt aber ohne dabei einen anderen Geschäftsvorfall zu beinhalten wie z.B. die Bestellungen.

13) Was könnten Ursachen für die Entstehung von Big Data sein und was könnte zu Problemen beim
Monolithen führen? 

Ursachen sind ein breites Spektrum an gesammelten Daten oder eine häufige Frequenz der Daten wie z.B. bei IoT.
Monolithen haben dabei Probleme, da sie die Datenmenge und Daten

14) Warum sollten .yml-Dateien (YAML) für Konfiguration benutzt werden (Vorteil)? 

Die Vorteile sind eine Portabilität zwischen versch. Programmiersprachen, besser lesbar und bietet mächtige Ausdrucksmöglichkeiten.

15) Welche Nachteile haben .yml-Dateien? 



16) Was ist Backpressure? 

Backpressure ist eine Überlast an Requests, mit der der Server umgehen muss.
Dabei aboniert der Subscriber nur zu einer gewissen Obergrenze und der Publisher produziert nur bis zu gewisser Obergrenze.
Alle weiteren Requests werden an einen anderen Server weitergeleitet oder werden nicht vom Server angenommen.

18) Beschreiben Sie 3 Vorteile, die IntelliJ IDEA im Vergleich mit Editoren, wie Notepad++ hat? 

Refactoring um Klassennamen nachträglich zu ändern. Die Codenavigation erlaubt das schnelle navigieren und lesen im Code.
Autovervollständigung um Tippfehler zu vermeiden

19) Vorteile von IntelliJ - IDE?

siehe 18

20) Was sind “one-way-functions” ?

Damit sind injektive funktionen gemeint, die ein effizientes Verfahren für die Bestimmung des Funktionsergebnisses haben aber deren Umkehrung praktisch unmöglich ist. 

21) Erklären Sie nicht-blockierende Verarbeitung! 

Damitist geminet, dass ein Thread während er eine andere Komponente aufruft nicht blockiert ist sondern während der Wartezeit andere Anweisungen ausführt.

22) Warum sollte asynchron statt imperativ programmiert werden? 

Um das Blockieren von Threads und z.B. das C10K Problem zu vermeiden sollte asynchron programmiert werden.

23) Erläutern Sie, warum nicht jede Server-Anwendung „reactive“ entwickelt wird! - KlausurFrage 

Es gibt immernoch genug anwendungsfälle, in den imperative Programmierung keine Skalierungsprobleme verursacht.

(reactive ist aufwendiger zu programmieren und lohnt sich durch das aufwendigere Trheadmanagement ab einer gewissen Menge an Requests)

24) Erläutern Sie Probleme bei Reactive Programming!* - KlausurFrage 

Sobald eine Komponente Blockierend ist, ist alles sinnlos.
Es ist aufwendiger zu programmieren.
Der Stacktrace des Eventloops ist nicht hilfreich um die Abarbeitung eines Requests nachzuverfolgen.

25) Erklären Sie was ein Stacktrace ist.- Klausur-Frage 

Ein stacktrace ist das Auslesen und darstellen des Callstacks eines Threads. Er wird verwendet um im Fall eines Fehlers nachzuverfolgen, wo der Fehler aufgetreten ist.

26) Vergleichen Sie Boundary Control Entity & Schichtenarchitektur? 

Der Zugriff erfolgt bei BCE durch das Boundry Objekt, während es in der 3 Schichten über die Präsentationsschicht erfolgt.
Der Controller bei

27) Wann ist es sinnvoll, den Cache in die Anwendungslogik zu implementieren? 

28) Erklären Sie die 4 Eigenschaften des Reactive Manifesto (MRRE)! 

Message driven Server verarbeiten eigehende Nachrichten bzw. requests.
Die skalierbarkeit ist elastisch, indem die Anzahl der verfügbaren Servcer entsprechend geändert wird
Resilient der Server ist wiederstandsfähig, so wird bei Überlast ein Loadsheading oder ein weiterleiten der Requests in eine Region mit weniger Auslastung gemacht.
Responsive, d.h. eine Antwortzeit in Millisekunden.

29) Grenzen Sie Funktionen, Methoden und Prozeduren voneinander ab! 

Funktionen haben einen Rückgabewert.
Methoden sind Funktionen einer Klasse.
Prozeduren haben keine Rückgabewert.

30) Was macht die Funktion findById() in der Handler Klasse? 

Sie ruft auf dem injezierten KundeService objekt die entsprechende funktion auf, überprüft das Ergebnis mit Hilfe von sealed classes und gibt je nach Ergebnise den gebauten Response zurück.

33) Erklären Sie den Unterschied zwischen Flow und List in Kotlin! 

List ist ein Synchron befüllter Datenbehälter während Flow ein asynchroner Datenbehälter ist, in dem zu einem späteren Zeitpunkt 0 bis n Elemente enthalten sein können.

35) Was ist der Unterschied zwischen einer Menge/Set und einer Liste? 

Liste hat eine Reihenfolge, eine Menge nicht.
In eienr MEnge dürfen Elemente nicht doppelt vorkommen, im Gegensatz zu eienr Liste.

36) Was ist der Unterschied zwischen Mutablelist und Flow? 

ein Flow ist ein Asynchroner Datenbehälter, der nicht beliebig modifiziert werden kann.
Die Mutable List ist ein Datenbehälter, der synchron ist und beliebig geändert werden.

37) Warum ist es sinnvoll, BigDecimal und nicht float/double zu verwenden? 

Um Rundungsfehler zu vermeiden.

38) Erklären Sie den Zusammenhang von ETags & If-None-Match bei einem GET-Request & einem wiederholten
GET-Request! 

Bei einem Get-Request wird vom Server ein ETag mit übertragen. Das Etag kann dafür verwendet bei einem späteren Get-Request abzufragen, ob neuere Daten vorhanden sind, oder ob der vorhandene Datensatz weiter verwendet werden kann.
Ein Get Request mit einem Etag und If-None-Match wird nur durchgeführt, wenn die mitgeschickte Versionsnummer nicht der Versionsnummer des Servers übereinstimmt, es also eine aktueller Version des Datensatzes gibt.

39) Erklären Sie ETags! 

Etags entsprechen der Versionsnummer eines Datensatzes. Sie wird vom DB-System vergeben und automatisch gepfelgt.

40) Was ist ein bedingter GET-Request? bedingt→ if 

Ein bedingter Get-Request wird nur unter eines Bedingung wie z.B. eine ungleiche Versionsnummer ausgeführt.

41) Wie viele verschiedene Kombinationen gibt es bei 4 Checkboxen? - Klausurfrage 

JEde Checkbox hat 2 Zustände, deswegen gibt es 2^4 Möglichkeiten. Also sind es 16 Möglichkeiten.

42) Unterschied Forward- und Reverse-Proxy? 

Der Forward Proxy Leitet bündelt und Verarbeitet den Internet Traffik aller Darunter liegenden Netzwerkteilnehmer.
Der Reverseproxy Nimmt Stellvertretend für darunterliegende Netzwerkteilnehmer Anfragen entgegen und leitet sie entsprechend an die Teilnehmer weiter.

43) Was sind Servlets und wie werden diese verwaltet? 

Servlets sind Java Klassen, deren instanzen in einem Webserver Anfragen entgegennehmen. Sie werden vom Webserver verwaltet.

44) Erklären Sie die Aussage „Make JAR, not WAR“! - swe schauen 

Wir sollen JAR archieve bauben, da diese einen Embedded Web Container beinhalten, der beim ausführen mit gestartet wird.
WAR müssen in einen bereits laufenden Web Container geladen werden und von einem Administrator konfiguriert werden.

45) Erläutern Sie, was durch den Produktnamen „Spring Boot“ ausgedrückt werden soll. 

Es handelt sich um ein Produkt, dass beim Starten einer Spring anwendung helfen soll.

46) Was ist ein Web-Container? 

Laufzeitumgebung für Servlets.

47) Was macht ein embedded Web-Container? 

Ein Webcontainer der im Contaienr integriert ist und beim Deployment mit gestarted wird

48) Was ist Netty? 

49) Unterschied Tomcat und Netty? 

NEtty ist leichtgewichtiger als Tomcat.

51) Wieso werden Microservices als Anwendungsdatenbank bezeichnet? 

Jeder microservice ist in sich abgeschlossen und verfügt damit über eine Instanz der dazugehörigen Daten in einer Datenbank.

52) Was sind Microservices? 

Ein Microservcie ist ein Boudned Context der einen Geschäfsvorfall abbildet.

54) Was sind die Prinzipien von REST? 

Das Prinzip von REST ist ein Architekturstil für die Verwaltung von REssourcen, die mit URIs zugänglichgemacht werde, unter der Verwendung von Standards wie z.B. JSON und HTTP aber auch URIs.

55) Nennen Sie 2 MIME-Typen, die bei Microservices häufig verwendet werden! 

application/json
text/plain

56) Erklären Sie IAM anhand von Social Logins! 

Unter IAM versteht man Identity Access Management, damit werden die Berechtigungen anhand der authentifizierung durch Social Logins verwaltet.
Durch Sozial Logins können konten von anderen Platformen für die Anemldung verwendet werden.

57) Was ist der Unterschied zwischen IAM und IDM? 

IAM ist die authorisierung von Benutzern während IDM die authentifizierung von Bneutzern ist.

58) Erklären Sie die Annotation @Bean! 

@Bean annotiert eine Funktion. Die Funktionen die mit @Bean annotiert sind liefern Objekte, die später zur
Laufzeit benötigt werden und die zur Laufzeit vom Spring-Container bereitgestellt werden, an den Stellen wo diese
Objekte benötigt werden. 

59) Erklären Sie den Unterschied zwischen @Bean & @Configuration 

Eine mit @Configuration annotierte Klasse enthält mindestens eine Funktion, die mit @Bean annotiert ist. 

60) Was macht die Annotation @Version? 

Damit wird gekennzeichnet, dass es sich um die Property der Versionsnummer eienr Klasse handelt. Dadurch wird die Versionsnummer von SpringData MongoDB gepflegt.

61) Erläutern Sie, warum man bei Kotlin-Property, die mit @Version annotiert ist, auch die Annotation @JsonIgnore
verwendet wird. 

Der Client benötigt die Versionsnummer das Datensatzes nicht. Deswegen muss sie nicht von Jackson zu einem Json Objekt hinzugefügt werden.

62) Wieso wird die Annotation @JsonIgnore bei Versionsnummern verwendet? 

63) Wie ist das Hauptprogramm eines Microservices annotiert? 

@SpringBootApplication

64) Was besagt Annotation @Component? 

Sie registriert die Klasse bei Spring, damit sie für Dependency Injections zur Verfügung steht.

65) Pfad/Query-Parameter, was wird wann genutzt? 

Pfad Params wenn es eine möglichst kurze URI sein soll.
Query PArametern, wenn es nicht lesbar, reihnenfolgen unabhängig und z.B. bei Auswahlkriterien.

67) Erklären Sie Singletons anhand eines Beispiels! 

Ein Singelton ist eine Klasse von der es nur eine Instanz gibt.
Der KundeService ist z.B. ein Singleton, da er Zustandslos ist und deswegen nur eine Instanz benötigt wird.

68) Was bedeutet Annotation @Service? 

Es handelt sich um einen Spezialfall von @Component, der eine Serviceklasse markiert.

71) Was bedeutet Annotation @JsonPropertyOrder? 

Damit wird Jackson mitgeteilt, in welcher Reihenfolge die Propertys einer Klasse strukturiert sind.    

72) Wie heißen Annotationen in C#? 

Annotationen

# Kotlin 

73) Was sind die Ziele von Kotlin? 

Leicht lesbaren, effizienten, wenig fehleranfälligen Code zu schreiben, der mit Java packages kompartibel ist und mit vielen Entwicklungsumgebungen kompatiebel ist.

74) Nennen sie 4 Vorteile von Kotlin? 

Typen sind Nullsafe, es werden Properties statt get und set genutzt, Higher-order-Functions mit Labdaausdrücken und funktionaler Programmierung, Named PArameter statt builder pattern 

75) Nenne 4 typische Anfängerfehler in der Entwicklung? 

Warnings ingoriert,
ungleichmäßig eingerückt,
Test vernachläsigt,
keine Dokumentation

76) Wie erstellt man ein „immutable“ Objekt in Kotlin? 

Objekte sind standardmäßig immutable in Kotlin

77) Wie erstellt man ein „immutable“ Property in Kotlin? 

Propertys sind standardmäßig immutable

78) Erklären Sie die Funktionsweise von „Extension functions“ bei Kotlin?

Eine Extension Function ist die nachträgliche Erweiterung einer Klasse um zusätzliche Funktionalität.

79) Wie wird die Funktionalität von Extension Functions (Kotlin) in C# realisiert?

Durch extension methods.

80) Wie lautet die Reihenfolge der Variablendeklaration? 



81) Was ist eine Higher-Order Function? – KlausurFrage

Eine Funktion, der eine Funktion als PAramter übergeben wird und deren Rückgabetpy eine Funktion ist.

82) Wieso braucht man Lambda-Ausdrücke in Higher-Order Functions?

Ein Labda ausdruck hat eine Funktion als eingabe pder rückgabewert und führt darauf Operationen aus.

83) Was sind pure functions? – phase6 15

Damit sind funktionen gemeint, die keine Seiteneffekte haben und bei selber Eingabe immer das selbe Ergebnis liefern.

84) Erklären Sie eine Single Expression Function anhand eines Beispiels! - KlausurFrage 

fun toString() = "Kunde id=$id"

85) Erklären Sie Syntax & Semantik des folgenden Codefragments: 

86) Erklären Sie die Semantik der folgenden Codezeilen: 

87) Nennen Sie 4 Aspekte guter Codequalität -phase6 

Kommentare wo sie benötigt werden.
Einheitliche Formatierung
Sinnvoll gewählt Namen
Ordentliche Verzeichnisstrucktur.

88) Was ist Type Aliases? 

Damit ist das Vergeben eines anderen Names für einen Typen gemeint. Der neue Name kann dann an Stelle des Typen verwendet werden.

89) Was macht die Funktion retrieve()? 

90) Was macht die Funktion runBlocking{}?

91) Wie geht Kotlin mit null-Status um?* - Klausur-Frage 

In Kotlin kann der Wert null standardmäßig nicht angenommen werden, außer es wird anders konfiguriert.

92) Erklären Sie den Safe Call Operator? 

Der Safe Call Operator führt zuerst eine Überprüfung durch, ob der Wert null gesetzt ist befor eine Weitere Operation durchgeführt wird. 

93) Erläutern Sie, wie man in Kotlin anders als in C# programmieren kann, weil es if-Ausdrücke gibt. 

Der If Ausdruck kann rechts vom Gleichheitszeichen stehen.

94) Erläutern Sie, warum suspendierbare Funktionen von Kotlin besser sind um„reactive“ zu programmieren. -
KlausurFrage 

Sie können unterbrochen und zu einem späteren Zeitpunkt fortgesetzt werden, sofern dies für nötig erachtet wird.

95) Was ist eine SAM? 

Ein funktionales interface mit genau einer MEthdoe

96) Was ist ein Companion Object? 

ein Singleton, das zu einer Klasse gehört.

97) Was ist eine Kotlin Coroutine? 

leichtgewichtige Benutzer level Threads, die in Kotlin für die nicht blockierende Verarbeitung genutzt werden.

98) Erläutern Sie, wie man prinzipiell “Sealed Classes“ statt Exception zur Fehlerb.?- Klausur-Fragen 

Wird zu Zentralisierung der Fehlerbehandlung gemacht indem man die Klassen für Fehlerfälle und Erfolgsfälle verwendet statt try catch.

# Grundlegende Konzepte heutiger Softwareentwicklung 

99) Was sind die grundlegenden Konzepte heutiger Softwareentwicklung? 

Es werden die Grundsätze Convention over Configuration und Configuration by Excception verwendet.
Ebenfalls ist die Verwendung von Dependency Injection und funktionaler Programmierung ein grundlesgendes Konzept.
Auch die Verkettung von Funktionsaufrufen unter Verwendung des Builder Patterns.

100) Was ist eine Dependency Injection (DI) anhand eines Beispiels in ihrem Projekt? 

class KontaktHandler (private val: KontaktService) {...}
Mit der Dependency Injektion wird ein Objekt der Klasse KontaktService instanziert um darauf die entsprechenden Funktionen aufzurufen.

101) Was bedeutet Inversion of Control (IoC)? 

Mit Inversion of Controll ist das Abgeben der Kontrolle an eine Platform wie z.B. Spring gemeint.

102) Warum sollte Dependency Injection, die Constructor Injection und nicht die Field Injection nutzen? 

Sie sollte genutzt werden, da die Abhängigkeiten im Konstrukter erkennbar sind. Zudem ist keine Endlosrekursion wie bei der Field Injektion möglich.

102) Was bedeutet Convention over Configuration (CoC)? 

Das Verwenden von sinnvoll gewählten Standardverwerten anstatt alles selbst zu konfigurieren.

103) Erklären Sie Convention over Configuration (CoC) am Beispiel von JSON und Kotlin Objekten! 

So wird z.B. von Jackson das gesammt Kotlin Objekt übersetzt außer es wird von uns anders konfiguriert.

105) Wann verwendet man Jackson? 

Wenn man Kotlin Objekte zu Json umwandelt und andersrum.

106) Was versteht man unter dem Builder Pattern + Bsp im eigenen Projekt?

Unter dem Buildpattern versteht man eine Verkettung von Funtkionsaufrufen. 
So z.B. im Kundehandler.

return ok().bodyValueAndAwait(Kontakt)

107) Wieso sind Named Parameters besser als das Builder Pattern? 

Es müssen weniger anweisungen gelesen und interpretiert werden.
Es ist reihenfolgenunabhängig.

108) Erklären Sie das LIFT-Prinzip! 

Es Besagt, dass das finden unseres Codes einfach ist.
Zudem soll unser Code leicht Identifizierbar sein und solange möglich niedrige ORdnerstrukturen verwendet werden sollen.
Außerdemm sollen wiederholungen in usnerem Code vermieden werden.

## Statuscodes 

109) Welche Statuscodes kommen bei einem fehlgeschlagenen POST Request bzw. PUT-Request zurück? 

400 Bad Resuest oder 500 bei einem internen Server fehler.

110) Was geben die Statuscodes 200,201, 204 zurück. Nenne auch die aufgerufene HTTP-Methoden. -phase6 

200 stellt den Status ok dar und kommt bei der HTTP Methode GET.
201 stellt den Status created dar und kommt bei der HTTP Methode Post.
204 stellt den Status keine Änderrung dar und kann bei der HTTP-MEthode PUT oder PATCH vorkommen. 

111) Erklären Sie das Zusammenspiel von Client und Server! 
Authentifizierungsverfahren 

112) Nenne 2 Authentifizierungsverfahren bei RESTful Webservices! 

Zwei Authentifizierungsverfahren sind z.B. Basic und Token.

113) Wieso ist es bei verteilten Systemen mit Microservices problematisch BASIC-Authentifizierung zu
verwenden? 

Es ist problematisch, da bei jedem Request Benutzername und PAsswort mitgeschickt werden müssten.

114) Wie funktioniert Token? 

In einem Token sind Informationen enthalten wie z.B. ein Schlüssel der den Benutzer Identifiziert und due Dauer, wie lange diese Identifikation gültig ist.
Es muss nur einmal der Benutzername und das Passwort mitgeschickt werden um ein Token zu erhalten, dass für künfigte Authorisierung und Authentifizierung verwendet wird.


# HATEOAS 

117) Erläutern Sie HATEOAS mit Beispielen von Unternehmen wie PayPal, Facebook, …! 

Bei HATEOS wird die API durch selbsterklärende Links im Response des Servers beschrieben. Bei Facebook kommt durch die Links beim Abfragen eines Benutzers  dadurch z.B. auf das Profil eines Benutzers, oder seine Pinnwand.

118) Erklären Sie den Unterschied zwischen Atom-Links & Link-Header! 

Bei Atom-Links befinden sich die Links zur beschreibung der API im Response-Body, während sie bei Header Links im Response-Header sind.

119) Erkläre Unterschied zwischen URI und URL! 

Die URL ist eine Teilgruppe der URI, bei der noch das Zugriffsprotokoll angegeben ist z.B. "HTTPS://" ...

120) Was ist der Unterschied zwischen Structural Links & Transitional Links? 
Datenbankzugriff und Spring Data (MongoDB) 



121) Was heißt eventually consistent? 

In einem verteilten System sind Datenbanken nicht immer auf dem aktuellesten Stand der Daten. Eventually konsisten bedeuted, dass sie sich zu einem späteren Zeitpunkt gegenseitig aktuallisieren.

122) Erklären Sie die Funktionsweise bei optimistischen DB-Transaktionen!

Bei optimistischen Transaktionen wird ein zu ändernder Datensatz nicht blockiert. Es wird jedoch vor dem Durchführen der Änderrung durch ein erneuten Request des Datensatzes überprüft, ob der Datensatz mittlerweile eine andere Versionsnummer erhalten hat. Wenn das der Fall ist, wird die Änderrung nicht durchgeführt, sonst wird sie durchgeführt.

123) Wieso ist es bei verteilten Systemen sinnvoll keine pessimistische Synchronisation zu verwenden? 

Es ist nicht sinnvoll, da bei der pessimistischen Synchronisation die Datenbanken für den Zeitraum der aktualisierung blockiert werden müssen. 
In verteilten Systemen ist diese Operation sehr schwierig. 

124) Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Änderung: Update - Update 

Die ersten Änderungen das Datensatzes werden rückgängig gemacht und nur die Änderungen des zweiten Requests werden übernommen.

125) Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als die eigene Änderung: Update - Delete 

Der Datensatz wird mit den Änderungen neu angelegt.

126) Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Löschen: Delete - Update 

Der Datensatz wird mit den vorherigen Änderungen gelöscht.

127) Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als das eigene Löschen. Delete - Delete 

Es kommt evtl. eine Fehlermeldung oder es passiert nichts.

128) Wie beschreibt man Abhängigkeiten in SQL bzw. MongoDB? 

Bei Mongo DB Durch Embedded Documents, bei SQL durch Relationen und Fremdschlüssel.

129) Nennen Sie zu Collection, Document & Embedded Document, die dazugehörigen Gegenstücke in
relationalen DB-Systemen. 

Collection: Tabelle
Document: Datensatz
Embedded Document: Relation bzw. Fremdschlüssel

130) Unterschiede von MongoDB & relationaler DB? 

relational vs Dokument orientiert.


131) Was ist das Schema bei relationalen Datenbanken? 

Create Table bzw. die Vorgabe einer Datensatzstruktur

132) Erklären Sie die Unterschiede zwischen relational und objektorientiert! 

relational werden Beziehungen durch FK und Relationen gebildet. Der Datensatz liegt an mehreren Stellen verteilt und muss evtl. über ein join der Tabellen gebaut werden.
Bei Objektorientierten Datensätzen befindet sich alles als ein Objekt mit Unterobjekten in der Datenbank und kann ohne joins ausgelesen werden.

133) 3 Unterschiede zwischen REST und DDD? 

DDD REST
ID URI
Version Etag
Relation Link

134) Wie werden Beziehungen in rel. DB, JSON Documents & Kotlin Objekten realisiert? 

rel: Foreign Key und Relation
Json: Embedded Document
Kotlin: Packages

135) Wann benutzt man ReactiveCrudRepository & wann ReactiveMongoOperations? 

Reactive Crud bei dem Arbeiten mit relationenalen DB und ReactiveMongoOperations beim Arbeiten mit mongoDB.

137) Vergleichen Sie die Abfrage einer relationalen DB mit der Abfrage in MongoDB! 

138) Erklären Sie 2 Pattern aus DDD, die bei Spring Data ähnlich verwendet werden? 

139) Beschreiben Sie die 4 Stores von NoSQL-Systemen! 

Document Speichert Dokumente im JSON format in BSON
Column Spezialisiert auf sehr viele Spalten
Key Value Spezialisiert auf des Speichern von KEy Value pairs
Graph durch das Speichern von Knoten

140) Warum sollte MongoDB und nicht relationale DB genutzt werden? 

Da MongoDB ansynchron ist, eine mächtige Query-Syntax hat und hoch skalierbar ist

141) Was ist umständlich an MongoDB? 

Keine Sprache wie SQL
Joins sind umständlich. 

142) Wieso werden Transaktionen bei MongoDB nicht wirklich benötigt. 

Da wir nur ein Dokument bearbeiten müssen und nicht mehrere gleichzeitig.

143) Beschreiben Sie, wann man bei MongoDB bei einem Schreibvorgang keine explizite Transaktion benötigt! 

Es wird keine Transaktion beötigt, da einfach ein kompletter Datensatz hinzugefügt wird.

144) Beschreiben Sie, wie man sinnvollerweise interaktiv inspiziert, ob Daten in MongoDB auch wirklich
eingefügt oder aktualisiert wurden. 

z.B. durch einen Browser wie MongoDBCompass

145) Beschreiben Sie, was man unter „Type-Safe Queries“ versteht. 

unter Type-Safe-Queries versteht man das Abfragen untder der Verwendung von Objekten statt strings.

146) Beschreiben Sie eine Möglichkeit, wie man in einem Spring Profile z.B. „dev“, prinzipiell die Testdaten in der
DB zurücksetzen kann.

Beim Start der Anwendung kann überprüft werden, welches Profil aktiv ist. Spring kann so konfiguriert werden, dass z.B. beim Profil "Dev" alle Collections der Datenbank gelöscht und neu mit Testdaten erstellt werden.

# Tests 

147) Was bedeutet „just Runs“ in der Syntax? 

148) Was macht Mocking? 

Es simuliert einen Bestandteil einer Anwendung wie z.B. einen Datenbankzugriff und gibt eine Antwort zurück wie es der Datenbankzugriff machen würde.

148) Was macht Funktion „every“? 



149) Was macht die Annotation @Nested? 

Damit wird die Schachtellung von Tests für eine übersichtliche Struktur markiert.

150) Was macht die Annotation @Order und warum steht in den Klammern von @Order eine 1000? 

Sie besagt, in welcher Reihenfolge die Tests ausgeführt werden sollen. Die Zahl in den Klammern gibt die Position in der Reihenfolge an.

151) Was macht die Annotation @Disabled? 

Sie markiert einen Test, der nicht ausgeführt werden soll.

152) Warum und wann sollte getestet werden? 

Es sollte getestet werden, da sonst der Endanwender der Tester ist und damit fehler in der Software entdeckt.
Es sollte bei jedem Commit und vor jeden Release getestet werden.

153) Wofür steht die Annotation @CsvSource? 

Um einen Test mit Parametern, die im CSV-Format bereitgestellt werden.

154) Nach welcher Funktionalität sollten Testklassen aufgebaut sein orientieren sie sich an CRUD? 



155) Nenne die bekanntesten Testarten und beschreibe Sie! 

Mit Modultests werden kleine Funktionalitäten bzw. Komponenten unserer Software getestet.
Integrationstest testen die Integration der Komponenten.
Bei End-to-End (E2E) also Ende zu Ende Tests wird vom Frontend die gesammte Anwendung getestet. 

158) Erklären Sie AAA bei Unit-Tests! 

Bei Unit Tests werden zuerst Testdaten bereit gestellt. Dieser Abschnitt wird als Arrage bezeichnet.
Im zweiten Abschnitt, wird der eigentliche Test durchgeführt. Er wird mit Act bezeichnet, da etwas durchgeführt wird.
Zuletzt werden die Soll- und Ist-Ergebnisse verglichen im sog. Assert block. 

160) Warum kann man bei der Testentwicklung in Kotlin von Specificationlike Test sprechen? 

Da wir am Namen der Funktion ablesen können, was getestet wird.

161) Was versteht man unter SoftAssertion 

Dadurch stürzt beim Überprüfen der Testergebnisse die Ausführung nicht ab, falls Null Wert mit einem Wert verglichen wird.

162) Was ermöglicht uns Kotest? 

## Scurity 

163) Was ist der Unterschied zwischen Authentifizierung und Autorisierung? 

Authentifizierung ist das überprüfen der Identität z.B. Login.
Authorisierung ist das Validieren der Berechtigung für den Zugriff auf eine Ressource.

164) Was macht die Annotation @PreAuthorize(„hasRole(‚Rolle‘)“)? 

Dadurch wird vor dem Funktionsaufruf überprüft, dass der Benutzer der benötigten Rolle zugeordnet ist.

165) Was ist der Unterschied zwischen einer Rolle und einer Gruppe? 

Eine Rolle ist eine Sammlung von Berechtigungen. Eine Gruppe ist eine Sammlung von Benutzern.

166) Erkläre die Abkürzung SSO! 

Mit Single-Sign-On (SSO) ist gemeint, dass sich der Benutzer nur einmal anmeldet und dadurch auch bei anderen Microservices in unserem Cluster angemeldet ist.

# Logging 

167) Welche Log-Level gibt es und für wen sind diese interessant ? 

INFO allgemein/ Administratoren
WARN Entwickler/ Administratoren
TRACE Entwickler
DEBUG Entwickler
FATAL Entwickler
ERROR Entwickler/ Administratoren

169) Warum {} besser als () ist, erklären Sie anhand diesem Codebeispiel? 
Apache Log4j2 kann Lazy Logging ? 

Es ist besser, da das Objekt erst gebaut wird, wenn es benötigt wird.

170) Beschreiben Sie eine Log-datei? 

JEde Zeile ist ein Eintrag. Zu Beginn der Zeile steht ein Zeitstempel, danach das Logleven gefolgt von der Prozess ID und Zuletzt der Inhalt der Nachricht.

171) Warum ist Trailing Comma ein tolles Feature? 

172) Erklären Sie die Impedance Mismatch? 

Damit ist gemeint, dass es bei der Umwandlung von Objektorientierter Darstellung zu Relationaler Darstellung von Objekten nicht Problemlos funktioniert. Eine N zu M beziehung muss mit Hilfe einer weiteren Tabelle dargestellt werden.

173) Beschreiben Sie die 4 Interfaces in Reactive Streams? 

???
Publisher Subscriber
Consumer Producer

## Codebeispiele 

174) Wo ist hier der Denkfehler im Codefragment ? 

175) Schreiben Sie den nachfolgenden Code so um, das Lambda-Ausdrücke verwendet werden. 

176) Schreiben Sie folgenden Code mit Lambda Ausdrücken. 

177) Was ist an folgendem Code schlecht? 

178) Beschreiben Sie den Code nach der Syntax (Code-Fragment wurde vorgegeben von Router Function) 

179) Beschreiben Sie folgendes Codebeispiel nach der Semantik