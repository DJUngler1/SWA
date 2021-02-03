# Kapitel 1 Was ist Softwarearchhitektur

* zeigen BPM Hamburger Hafen

## Standardsoftware mit der eigene Software höufig gekopplt wird:

* Excel (leider)
* SAP ERP
* Cas (Computer aided sales)
* abas (SAP ERP System für kleine und mittleständische Unternehmen) in Karlsruhe

## Unterschied Excel und DB System: 

* Datenbank hat ein Schema Excel nicht
* mehre Clients auf der Datenbak möglich
* Benutzer, Gruppen, Rechte im DB System
* DB-Systeme haben Transaktionen

## Was sind Transaktionen: 

* Jede Transaktion hat begin of Transaction als Star tund Commit als Ende dazwischen Datenbankoperationen z.B SELECT FROM, UPDATE, INSERT INTO, DELETE ...
* Commit dauerhaftes abspeichern der durchgeführten Änderungen in der Datenbank
* Statt Commit auch Roll Back möglich, Rückgängig machen aller Operationen der Transaktion. Zurücksetzen der DB auf den Stand der vor Beginn der Transaktion

* noch mehr Hamburger Hafen blabla :(

## typische Programmiersprachen bei Altanwendungen in der freien Wirtschaft:

* Cobol
* Pascal
* C++
* PEARL
* Assembler (hofentlich nicht, wenn gesehen abhauen)
* Java 

* Jahr 2000 Problem, Problem mit Datumsvergleich, 99 zu 00, Komplette Umstellung nötig 

* Um Übersicht über einen Prozess zu erstellen laut Jürgen nicht immer korrektes UML nötig, die Verständlichkeit ist wichtiger

## 3 Schichtenarchitektur:

* Präsentationschicht: Darstellung der Daten und Zugriff auf die Daten, mit z.B REST, RSocker, GraphQL, gRPC, HTML-Seiten
* Anwendungskern: Implementierung der Use Cases losgeslöst von konkretem Datenbanksystem. Im englischen Service Layer oder Business Layer. Beziehung der Daten aus der Datenbankzugirffschickt und Weiterleitung der Daten an die Präsentationschicht
* Datenbankzugriffsschicht: Implementierung des Datenbankzugriffs 

## Probleme bei Monolithen:

* langsames Deployment, durch immer größere Software
* Abgrenzung der Komponenten mit zunehmender Größe immer unklarer, schwierigere Aufteileilung in Teilteams
* alle Teilkomponenten müssen gleiche Technologiebasis haben
* Schlechtere Skalierung bei zunehmender Datenmenge
* Handhabung mit IDEs wird immer schwerer bei großen Projekten
* -> immer mehr Unternehmen zerlegen ihre Server

# Domain Driven Design

* Motivation: Entwurf orientiert sich hauptsächlich an der fachlichen Logik

* Unterschied zu UML, keine graphische Darstellung.

* Ergänzung zu UML KEINE Alternative

## Aufbau DDD

## Entities

* Datenobjekte mit eindeutiger unveränderlicher Identität.
* zusäztlich kann ein Entity noch weitere Eigenschaften haben

## Aggregate 

* Aggregation (z.T auch Komposition) der einzelnen Entittys.
* Aggregate Root einzige Schnittstelle nach draußen.
* Untergerordnete Entitys sind von außen nicht direkt zugreibar.
* Aggragate sind eine transaktionale Einheit, heißt sie sind in sich atomar und konsistent

## Value Object

* kleine unveränderliche Objekte. z.B Adresse wird als unveränderliches Object statt als String implementiert

## Bounded Contect

* Abgrenzung dessen was wir betrachten wollen zum Rest
* Logische Gruppierung von zusammenhöngender Funktionalität
* jeder BC hat eigenes Domainmodell
* Bounded Context orientiert sich an den Geschäftsvorfällen
* Wenn eine neue Funktionalität zu realisieren ist wird sie innerhalb von einem BC realisiert. 
* Bounded Context = eigenes Projekt in IDE
 
 ## Repository

* Abstraktion des Persistenz-Mechanismus. 
* Über Repositorys werden Operationen auf der Datenbank ausgeführt, sodass man nich explizit SQL oder ähnliches schreiben muss sondern die Aufrufe in der Operationen mit der gewünschten Programiersprache ausführen kann.

## Service 

* Modellierung der fachlichen Logik, mit Entities, Value Objects, Repositories
* im Service selbst interresiert uns weder woher die Daten kommmen (erledigt das Reposistory) noch wie die Daten dargestellt werden
* Zustandslos das heißt Services haben keine Properties 
* Implementieurng in Spring durch annotieren der erstellten Service Klasse mit @Service


