# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.


---
## My Documentation 
1. redirectToAuthCodeFlow(clientId)
Startet den Spotify-Login-Prozess.
Erstellt eine sichere Challenge (PKCE), speichert den Verifier im Local Storage und leitet den Nutzer zur Spotify-Loginseite weiter.

2. generateCodeVerifier(length)
Erzeugt einen zufälligen String (Code Verifier) mit der gewünschten Länge.
Dieser wird für die PKCE-Authentifizierung benötigt.

3. generateCodeChallenge(codeVerifier)
Erstellt aus dem Code Verifier eine Challenge (SHA-256 Hash, base64-url-kodiert).
Diese Challenge wird an Spotify gesendet, um die Sicherheit zu erhöhen.

4. getAccessToken(clientId, code)
Tauscht den von Spotify erhaltenen Code gegen ein Access Token ein.
Sendet dazu eine POST-Anfrage an die Spotify-API mit Client ID, Code, Redirect URI und Code Verifier.

5. fetchProfile(token)
Holt das Spotify-Profil des eingeloggten Nutzers.
Sendet eine GET-Anfrage an die Spotify-API und gibt die Profildaten als Objekt zurück.

6. populateUI(profile)
Füllt die HTML-Oberfläche mit den Profildaten des Nutzers (Name, E-Mail, Profilbild, Links usw.).