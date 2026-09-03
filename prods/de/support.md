# Support

## Service-Level

| Stufe | Reaktionszeit | Abdeckung |
| --- | --- | --- |
| Standard | 8 Arbeitsstunden | Mo–Fr, 08:00–17:00 |
| Erweitert | 4 Stunden | Mo–Sa, 06:00–22:00 |
| Kritische Linie | 1 Stunde | 24 / 7 |

## Diagnosepaket

Vor dem Öffnen eines Tickets bitte das Diagnosepaket erzeugen:

```bash
productctl diagnostics collect --since 24h --output /tmp/bundle.tar.gz
```

Das Paket enthält Konfiguration, Logs und die letzten 500 Ereignisse. Bilddaten
werden nur mit `--include-images` aufgenommen.

## Häufige Probleme

**Uplink bleibt getrennt.** Prüfen, ob das Gerätezertifikat abgelaufen ist und
ob der ausgehende Port 8883 offen ist.

**Zykluszeit verschlechtert sich.** Meist ein voller lokaler Puffer. Freien
Speicherplatz und die Aufbewahrungseinstellung prüfen.

**Bedienpanel zeigt veraltete Werte.** Panel-Dienst neu starten; die
darunterliegende Pipeline läuft während des Neustarts weiter.

## Ersatzteile

Ersatz-Controller werden vorinstalliert geliefert. Nach einem Controllertausch
muss das Gerätezertifikat neu ausgestellt werden.
