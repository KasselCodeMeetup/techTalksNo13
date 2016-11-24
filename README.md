# techTalksNo13
Content from the 13th KasselCodeMeetup TechTalks

## Was is'n Graphdatenbank?

Um die Beispiele laufen zu lassen ist gar nicht viel nötig.

Datenbank starten mit docker `run -p 7474:7474 -p 7687:7687 -d neo4j:3.0` und schon ist die Datenbank einsatzbereit.
Der erste Port ist für den Zugriff via HTTP, der zweite über das binäre Bolt-Protokoll.
Jetzt im Browser [http://localhost:7474](http://localhost:7474) öffnen und loslegen :-) 

Nach dem ersten `:server connect` muss das Standardpasswort geändert werden. 
Jetzt ist ein erneutes `:server connect` notwendig und das Frontend ist mit der Datenbank verbunden.
Mittels `:play movies` kann die Beispieldatenbank mit Filmdaten eingespielt werden. 

Das [neo4j-movies-java-bolt](https://github.com/neo4j-examples/neo4j-movies-java-bolt) Beispiel setzt die Movies-Datenbank voraus. 
Damit die Sache läuft muss entweder in der `Util.java` die default URL geändert oder die Umgebungsvariable `NEO4J_URL` entsprechend gesetzt werden.
Danach kann die App mit `mvn compile exec:java` gestartet werden und läuft dann auf [http://localhost:8080](http://localhost:8080).

Das Beispiel [movies-java-spring-data-neo4j-4](https://github.com/neo4j-examples/movies-java-spring-data-neo4j-4) ist ganz gut geeignet, um die Integration in Spring und den `Object Graph Mapper (OGM)` kennen zu lernen.
Für einen Überblick über Spring Data Neo4J empfehle ich auch [Good Relations](http://docs.spring.io/spring-data/neo4j/docs/current/reference/html/)
Allerdings passen die Beispiele auf spring.io und die Beispiele auf github nicht immer so ganz zusammen.
Es gibt schlicht mehrere Arten und Weisen um mit der DB zu sprechen und die werden da ein bisschen vermischt.

_Viel Erfolg! -- Christoph_

