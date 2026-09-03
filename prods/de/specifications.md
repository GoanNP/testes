# Technische Daten

## Gemeinsame Plattform

Alle Produkte nutzen dasselbe Controller-Image. Dadurch bleiben Ersatzteil-
handhabung und Firmware-Updates im gesamten Katalog identisch.

| Eigenschaft | Wert |
| --- | --- |
| Controller | x86-64 Quad-Core, 16 GB RAM |
| Speicher | 256 GB Industrie-SSD |
| Betriebssystem | Debian 12 (gehärtetes Image) |
| Versorgungsspannung | 24 V DC ±10 % |
| Betriebstemperatur | 0 °C bis 45 °C |
| Schutzart | IP54 (Schaltschrankmontage) |

## Schnittstellen

- 2 × Gigabit-Ethernet (Werksnetz und Gerätenetz, physisch getrennt)
- 4 × USB 3.0 für Kameras, Scanner oder Servicewerkzeuge
- 1 × isolierter digitaler I/O-Block, 8 Eingänge und 8 Ausgänge
- Optionale PROFINET- oder EtherNet/IP-Zusatzkarte

## Software-Stack

```yaml
runtime:
  container: podman
  telemetry: opentelemetry
  storage: postgresql
protocols:
  - opc-ua
  - mqtt
  - modbus-tcp
```

## Zertifizierung

Die Hardware trägt CE- und UKCA-Kennzeichnung. Funktionale Sicherheit ist nicht
Teil des Basisprodukts; Sicherheitskreise stellt die umgebende Maschine bereit.
