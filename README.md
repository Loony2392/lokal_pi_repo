Raspberry Pi Lokales Repository Docker-Container
Dieses Repository enthält ein Docker-Setup zum Erstellen und Betreiben eines lokalen Spiegels des Raspberry Pi Debian-Repositories sowie ausgewählter Python-Pakete.

Inhalt
Deutsch
Voraussetzungen
Anleitung
Hinweise
English
Prerequisites
Instructions
Notes
Deutsch
Voraussetzungen
Docker
Docker Compose
Anleitung
Repository klonen

bash
Copy code
git clone <URL des Repositories>
cd <Verzeichnis des Repositories>
Docker-Container bauen und starten

bash
Copy code
docker-compose up --build
Konfiguration des Raspberry Pi

Bearbeiten Sie die /etc/apt/sources.list-Datei auf Ihrem Raspberry Pi:

bash
Copy code
sudo nano /etc/apt/sources.list
Fügen Sie die folgende Zeile am Anfang der Datei hinzu:

perl
Copy code
deb http://<Ihre IP-Adresse> /raspberry/
Überprüfung des Aktualisierungsdatums

Sie können das Datum der letzten Aktualisierung überprüfen:

arduino
Copy code
http://<Ihre IP-Adresse>/last_update.txt
Hinweise
Der Container verwendet Port 80. Stellen Sie sicher, dass dieser Port verfügbar ist.
Das Hosten eines eigenen Repository-Spiegels kann erhebliche Bandbreite und Speicherplatz erfordern.
English
Prerequisites
Docker
Docker Compose
Instructions
Clone the repository

bash
Copy code
git clone <repository URL>
cd <repository directory>
Build and start the Docker container

bash
Copy code
docker-compose up --build
Configure your Raspberry Pi

Edit the /etc/apt/sources.list file on your Raspberry Pi:

bash
Copy code
sudo nano /etc/apt/sources.list
Add the following line at the beginning of the file:

perl
Copy code
deb http://<Your IP Address> /raspberry/
Check the date of the last update

You can check the date of the last update:

arduino
Copy code
http://<Your IP Address>/last_update.txt
Notes
The container uses port 80. Make sure this port is available.
Hosting your own repository mirror can require considerable bandwidth and storage.
