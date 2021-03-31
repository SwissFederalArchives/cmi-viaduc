[English](readme_en.md) :point_left:

# cmi-viaduc
- **[cmi-viaduc](https://github.com/SwissFederalArchives/cmi-viaduc)**  :triangular_flag_on_post:
   - [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core)
   - [cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)
   - [cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)
   - [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)

# Einleitung
Viaduc war der Projektname für die Entwicklung des Online-Zugangs des Schweizerischen Bundesarchivs (webOZ).

Der Online-Zugang des BAR kann als digitaler Lesesaal bezeichnet werden, da er ein Grossteil der Aufgaben des Archivs über die digitale Platform abwickeln kann. 
Die folgenden Merkmale sind hervorzuheben:
- Suche in öffentlichen Metadaten und Primärdaten.
- Suche in geschützten Metadaten und Primärdaten für berechtigte Benutzer.
- Differenziertes Berechtigungskonzept für den Zugriff auf Meta- und Primärdaten anhand des angemeldeten Benutzers.
- Herunterladen von Primärdaten (DIP) als Gebrauchskopie.
- Bestellung von Archivalien als Digitalisat. (Die Archivalien werden zeitnah digitalisiert und dem Benutzer
zugänglich gemacht.)
- Aufbereitung der Gebrauchskopie umfasst
  - OCR Erkennung von Scans
  - Formatumwandlug von Archiv- in Benutzerformate
- Speicherung im Cache von öffentlichen Gebrauchskopien
- Stellen von Einsichtsgesuchen
- Zeitliche befristete Freigabe von Unterlagen an bewilligte Personen
- Zugriff der Verwaltung auf eigene Unterlagen
- Interne Web-Applikation zur Verwaltung der Bestellungen, Einsichtsgesuche, Verwaltungszugriff und Einstellungen.

Damit die Archivgemeinschaft von den Investitionen, Erkenntnissen und der verschiedenen Problemlösungen profitieren kann, hat das BAR beschlossen den Source-Code Open-Source zur
Verfügung zu stellen.

# Übersicht
Die Gesamtlösung des Online-Zugangs des Bundesarchivs (webOZ) umfasst 4 Code Repositories. 

Das Repository [cmi-viaduc-web-core](https://github.com/SwissFederalArchives/cmi-viaduc-web-core) ist eine Angular-Library. 
Diese Library wird in den beiden anderen Applikationen öffentlicher Zugang ([cmi-viaduc-web-frontend](https://github.com/SwissFederalArchives/cmi-viaduc-web-frontend)) und die interne Verwaltungsapplikation ([cmi-viaduc-web-management](https://github.com/SwissFederalArchives/cmi-viaduc-web-management)) als gemeinsame Codebasis und Komponentenbibliothek verwendet. 
Die Frontend-Applikationen werden in einem `ASP.NET` Container (siehe Backend-Repository [cmi-viaduc-backend](https://github.com/SwissFederalArchives/cmi-viaduc-backend)) gehostet und kommunizieren via Web-API mit dem System.

![Kontext in Big-Picture](docs/imgs/context.svg)

# Bemerkungen
Dieser Code wurde im spezifischen Kontext des Schweizerischen Bundesarchivs entwickelt. Er enthält an manchen Orten hartcodierte Links zu verschiedenen Diensten, die in diesem Zusammenhang verwendet werden, namentlich

- URLs zu Seiten anderer Dienste der Bundesverwaltung ( *\.admin.ch ) 
- URLs zum Public-Client und zum Management-Client ( https://www.recherche.bar.admin.ch.*) 
- URLs zu Authentifizierungsdiensten (E-IAM und Swisscom) ( https://www.recherche.bar.admin.ch/private | https://dis.swisscom.ch/* )
- URLs zu Chatbot- und Co-Browsing-Diensten ( https://chatbot.bar.smartive.cloud/* | https://unblu.cloud/unblu/* )

Diese können nach Bedarf ersetzt werden, um den Code an die spezifische Umgebung anzupassen

# Autoren
- [CM Informatik AG](https://cmiag.ch)
- [Evelix GmbH](https://evelix.ch)

# Lizenz
Alle Repositories stehen unter derselben Lizenz:
GNU Affero General Public License (AGPLv3), siehe [LICENSE](LICENSE.TXT)

# Projektstatus
Das initiale Entwicklungsprojekt ist abgeschlossen, zurzeit befindet sich der webOZ in der Wartung/Weiterenticklungsphase.
Es ist geplant, jährlich punktuelle Weiterentwicklungen, Korrekturen und Verbesserungen vorzunehmen und diese hier zu publizieren.

# Mitwirken
Hierbei handelt es sich um eine Kopie, welche regelmässig aktualisiert wird - daher sind Beiträge via Pull-Requests nicht möglich. Eigenständige Kopien (Forks) sind jedoch möglich unter der Berücksichtigung der AGPLV3 Lizenz.

# Kontakt
Bei Fragen zu allgemeinen Themen (und fachlicher Support) steht das schweizerische Bundesarchiv mit der E-Mail bundesarchiv@bar.admin.ch zur Verfügung.

Bei technischen Fragen oder Problemen betreffend Quellcode können diese im GitHub mittels "Issue" verfasst werden.