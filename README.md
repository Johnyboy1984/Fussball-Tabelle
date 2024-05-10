# Fussball-Tabelle
Home Assistant yaml -  Code für Fußball Tabellen

Habe euch mal Yaml Dateien hinzugefügt, um Fußball Tabellen in Home Assistant zu bekommen. Der Code basiert auf Yaml-Basis

Es gibt unterschiedliche Methoden, wie man die Dateien in Home Assistant hinzufügen kann. Wichtig ist bei jeder Datei, die man hinzufügt, zu prüfen, ob die Konfiguration in der Datei selber in Ordnung ist (File Editor, VS Studio Code....) und im 2. Schritt, die Konfiguration in Home Assistant selber unter den Entwicklerwerkzeugen und dann auf Konfiguration prüfen klicken, zu prüfen. Erst, wenn beides in Ordnung ist, Home Assistant neustarten.

1. Methode zum Hinzufügen in Home Assistant (in dem Verzeichnis, wo auch die Configuration.yaml ist):

   Hier ist wichtig, dass man in der Configurationen yaml folgendes hinzufügt:
   deinName der Datei (ohne.yaml): !include deinName der Datei.yaml
   
3. Methothe, die ich verwende. Habe einen Ordner namens _packages erstellt.

   Damit der Ordner in Home Assistant eingelesen wird muss man in der Configuration.yaml um folgenden Code ergänzen:

   ```yaml
   homeassistant:
     packages: !include_dir_named _packages
   ```

Um die Tabelle nun darstellen zu können, empfehle ich die Flex-Table-Card, die ihr unter HACS / Fronted findet. HACS steht für Home Assistant Community Store und muss erst installiert werden und ist somit nicht Bestandteil der Home Assistant Grund - Installation.

Für die Installation von HACS empfehle ich dir das Video von Simon42, welches du auf Youtube findest anzusehen. Hier der Link zum Video: https://www.youtube.com/watch?v=uwEzePULIyo&t=227s

Flex-Table-Card: https://github.com/custom-cards/flex-table-card

Einen Beispiel Code für die Flex-Table-Card findest du auch in meinem Beitrag.


Vielen Dank für dein Interesse und viel Erfolg beim Einfügen.

So sieht es dann aus (Beispiel für die 1. und 2. Bundesliga):
https://github.com/Johnyboy1984/Fussball-Tabelle/blob/main/Tabelle%201.%20und%202.%20Bundesliga.png
