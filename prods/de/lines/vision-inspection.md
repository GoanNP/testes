# Vision Inspection

Kamerabasierte Inline-Prüfung auf Oberflächenfehler, Druckqualität und
Maßtoleranzen.

## Highlights

- Bis zu 1200 Teile pro Minute bei 5 MP Auflösung.
- Fehlerklassifikationsmodell direkt am Bedienpanel nachtrainierbar.
- Ausschuss wird mit Bildnachweis 90 Tage lang protokolliert.

## Konfiguration

```json
{
  "camera": { "resolution": "2448x2048", "fps": 60 },
  "trigger": "encoder",
  "model": "surface-defect-v4",
  "confidenceThreshold": 0.82
}
```

## Ergebnisse

| Kennzahl | Vorher | Nachher |
| --- | --- | --- |
| Durchgeschlüpfte Fehler | 1,8 % | 0,2 % |
| Manueller Prüfaufwand | 2 Bediener | 0,5 Bediener |
| Linienstillstand pro Schicht | 22 min | 7 min |

## Einschränkungen

Transparente und spiegelnde Oberflächen erfordern ein zusätzliches
Beleuchtungspaket, das nicht zum Standardumfang gehört.
