## Ziele von Microservices

* neue Funktionalität schnell bereistellen, da weniger Tests nötig als bei großen Servern

* agile Entwicklung, kleinere von einander unabhängige Teams

* ein Microservice = ein Bounded Context = eine Deployment Unit

* The Microservice archiectural style is an approach to developing a single applicateion as a suite of a small service, each running in its own process and communictaing with ligthweigt mmechanisms, often an HTTP resource API

# Reactive Rogramming und Multi-Threading

## Anforderungen an Server-Anwendungen
* Heterogene Clients müssen "bedient" werden: Smartphones, Tablets, Desktops, IoT-Geräte
* schnelle Antwortzeit
* immer Verfügbar
* Big Data, es fallen große Datenmengen an vorallem bei IoT

## Threads, Stack und Heap

* Thread: 

    * ein Thread entspricht einem Ausführungsstrang.
    * lineare Abarbeitung der Anweisungen.
    * Multi-Trhreading: paralles Ausführen der Threads
    * Mehre Threads gehören zu einem Betriebssytemprozess, all diese teilen sich den Heap
    
* Stack: 

    * jeder Thread hat genau einen Stack auf dem alle Anweisungen des Threads gespeichert werden.
    * Abarbetien nach dem Lifo Prinzip
    * Auch Referenzen auf Argumente und lokolae Variablen enthalten
    * Größe des Stacks wird beim Start des Threads bestimmt

    * Heap:

    * "Halde" , "Haufen"
    * für dynamische Speicherallokation 
    * wenn ein Thread Objekte beim Ablauf erzeugt, werden diese im Heap gespeichert
    * wenn ein Thread ein Object anlegt können alle Threads im selben Prozess auch darauf zufreifen
    * zum Schutz vor Memory Leaks Garbage Collector der nicht genutzte Objekte im Heap "collected" löscht.

## Scheduling von Threads:

* sequentielles Ausführen 1 Thread nach dem anderen
* preemptive: Timeslice, festgellegte Zeit für einen Thread, wenn ein Thread nicht fertig wird, wird der Rest ausgelagert. Es werden solange erst andere Threads ausgeführt. Danach wird der Rest des ersten Threads ausgeführt

## typische Probleme mit Threads
    
* Kontextwechsel sind teuer. 
* Ziel: mehrere Threads teilen sich ein CPU Kern
* Scheduler steuert wann Threads unterbrochen und zu einem anderen Thread gewechselt wird
* Anzahl der parallelen Threads ist durch das Betriebssystem begrenzt.

## Thread per Request und Blockierungen

* Problem:

    * Threads müssen z.B auf einen Datenbankzugriff, einen xternen Sevices oder ein ERP-Service warten und blockiern solange Ressourcen
    * bei vielen Threads führt das zu einer immensen Hauptspeicheranforderung
    * auch C10K Problem: 10000 Clients, 2 MB pro Stack = 20 GB Hauptspeicher nur für Thread-Management aber während ein Thread blockiert ist keine Nutzung des CPUs sondern nur Belegung des Hauptspeichers = Ressourcen Verschwendung

* Lösung: 
        
     * in Kotlin werden statt Threads Corotinen gestartet, deutlich effinzienter  als Threads.
    * Wenn ein Request abgesetzt wird kein eigenener Thread gestartet, sondern es gibt einen Request Handler der sich um die Requests kümmert.
    * der Request Handler nimmt Anfragen entegegen und startet durch einen magischen Algoritmus nur so viele Threads wie gerade notwendig sind und steuert die Ausführung der Threads
    * die Worker Threads sarten den Aufruf warten aber nicht auf das Ergebniss und ein freier Threads aus dem Thread-Pool nimmt das Ergebniss später an und leitet es an den Request Handler weiter
    * führt zu besserer Skalierung da weniger Threads benötigt werden, aber etwas höheren Aufwand für das Thread-Management.
    * Verstehen zusammen mit 1-architektur Folie 34, 35
    * Kotlin macht thread Management automatisch durch das Stichwort suspend vor einer Funktion.

* um nicht blockierend zu coden benötigt man Reactive Programming

    * bei C# durch RX.Net
    * bei JavaScript durch RxJS
    * bei Java durch RxJava oder Project Reactor oder Fibers ab Java 14
    * bei Kotlin durch Coroutines

## Was ist Reactive Programming

* auf Ergeignisse reagieren anstatt den Ablauf zu steuern
* Streaming von Events funktionales verarbeiten der Events

* Ziele: 
    * nicht blockiernd vorallem bei Zugriff auf externe Ressourcen
    * sehr viele Request gleichzeitig bedienen
    * Vorkehrung zum Umngang mit Überlast. Heißt Umleitung im Überlast Fall auf z.B einen anderen Server.

##  Nur noch Reactive Programming ? 
 
* mit Sicherheit nicht
* es gibt viele Anwendungen bei der imperative Programmierung funktioniert, warum also umstellen solange keine Skalierungsprobleme aufterten.
* imperative is simple until it is not.

# Codequalität

* gute selbesterklärende Namen 
* angemessene Kommentare (am besten keine sondern Code selbserklärend aber nicht umsetzbar)
* einheitliche Formatierung
* sinnvolle Schachtelung
