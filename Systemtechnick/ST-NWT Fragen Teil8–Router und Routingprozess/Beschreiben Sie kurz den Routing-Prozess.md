![[Снимок экрана 2023-01-22 в 17.59.05.png]]

Lokales oder Remote Netzwerk?-durchUndieren(d.h. es wird die Netzwerkadresse ermittelt) →
	1.Wenn lokal→direkte Zustellung(ARP löst IP-Adresse noch inMac-Adresse auf)
	2.Wenn Remote→lokale Routingtabelle (Anzeige „route print“) →Standardgateway→Routing →Routingtabelle (kürzester Weg zum Ziel) →nächster Router →bis Zielerreicht ist (Hops -1)→wenn TTL*)= 0 wird das Datenpaket gelöscht