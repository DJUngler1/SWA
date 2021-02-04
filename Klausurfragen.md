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
* YAML ist leichtgewichter, leichter lessbar, und mächtiger als z.B XML.
1)  Welche Nachteile haben .yml-Dateien? 

2)  Was ist Backpressure? 

3)  Beschreiben Sie 3 Vorteile, die IntelliJ IDEA im Vergleich mit Editoren, wie Notepad++ hat? 

4)  Vorteile von IntelliJ - IDE?

5)  Was sind “one-way-functions” ? 

6)  Erklären Sie nicht-blockierende Verarbeitung! 

7)  Warum sollte asynchron statt imperativ programmiert werden? 

8)  Erläutern Sie, warum nicht jede Server-Anwendung „reactive“ entwickelt wird! - KlausurFrage 

9)  Erläutern Sie Probleme bei Reactive Programming!* - KlausurFrage 

10) Erklären Sie was ein Stacktrace ist.- Klausur-Frage 

11) Vergleichen Sie Boundary Control Entity & Schichtenarchitektur? 

12) Wann ist es sinnvoll, den Cache in die Anwendungslogik zu implementieren? 

13) Erklären Sie die 4 Eigenschaften des Reactive Manifesto (MRRE)! 

14) Grenzen Sie Funktionen, Methoden und Prozeduren voneinander ab! 

15) Was macht die Funktion findById() in der Handler Klasse? 

16) Erklären Sie den Unterschied zwischen Flow und List in Kotlin! 

17) Was ist der Unterschied zwischen einer Menge/Set und einer Liste? 

18) Was ist der Unterschied zwischen Mutablelist und Flow? 

19) Warum ist es sinnvoll, BigDecimal und nicht float/double zu verwenden? 

20) Erklären Sie den Zusammenhang von ETags & If-None-Match bei einem GET-Request & einem wiederholten
GET-Request! 

39) Erklären Sie ETags! 

40) Was ist ein bedingter GET-Request? bedingt→ if 

41) Wie viele verschiedene Kombinationen gibt es bei 4 Checkboxen? - Klausurfrage 

42) Unterschied Forward- und Reverse-Proxy? 

43) Was sind Servlets und wie werden diese verwaltet? 

44) Erklären Sie die Aussage „Make JAR, not WAR“! - swe schauen 

45) Erläutern Sie, was durch den Produktnamen „Spring Boot“ ausgedrückt werden soll. 

46) Was ist ein Web-Container? 

47) Was macht ein embedded Web-Container? 

48) Was ist Netty? 

49) Unterschied Tomcat und Netty? 

51) Wieso werden Microservices als Anwendungsdatenbank bezeichnet? 

52) Was sind Microservices? 

54) Was sind die Prinzipien von REST? 

55) Nennen Sie 2 MIME-Typen, die bei Microservices häufig verwendet werden! 

56) Erklären Sie IAM anhand von Social Logins! 

57) Was ist der Unterschied zwischen IAM und IDM? 

58) Erklären Sie die Annotation @Bean! 
@Bean annotiert eine Funktion. Die Funktionen die mit @Bean annotiert sind liefern Objekte, die später zur
Laufzeit benötigt werden und die zur Laufzeit vom Spring-Container bereitgestellt werden, an den Stellen wo diese
Objekte benötigt werden. 

59) Erklären Sie den Unterschied zwischen @Bean & @Configuration 

60) Was macht die Annotation @Version? 

61) Erläutern Sie, warum man bei Kotlin-Property, die mit @Version annotiert ist, auch die Annotation @JsonIgnore
verwendet wird. 

62) Wieso wird die Annotation @JsonIgnore bei Versionsnummern verwendet? 

63) Wie ist das Hauptprogramm eines Microservices annotiert? 

64) Was besagt Annotation @Component? 

65) Pfad/Query-Parameter, was wird wann genutzt? 

67) Erklären Sie Singletons anhand eines Beispiels! 

68) Was bedeutet Annotation @Service? 

71) Was bedeutet Annotation @JsonPropertyOrder? 

72) Wie heißen Annotationen in C#? 

# Kotlin 

73) Was sind die Ziele von Kotlin? 

74) Nennen sie 4 Vorteile von Kotlin? 

75) Nenne 4 typische Anfängerfehler in der Entwicklung? 

76) Wie erstellt man ein „immutable“ Objekt in Kotlin? 

77) Wie erstellt man ein „immutable“ Property in Kotlin? 

78) Erklären Sie die Funktionsweise von „Extension functions“ bei Kotlin?

79) Wie wird die Funktionalität von Extension Functions (Kotlin) in C# realisiert?

80) Wie lautet die Reihenfolge der Variablendeklaration? 

81) Was ist eine Higher-Order Function? – KlausurFrage

82) Wieso braucht man Lambda-Ausdrücke in Higher-Order Functions?

83) Was sind pure functions? – phase6 15

84) Erklären Sie eine Single Expression Function anhand eines Beispiels! - KlausurFrage 

85) Erklären Sie Syntax & Semantik des folgenden Codefragments: 

86) Erklären Sie die Semantik der folgenden Codezeilen: 

87) Nennen Sie 4 Aspekte guter Codequalität -phase6 

88) Was ist Type Aliases? 

89) Was macht die Funktion retrieve()? 

90) Was macht die Funktion runBlocking{}?

91) Wie geht Kotlin mit null-Status um?* - Klausur-Frage 

92) Erklären Sie den Safe Call Operator? 

93) Erläutern Sie, wie man in Kotlin anders als in C# programmieren kann, weil es if-Ausdrücke gibt. 

94) Erläutern Sie, warum suspendierbare Funktionen von Kotlin besser sind um„reactive“ zu programmieren. -
KlausurFrage 

95) Was ist eine SAM? 

96) Was ist ein Companion Object? 

97) Was ist eine Kotlin Coroutine? 

98) Erläutern Sie, wie man prinzipiell “Sealed Classes“ statt Exception zur Fehlerb.?- Klausur-Fragen 

# Grundlegende Konzepte heutiger Softwareentwicklung 

99) Was sind die grundlegenden Konzepte heutiger Softwareentwicklung? 

100) Was ist eine Dependency Injection (DI) anhand eines Beispiels in ihrem Projekt? 

101) Was bedeutet Inversion of Control (IoC)? 

102) Warum sollte Dependency Injection, die Constructor Injection und nicht die Field Injection nutzen? 

102) Was bedeutet Convention over Configuration (CoC)? 

103) Erklären Sie Convention over Configuration (CoC) am Beispiel von JSON und Kotlin Objekten! 

105) Wann verwendet man Jackson? 

106) Was versteht man unter dem Builder Pattern + Bsp im eigenen Projekt?

107) Wieso sind Named Parameters besser als das Builder Pattern? 

108) Erklären Sie das LIFT-Prinzip! 
Statuscodes 

109) Welche Statuscodes kommen bei einem fehlgeschlagenen POST Request bzw. PUT-Request zurück? 

110) Was geben die Statuscodes 200,201, 204 zurück. Nenne auch die aufgerufene HTTP-Methoden. -phase6 

111) Erklären Sie das Zusammenspiel von Client und Server! 
Authentifizierungsverfahren 

112) Nenne 2 Authentifizierungsverfahren bei RESTful Webservices! 

113) Wieso ist es bei verteilten Systemen mit Microservices problematisch BASIC-Authentifizierung zu
verwenden? 

114) Wie funktioniert Token?
     
# HATEOAS 

1)   Erläutern Sie HATEOAS mit Beispielen von Unternehmen wie PayPal, Facebook, …! 

2)   Erklären Sie den Unterschied zwischen Atom-Links & Link-Header! 

3)   Erkläre Unterschied zwischen URI und URL! 

4)   Was ist der Unterschied zwischen Structural Links & Transitional Links? 
Datenbankzugriff und Spring Data (MongoDB) 

1)   Was heißt eventually consistent? 

2)   Erklären Sie die Funktionsweise bei optimistischen DB-Transaktionen!

3)   Wieso ist es bei verteilten Systemen sinnvoll keine pessimistische Synchronisation zu verwenden? 

4)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Änderung: Update - Update 

1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als die eigene Änderung: Update - Delete 

1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und eine
konkurrierende Änderung schneller erfolgt als die eigene Löschen: Delete - Update 

1)   Erläutern Sie, was passiert, wenn auf optimistische Synchronisation verzichtet wird und ein konkurrierendes
Löschen schneller erfolgt als das eigene Löschen. Delete - Delete 

1)   Wie beschreibt man Abhängigkeiten in SQL bzw. MongoDB? 

2)   Nennen Sie zu Collection, Document & Embedded Document, die dazugehörigen Gegenstücke in
relationalen DB-Systemen. 

1)   Unterschiede von MongoDB & relationaler DB? 

2)   Was ist das Schema bei relationalen Datenbanken? 

3)   Erklären Sie die Unterschiede zwischen relational und objektorientiert! 

4)   3 Unterschiede zwischen REST und DDD? 

5)   Wie werden Beziehungen in rel. DB, JSON Documents & Kotlin Objekten realisiert? 

6)   Wann benutzt man ReactiveCrudRepository & wann ReactiveMongoOperations? 

7)   Vergleichen Sie die Abfrage einer relationalen DB mit der Abfrage in MongoDB! 

8)   Erklären Sie 2 Pattern aus DDD, die bei Spring Data ähnlich verwendet werden? 

9)   Beschreiben Sie die 4 Stores von NoSQL-Systemen! 

10)  Warum sollte MongoDB und nicht relationale DB genutzt werden? 

11)  Was ist umständlich an MongoDB? 

12)  Wieso werden Transaktionen bei MongoDB nicht wirklich benötigt. 

13)  Beschreiben Sie, wann man bei MongoDB bei einem Schreibvorgang keine explizite Transaktion benötigt! 

14)  Beschreiben Sie, wie man sinnvollerweise interaktiv inspiziert, ob Daten in MongoDB auch wirklich
eingefügt oder aktualisiert wurden. 

1)   Beschreiben Sie, was man unter „Type-Safe Queries“ versteht. 

2)   Beschreiben Sie eine Möglichkeit, wie man in einem Spring Profile z.B. „dev“, prinzipiell die Testdaten in der
DB zurücksetzen kann.

# Tests 

1)   Was bedeutet „just Runs“ in der Syntax? 

2)   Was macht Mocking? 

3)   Was macht Funktion „every“? 

4)   Was macht die Annotation @Nested? 

5)   Was macht die Annotation @Order und warum steht in den Klammern von @Order eine 1000? 

6)   Was macht die Annotation @Disabled? 

7)   Warum und wann sollte getestet werden? 

8)   Wofür steht die Annotation @CsvSource? 

9)   Nach welcher Funktionalität sollten Testklassen aufgebaut sein orientieren sie sich an CRUD? 

10)  Nenne die bekanntesten Testarten und beschreibe Sie! 

11)  Erklären Sie AAA bei Unit-Tests! 

12)  Warum kann man bei der Testentwicklung in Kotlin von Specificationlike Test sprechen? 

13)  Was versteht man unter SoftAssertion 

14)  Was ermöglicht uns Kotest? 
Security 

1)   Was ist der Unterschied zwischen Authentifizierung und Autorisierung? 

2)   Was macht die Annotation @PreAuthorize(„hasRole(‚Rolle‘)“)? 

3)   Was ist der Unterschied zwischen einer Rolle und einer Gruppe? 

4)   Erkläre die Abkürzung SSO! 

# Logging 

1)   Welche Log-Level gibt es und für wen sind diese interessant ? 

2)   Warum {} besser als () ist, erklären Sie anhand diesem Codebeispiel? 
Apache Log4j2 kann Lazy Logging ? 

1)   Beschreiben Sie eine Log-datei? 

2)   Warum ist Trailing Comma ein tolles Feature? 

3)   Erklären Sie die Impedance Mismatch? 

4)   Beschreiben Sie die 4 Interfaces in Reactive Streams? 

# Codebeispiele 

1)   Wo ist hier der Denkfehler im Codefragment ? 

2)   Schreiben Sie den nachfolgenden Code so um, das Lambda-Ausdrücke verwendet werden. 

3)   Schreiben Sie folgenden Code mit Lambda Ausdrücken. 

4)   Was ist an folgendem Code schlecht? 

5)   Beschreiben Sie den Code nach der Syntax (Code-Fragment wurde vorgegeben von Router Function) 

6)   Beschreiben Sie folgendes Codebeispiel nach der Semantik