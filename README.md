# bdr RedHat OpenShift Lab Days Testprojekt
## Voraussetzungen
* Minishift lokal installiert _oder_
* Zugang zu OpenShift Online und installiertes OpenShift CLI (`oc`).

## Hello World Service bauen und deployen
1. Minishift starten
    ````
    minishift start
    ````
1. Minishift Web-Konsole öffen
    ````
    minishift console
    ````
1. Am OpenShift-Cluster anmelden
    ````
    oc login -u developer
    ````
1. In Projekt _myproject_ wechseln (sollte bereits das Standardprojekt für _devloper_ sein)
    ````
    oc project myproject
    ````
1. Maven-Projekt bauen und in OpenShift-Cluster deployen
    ````
    mvnw clean package fabric8:deploy
    ````
1. Route manuell über Web-Konsole konfigurieren
    1. Projekt _My Project_ auswählen
    1. _Aplications > Services_
    1. Service _hellow-world_ auswählen
    1. _Actions > Create Route_
    1. Standardeinstellungen übernehmen und auf _Create_ klicken
    1. _Applications Routes_ bei _hello-world_ auf Link unter Hostname klicken