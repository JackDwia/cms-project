# Content-Management-Systeme Semesterprojekt
Umsetzung einer komplexen Webseite mit Drupal für das Device Lab der HS-Flensburg.

## VM Konfigurieren
Um vernünftig auf VM Instanz arbeiten zu können, hinterlegen wir anfangs unsere SSH Public Keys auf dem Server.
Dafür kopieren wir unsere Keys:
`pbcopy < ~/.ssh/id_rsa.pub`

Nun verbinden wir uns mit dem Server per SSH `ssh benutzername@serveradresse` und bestätigen den Zugriff mit dem Passwort.

Sind wir mit dem Server verbunden, erstellen wir eine Datei `authorized_keys` im Ordner `.ssh` im Root-Verzeichnis. Dort fügen wir die SSH Public Keys der Personen/Rechner, die sich mit dem Server verbinden sollen, ein.

### Server shortcuts 

#### Services

`sudo service --status-all`
`sudo service nginx restart`
`sudo service php restart`

## Deployment

Simples Deployment, bzw. das Versenden von Daten auf den Server erfolgt durch `rsync`. Bauen wir uns unser Kommando zusammen, bekommen wir:

`rsync -av -e "ssh" index.html benutzername@serveradresse:/var/www/cmsha/web/`

Hiermit schicken wir vom aktuellen Verzeichnis, wo das Kommando ausgeführt wird, eine Datein namens `index.html` in das Verzeichnis: `/var/www/cmsha/web/`
