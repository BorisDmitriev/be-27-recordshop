## Dinge, die getan werden müssen

In dieser Datei sind die Änderungen aufgeführt, die in jeder Phase vorgenommen werden müssen. Sie ist in umgekehrter chronologischer Reihenfolge geordnet, d. h. die zuletzt vorgenommenen Änderungen stehen immer ganz oben in der Datei, so dass die Leser nicht bei jeder hinzugefügten Aufgabe ganz nach unten scrollen müssen.

## Aufgabe 05 - Mongoose und Controller

In dieser Aufgabe werden unsere Controller aktualisiert, um mit unserer Datenbank zu kommunizieren. `Lowdb` wird nicht mehr benötigt, also werden wir seine Struktur loswerden. Wir werden in die Mongoose API eintauchen und Methoden einführen, die die Kommunikation mit unserer Datenbank herstellen. Mit Mongoose werden wir Daten aus der Datenbank lesen, neue Datensätze einfügen und bereits gespeicherte Daten manipulieren.

**TODO**:

1. Bitte aktualisieren Sie den `records`-Controller mit Mongoose.
2. Stellen Sie sicher, dass alle API-Endpunkte für `records` so funktionieren, wie sie sollten.
3. Wiederholen Sie den Prozess für Ihre `users` und `orders` Controller.

## Aufgabe 04 - Mongoose und Seeding

In dieser Aufgabe werden wir Mongoose vorstellen. Mongoose ist eine Object Data Modeling (ODM) Bibliothek für MongoDB und Node.js. Sie verwaltet Beziehungen zwischen Daten, bietet Schema-Validierung und wird verwendet, um zwischen Objekten im Code und der Darstellung dieser Objekte in MongoDB zu übersetzen.
Wir werden lernen, wie wir Mongoose einrichten und mit unserer Anwendung verbinden. Wir werden unsere Benutzermodelle und Schemata erstellen und genau definieren, wie ein Datensatz/Benutzer/Bestellungsobjekt aussehen wird.
Im nächsten Schritt erstellen wir eine Feed-Funktion, die unsere Datenbank mit gefälschten Daten füttert, damit wir alle unsere Endpunkte direkt nach der Initialisierung unseres Servers testen können.

**TODO**:

1. Bitte richten Sie mongoose auf Ihrem Server ein.
2. Erstellen Sie ein Datenschema und ein Modell für unsere Datensätze (`records`), Benutzer (`user`) und Bestellungen (`orders`).
3. Schreiben Sie ein Seed-Skript mit `Faker` (externe Bibliothek: https://fakerjs.dev/), das jedes Mal ausgeführt wird, wenn wir unser Projekt starten. Wenn die Datenbank leer ist, wird sie mit einigen Datensätzen, Bestellungen und Benutzern gefüttert.

## Aufgabe 03 - Routing und Fehlerbehandlung

Wie wir in der ersten Aufgabe gesehen haben, gibt es Anfragen wie `GET` und `POST`, die die Funktionalität der einzelnen Endpunkte definieren. Wir werden nun `PUT` und `DELETE` einführen.

-   Mit `PUT` wird eine bereits vorhandene Ressource aktualisiert
-   `DELETE` löscht eine bereits vorhandene Ressource.

Nachdem wir die oben genannten Anfragen für unseren Plattenladen eingeführt haben, müssen wir einige Fehlerbehandlungen vornehmen. Was passiert, wenn bei einer Anfrage etwas schief läuft? Wir müssen den Benutzer auf konsistente Weise darüber informieren, was schief gelaufen ist. Das können wir erreichen, indem wir Middleware-Funktionen schreiben, die sich um die Fehlerrückmeldungen kümmern.

**Geschichte**: Unser Kunde, der Plattenladen, möchte in der Lage sein, Datensätze in seinem Speicher zu aktualisieren und zu löschen. Außer dem Datensatzdatenmodell möchte unser Kunde zwei weitere Datenmodelle haben. Eines für die Benutzer und eines für die Bestellungen.

**TODO**:

1. Bitte erstellen Sie zwei Endpunkte (Routen) für den Shop-Betreiber

    - `records` -> ein `GET`, der alle Datensätze des Shops zurückgibt
    - `records` -> ein `POST`, der einen neuen Datensatz zur Plattensammlung hinzufügt

    Für den Moment können Sie einfach eine Zeichenkette von den obigen Endpunkten zurückgeben, nur um sicherzustellen, dass alles funktioniert.

2. Verwenden Sie `lowdb`, um eine Mock-Datenbank für unsere Platten einzurichten. Sie kann leer sein oder bereits einige "falsche" Daten enthalten. Aktualisieren Sie die obigen Routen so, dass sie genau so funktionieren, wie sie sollten.

    - `records` -> sollte alle Datensätze zurückgeben, die sich in unserer lowdb-Datenbank befinden
    - `records` -> soll einen neuen Datensatz zu unserer lowdb-Datenbank hinzufügen
