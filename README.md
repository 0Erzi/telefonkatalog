"# Telefonkatalog" 
Oppsett av telefonkatalogen på Raspberry Pi

1. Lag et GitHub-repo

2. Opprett et nytt GitHub-repo (sørg for at det er offentlig) for telefonkatalogen.
Repoet skal inneholde all kode (Python) og eventuelt databasescript som trengs for oppsett.
3. Lag et Kanban-board

4. Bryt opp alle stegene i oppgaver for prosjektet ditt.
Klargjør Raspberry Pi
Klargjør Raspberry Pi

5. Bruk Raspberry Pi Imager for å skrive operativsystemet til et microSD-kort.
Sett inn microSD-kortet i Raspberry Pi

6. Sett inn microSD-kortet i din Raspberry Pi og koble til strøm, skjerm og tastatur.
Følg oppstartsprosessen for å konfigurere Raspberry Pi

7. Konfigurer Raspberry Pi (språk, nettverk osv.).
Installer nødvendige pakker
Installer SSH-server på Raspberry Pi

8. Kjør:
Kopier kode
"sudo apt install openssh-server"
Start SSH-serveren med:
Kopier kode
"sudo systemctl start ssh"
Sjekk statusen med:
"sudo ufw status"

9. Installer Python 3, Git og MariaDB
Kjør følgende kommandoer for å installere nødvendige pakker:

"sudo apt install python3 python3-pip git mariadb-server"

10. Sikre MariaDB-installasjonen
Kjør:
"sudo mysql_secure_installation"

11. Sett opp et root-passord og sikre databasen.
Lag ny database-bruker og sett riktige rettigheter
a. Logg inn i MariaDB:
"sudo mariadb -u root"


b. Lag ny bruker:
sql
Kopier kode
"CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';"

c. Gi ny bruker rettigheter:
sql
Kopier kode
"GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost';"

d. Oppdater rettigheter:
sql
Kopier kode
"FLUSH PRIVILEGES;"


12. Oppdater programvaren på Raspberry Pi
Åpne terminalen og kjør:
"sudo apt update"
"sudo apt upgrade"


13. Klon og start prosjektet
Finn IP-adressen til Raspberry Pi

Kjør:
ip a
for å finne IP-adressen.

13. Klon repoet til Raspberry Pi
Klon repoet for å kunne legge til og endre filer:
Kopier kode
"git clone https://github.com/[ditt-brukernavn]/telefonkatalog.git"

14. Gå deretter inn i prosjektmappen:
Kopier kode
"cd telefonkatalog"


15. Start telefonkatalog-applikasjonen

Kjør:
"python3 dittFilnavn.py"
Sjekk at alle nødvendige biblioteker er installert før du kjører applikasjonen.


--------------------------------------------------------------------------------------

Testing og Iterasjon
Iterativ prosess med læringspartner
La læringspartner følge instruksjonene nøyaktig og bokstavelig for å teste oppsettet.
Rett opp eventuelle uklarheter som oppstår, og oppdater dokumentasjonen i GitHub-repoet.
Gjenta prosessen til veiledningen er så god at en ny bruker kan sette opp alt ved å følge den.
