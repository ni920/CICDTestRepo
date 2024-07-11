[![json-yaml-validate](https://github.com/ni920/CICDTestRepo/actions/workflows/main.yml/badge.svg)](https://github.com/ni920/CICDTestRepo/actions/workflows/main.yml)

# Test-Umgebung

Dieses Repository dient dem testen und ausprobieren von ArgoCD

Hierzu wurden folgende Schritte ausgeführt:

- Anlegen eine Repositories
- Aktivieren von Kubernetes auf dem Mac
- Aufsetzen von ArgoCD mittels Portainer (weils einfacher ist und eine gewohnte Umgebung darstellt)
- Erstellen der YAML-Dateien für ein HelloWorld auf Basis von NGINX
  - ``helloworld-depl`` angelegt
  - ``helloworld-svc`` angelegt
  - Ordner Root angelegt mit 
    - ``Chart``und `Values`
    - Template Ordner
      - In diesem war zuvor die ArgoCD Yaml diese hat jedoch dazugeführt das es zu Problemen in ArgoCD kam weshalb ich sie entfernt habe. 
      - @Todo Schauen wo das Problem liegt..



Probleme die ich während des Testens hatte/habe:

- Zuvor lagen alle Dateien direkt in dem Git verzeichnis und nicht wie jetzt in dem Ordner ``helloworld`` dies führte dazu das ArgoCD zwar etwas angelegt hat dies aber nicht das Hello World war. 
- Port freigabe funktionierte mit der initialen Service Datei nicht zum einen fehlt der Type und der Port stimmt auch nicht hier scheint es eine bestimmte Range zu geben (Siehe Fehlermeldung ArgoCD)
- Netzwerksettings funktionieren nicht scheinbar nicht ohne weiteres hinzufügen löst Probleme aus (siehe ArgoCD)
