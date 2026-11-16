# Projektboard – Concept Art Hannover

Web-App zur Projektverwaltung im Team: Kacheln je Projekt (verschiebbar), Notizen direkt in der Kachel, Wochen- und Tagesplanung mit Drag & Drop.

**App:** https://jruppin.github.io/projektboard/

## Technik
- Reine statische Seite (`index.html`), gehostet über GitHub Pages
- Daten und Live-Abgleich: Firebase Cloud Firestore (Spark-Tarif, Standort Frankfurt)
- Anmeldung: Firebase Authentication (E-Mail/Passwort, E-Mail-Bestätigung Pflicht)
- Drag & Drop: SortableJS

## Zugang nur auf Einladung
Der Admin lädt Personen in der App unter **Team** per E-Mail-Adresse ein. Nur eingeladene Adressen mit bestätigter E-Mail können Daten lesen oder schreiben; das erzwingen die Firestore-Sicherheitsregeln (`firestore.rules`, dort ist die Admin-Adresse als Platzhalter `ADMIN_EMAIL` eingetragen – die echte Adresse steht nur in der Firebase Console).

## Dateien
- `index.html` – die App
- `firebase-config.js` – öffentliche Firebase-Web-Konfiguration
- `firestore.rules` – Sicherheitsregeln (Referenz; aktiv sind die in der Firebase Console veröffentlichten)
