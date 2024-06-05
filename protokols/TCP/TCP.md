# Transmission Control Protocol (TCP)

## Was ist TCP?
TCP (Transmission Control Protocol) ist ein verbindungsorientiertes Protokoll im Transport-Layer des Internetprotokoll-Stacks. Es sorgt für die zuverlässige Übertragung von Daten zwischen Computern im Netzwerk und stellt sicher, dass die Daten in der richtigen Reihenfolge und ohne Fehler ankommen.

## Hauptmerkmale von TCP
- **Verbindungsorientiert**: TCP etabliert eine Verbindung zwischen Sender und Empfänger, bevor Daten übertragen werden. Diese Verbindung bleibt bestehen, bis alle Daten erfolgreich übertragen wurden.
- **Zuverlässigkeit**: TCP garantiert die Zustellung von Datenpaketen. Falls Pakete verloren gehen oder beschädigt werden, werden sie erneut gesendet.
- **Flusskontrolle**: TCP steuert den Datenfluss zwischen Sender und Empfänger, um Überlastungen zu vermeiden.
- **Fehlerkorrektur**: TCP nutzt Prüfsummen zur Fehlererkennung und sendet beschädigte Pakete erneut.
- **Sequenzierung**: TCP stellt sicher, dass Daten in der richtigen Reihenfolge ankommen, indem es Sequenznummern verwendet.

## TCP-Verbindungsaufbau (Three-Way Handshake)
Der Verbindungsaufbau in TCP erfolgt in drei Schritten:
1. **SYN**: Der Client sendet ein SYN-Paket (Synchronize) an den Server, um eine Verbindung anzufordern.
2. **SYN-ACK**: Der Server antwortet mit einem SYN-ACK-Paket (Synchronize-Acknowledge), um die Anfrage zu bestätigen und eine Verbindung anzubieten.
3. **ACK**: Der Client sendet ein ACK-Paket (Acknowledge), um die Verbindung zu bestätigen.

## TCP-Verbindungsabbau (Four-Way Handshake)
Der Verbindungsabbau in TCP erfolgt in vier Schritten:
1. **FIN**: Der Client oder Server sendet ein FIN-Paket (Finish), um die Verbindung zu beenden.
2. **ACK**: Der Empfänger des FIN-Pakets bestätigt den Erhalt mit einem ACK-Paket.
3. **FIN**: Der Empfänger sendet ebenfalls ein FIN-Paket, um die Verbindung zu beenden.
4. **ACK**: Der ursprüngliche Sender des FIN-Pakets bestätigt den Erhalt des zweiten FIN-Pakets mit einem ACK.

## TCP-Header
Der TCP-Header enthält mehrere wichtige Felder:
- **Quellport**: Der Port des sendenden Geräts.
- **Zielport**: Der Port des empfangenden Geräts.
- **Sequenznummer**: Die Position des ersten Datenbytes im aktuellen Segment.
- **Bestätigungsnummer**: Die nächste erwartete Sequenznummer.
- **Datenoffset**: Die Länge des TCP-Headers.
- **Flags**: Steuern die verschiedenen Steuerfunktionen (z.B., SYN, ACK, FIN).
- **Fenstergröße**: Die Größe des Empfangsfensters für die Flusskontrolle.
- **Prüfsumme**: Zur Fehlererkennung.
- **Dringendkeitszeiger**: Gibt an, ob dringende Daten vorhanden sind.

## Vorteile von TCP
- **Zuverlässigkeit**: Garantierte Zustellung von Datenpaketen.
- **Fehlerkorrektur**: Automatische Wiederholung von verlorenen oder beschädigten Paketen.
- **Datenreihenfolge**: Sicherstellung der richtigen Reihenfolge von Datenpaketen.
- **Flusskontrolle**: Vermeidung von Überlastungen und Datenverlust.

## Nachteile von TCP
- **Overhead**: Aufgrund der zusätzlichen Header-Informationen und der Mechanismen zur Sicherstellung der Zuverlässigkeit ist TCP ressourcenintensiver als verbindungslose Protokolle.
- **Latenz**: Der Verbindungsaufbau und die Fehlerkorrektur können zu Verzögerungen führen.

