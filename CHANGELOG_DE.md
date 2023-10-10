# Das Änderungsprotokoll des Tutorials

Dieses Änderungsprotokoll ist in umgekehrter chronologischer Reihenfolge geordnet, d.h. die zuletzt vorgenommenen Änderungen stehen immer ganz oben in der Datei, so dass die Leser nicht bei jeder Änderung ganz nach unten scrollen müssen.

## Stufe 0: Grundgerüst

Dieser Zweig enthält ein Grundgerüst für fast jeden Express-Server, den Sie erstellen werden.  
Diese Boilerplate besteht aus:

-   Dateien, die von [`npx express-generator`](https://expressjs.com/en/starter/generator.html) erstellt wurden, unter Verwendung der `--no-view` und `--git` Flags, leicht modifiziert und modernisiert.

### Änderungen an `express-generator` Dateien:

-   `routes/index.js` und `routes/users.js` wurden aktualisiert, um `const` zu verwenden.
-   `app.js` wurde ebenfalls aktualisiert, um `const` zu verwenden. Außerdem wurden Kommentare hinzugefügt, um die Datei in kleinere, leichter lesbare Teile zu zerlegen.
