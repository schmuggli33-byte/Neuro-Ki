# NEURO LEARN – sichere KI-Bewertung

## Was ist vorbereitet?
- `index.html` ruft die API-URL aus `ai-config.js` auf.
- `api/ai.js` ist eine Vercel-Serverless-Function.
- Der Gemini-Schlüssel wird ausschliesslich als Server-Umgebungsvariable gelesen.
- Die API bewertet sinngemäss und vergibt Teilpunkte.

## Wichtig
GitHub Pages kann keine Node.js-API-Funktion ausführen. Die Website bleibt auf GitHub Pages; der API-Server wird separat gehostet (hier: Vercel).

## Einrichtung
1. Erstelle ein Vercel-Projekt und importiere dieses GitHub-Repository.
2. In Vercel unter Project Settings -> Environment Variables:
   - Name: GEMINI_API_KEY
   - Value: dein privater Schlüssel aus Google AI Studio
   - Nur für die benötigten Deployments aktivieren.
3. Optional:
   - APP_ORIGIN = https://schmuggli33-byte.github.io
   - GEMINI_MODEL = gemini-3.5-flash-lite
4. Deploye das Projekt bei Vercel.
5. Kopiere die Vercel-Adresse und ändere in `ai-config.js` den Platzhalter zu:
   https://DEIN-PROJEKT.vercel.app/api/ai
6. Committe `ai-config.js` in GitHub und warte auf GitHub Pages.
7. Teste mit einer Lernkarte und einer Antwort in eigenen Worten.

## Kosten und Schutz
- Ein kostenloses Kontingent kann je nach Modell, Land, Konto und aktueller Verfügbarkeit begrenzt sein. Es ist keine dauerhafte Kostenfreiheit garantiert.
- Prüfe vor dem Aktivieren die Limits und Abrechnung im Google AI Studio.
- Die Funktion hat Eingabelimits und eine einfache In-Memory-Anfragebremse. Diese ist KEIN robuster Missbrauchsschutz für eine öffentliche Website. Vor öffentlicher Nutzung sollte ein persistenter Rate-Limiter und ein tägliches Budgetlimit ergänzt werden.
- Teile den API-Schlüssel niemals in HTML, JavaScript im Browser, GitHub, Screenshots oder Chat.
- Schicke keine persönlichen Daten, Passwörter oder vertraulichen Schulunterlagen an die KI.
