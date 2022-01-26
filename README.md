# Express Post Calculator

Wir programmieren einen Server, der einige Rechen-Operationen ausführen kann

**Endpunkte**
* `GET /` -> Statusmeldung: Server is running
* `POST /` -> Führt eine Rechnung aus und schickt das Ergebnis zurück

## Status Meldung
Die Route `/` soll bei einem GET Request nur den Text 'Server is running' mit dem Statuscode 200 zurück shcicken.

## Rechner
Bei einem POST Request auf die Route `/` soll eine von mehreren Rechenoperationen ausgeführt werden.
### Post-Daten
```
{
    "command": "sum",
    "data": [1, 2, 3, 4]
}
```
**comand** kann entweder **sum** oder **avg** sein. Bei ienem falschen Command soll ein Fehler code 404 zurück geschickt werden.  
**data** soll ein Array mit Zahlen sein. Falls es kein Array gibt oder das Array leer ist, soll imer **0** zurück gegeben werden.