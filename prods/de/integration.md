# Integration

## Netzwerkaufbau

Jedes Produkt nutzt zwei getrennte Netzwerkschnittstellen. Die Geräte-
schnittstelle bleibt im Maschinennetz, die Werksschnittstelle überträgt nur
aggregierte Daten.

```
[ Maschinennetz 192.168.10.0/24 ]---( eth1 )  Produkt  ( eth0 )---[ Werksnetz ]
```

## Benötigte Werksdienste

| Dienst | Zweck | Port |
| --- | --- | --- |
| MQTT-Broker | Telemetrie-Uplink | 8883 |
| NTP | Zeitsynchronisation | 123 |
| Syslog-Collector | Audit und Diagnose | 6514 |

## Beispielkonfiguration Uplink

```yaml
uplink:
  broker: mqtts://broker.plant.internal:8883
  clientId: line-04-vision
  topicPrefix: plant/line-04/vision
  qos: 1
credentials:
  method: client-certificate
  certPath: /etc/product/certs/device.pem
```

## Checkliste Inbetriebnahme

- [ ] Statische IP-Adressen auf beiden Schnittstellen vergeben
- [ ] Gerätezertifikat installiert und validiert
- [ ] Zeitquelle erreichbar, Abweichung unter 50 ms
- [ ] Schattenbetrieb über eine volle Schicht abgeschlossen
