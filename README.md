# systemtreue-status

Externe Erreichbarkeitspruefung fuer das SK Trading Journal (app.systemtreue.de, systemtreue.de).

- Laeuft alle 10 Minuten auf GitHub Actions, also ausserhalb des eigenen Servers.
- Fehlschlag (2 Versuche je Seite, kein HTTP 200) -> Karte mit Push im Cockpit.
- Ist auch das Cockpit nicht erreichbar, wird der Lauf rot -> GitHub-Fehlermail.
- Oeffentlich, weil Actions-Minuten fuer oeffentliche Repos frei sind. Enthaelt keine Geheimnisse;
  Cockpit-Adresse und Schluessel liegen als Repo-Secrets.

Probe-Alarm: Actions -> "Erreichbarkeit systemtreue" -> Run workflow -> probe_url = eine absichtlich kaputte Adresse.
