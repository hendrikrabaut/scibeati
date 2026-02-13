# UC1 – Inloggen met Spotify

Primary Actor: Gebruiker

Stakeholders: /

Precondities:
- Gebruiker beschikt over een Spotify-account

Postcondities:
- Gebruiker is succesvol ingelogd
- Access token is opgeslagen
- Systeem heeft toestemming voor relevante Spotify-data

Normaal verloop: 

1. Gebruiker klikt op “Log in met Spotify”.
2. Systeem stuurt gebruiker naar Spotify OAuth-pagina.
3. Gebruiker logt in bij Spotify.
4. Gebruiker geeft toestemming voor gevraagde rechten.
5. Spotify stuurt access token terug.
6. Gebruiker wordt ingelogd in de applicatie.

Alternatief verloop

- 4A: Gebruiker weigert toestemming
    - 4A1: Login mislukt
    - 4A2: foutmelding.
- 5A: Token vervallen
    - 5A1: Systeem vraagt opnieuw login.

Domeinspecifieke regels:

- OAuth 2.0 protocol moet gevolgd worden
- Minimale permissies (principle of least privilege)
