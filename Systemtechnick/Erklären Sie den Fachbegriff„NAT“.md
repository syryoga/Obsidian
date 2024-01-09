NAT steht für "Network Address Translation" und ist eine Technologie, die verwendet wird, um die öffentlichen IP-Adressen von Geräten in einem privates Netzwerk durch private IP-Adressen zu ersetzen, die innerhalb des Netzwerks verwendet werden.

NAT wird häufig verwendet, um eine begrenzte Anzahl von öffentlichen IP-Adressen effektiver zu nutzen, da eine große Anzahl von Geräten in einem privaten Netzwerk hinter einer einzigen öffentlichen IP-Adresse versteckt werden kann. Es ermöglicht auch die Verbergung der Geräte und Services innerhalb des privaten Netzwerks vor unbefugtem Zugriff von außen.

NAT arbeitet in zwei Schritten:

1.  Translation: Wenn ein Gerät innerhalb des privaten Netzwerks eine Verbindung zu einem externen Netzwerk herstellt, wird seine private IP-Adresse durch die öffentliche IP-Adresse des Routers ersetzt, der das private Netzwerk mit dem Internet verbindet.
    
2.  Mapping: Der Router erstellt eine Tabelle, die die Zuordnung von privaten und öffentlichen IP-Adressen verfolgt. Wenn Daten von außen an die öffentliche IP-Adresse des Routers gesendet werden, leitet der Router sie an das entsprechende private Gerät weiter, basierend auf der Tabelle.
    

Nat ermöglicht also, dass eine begrenzte Anzahl von öffentlichen IP-Adressen von vielen Geräten genutzt werden kann und erhöht die Sicherheit von privaten Netzwerken, indem es die Geräte vor unbefugtem Zugriff von außen versteckt.