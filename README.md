# Content-Management-Systeme Semesterprojekt
Umsetzung einer komplexen Webseite mit Drupal für das Device Lab der HS-Flensburg.

## VM Konfigurieren
Um vernünftig auf VM Instanz arbeiten zu können, hinterlegen wir anfangs unsere SSH Public Keys auf dem Server.
Dafür kopieren wir unsere Keys:
`pbcopy < ~/.ssh/id_rsa.pub`

Nun verbinden wir uns mit dem Server per SSH `ssh benutzername@serveradresse` und bestätigen den Zugriff mit dem Passwort.

Sind wir mit dem Server verbunden, erstellen wir eine Datei `authorized_keys` im Ordner `.ssh` im Root-Verzeichnis. Dort fügen wir die SSH Public Keys der Personen/Rechner, die sich mit dem Server verbinden sollen, ein.
